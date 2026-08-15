---
title: "How much text actually fits in a 1M-token context window?"
slug: context-window-explained
seo_title: "What a Context Window Really Holds"
meta: "A 1M-token context window sounds infinite. Here is what it holds in real words and pages, what silently eats it, and why filling it makes answers worse."
category: ai
date: 2026-08-15
updated: 2026-08-15
description: "Context windows are quoted in tokens, which is a unit nobody thinks in. Converted into pages, the numbers get concrete fast — and so does the reason you shouldn't try to fill one."
image_alt: "Typographic cover reading: how much text fits in a 1M-token context window"
tags: [context window, tokens, LLM, Claude, OpenAI, AI, tokenizer, prompt engineering]
about: ["Anthropic", "Claude", "OpenAI", "Large language model", "Tokenization"]
hero: photo
key_takeaways:
  - text: "At OpenAI's published rule of thumb of **1 token to roughly 4 characters** of English, a **1,000,000-token** context window holds about **750,000 words** — near enough **2,500 paperback pages**."
    source: [1, 2]
  - text: "OpenAI's own worked example puts the entire US Declaration of Independence at **1,695 tokens**, so a 1M-token window would hold about **590 copies** of it."
    source: 2
  - text: "Anthropic documents a **1M-token** context window on Claude Opus 5, Opus 4.8, 4.7, 4.6, Sonnet 5, Sonnet 4.6, Fable 5 and Mythos 5, with **200k tokens** on other models including Sonnet 4.5 and Haiku 4.5."
    source: 1
  - text: "The window is not just your question. Anthropic states the system prompt, every message, tool results, images, documents and tool definitions all count against it — as does the model's own output, which on 1M-token models can reach **128,000 tokens**."
    source: 1
  - text: "Bigger is not automatically better: Anthropic states accuracy and recall degrade as token count grows, an effect it calls context rot. **4 Claude models** — Sonnet 5, Sonnet 4.6, Sonnet 4.5 and Haiku 4.5 — now track their own remaining budget to manage it."
    source: 1
  - text: "A single request can carry up to **600 images or PDF pages** on a 1M-token model, and **100** on a 200k-token model, before separate request-size limits apply."
    source: 1
faq:
  - q: "What is a token, in plain terms?"
    a: "A token is a chunk of text the model processes as one unit. It can be a whole word, part of a word, a space or a punctuation mark. OpenAI's rule of thumb for English is that one token is about four characters, or about three quarters of a word. The exact split depends on the model's tokenizer, which is why the same sentence can produce different token counts on different models."
  - q: "Does a bigger context window mean the model is smarter?"
    a: "No. Context window size describes working memory, not reasoning ability. Anthropic's documentation is explicit that more context is not automatically better, because accuracy and recall degrade as the token count grows. A model with a smaller window and better handling of what is in it can easily outperform one with a larger window stuffed full of marginally relevant text."
  - q: "Why does my conversation slow down or lose the thread near the limit?"
    a: "Because every previous turn is still in the request. Each new message carries the entire conversation history with it, so requests get progressively larger and the model has more material to search through for the relevant part. Anthropic calls the resulting degradation context rot, and it is the reason curating what stays in context matters as much as how much room there is."
  - q: "Do images count toward the context window?"
    a: "Yes. Anthropic's documentation lists images and documents among the things that count, and notes that image tokens are included in the model's token budget. A single request can include up to 600 images or PDF pages on a 1M-token model, or 100 on a 200k-token model, though you may hit separate request-size limits first."
  - q: "Does prompt caching free up context space?"
    a: "No, and this catches people out. Anthropic's documentation states plainly that cached prompt prefixes still occupy the context window — caching changes what you pay for those tokens, not whether they count. If you cache a 50,000-token system prompt, you still have 50,000 fewer tokens of room."
  - q: "What happens if I go over the limit?"
    a: "If the input alone exceeds the window, the Claude API returns a 400 error saying the prompt is too long. On Claude 4.5 models and newer, a request whose input plus requested output would exceed the window is accepted, and generation simply stops with a stop reason of model_context_window_exceeded if it reaches the ceiling. Anthropic recommends the token counting API to estimate before sending."
resources:
  - title: "Anthropic — Context windows"
    url: "https://platform.claude.com/docs/en/build-with-claude/context-windows"
    note: "The primary reference: what counts toward the window, sizes by model, overflow behaviour"
  - title: "OpenAI — What are tokens and how to count them?"
    url: "https://help.openai.com/en/articles/4936856-what-are-tokens-and-how-to-count-them"
    note: "The rules of thumb, plus worked token counts for real documents"
  - title: "OpenAI Tokenizer"
    url: "https://platform.openai.com/tokenizer"
    note: "Paste your own text and watch it split into tokens — the fastest way to build intuition"
  - title: "tiktoken"
    url: "https://github.com/openai/tiktoken"
    note: "Count tokens programmatically rather than estimating"
  - title: "Anthropic — Effective context engineering for AI agents"
    url: "https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents"
    note: "Why long contexts degrade, and how to design around it"
sources:
  - title: "Context windows — Claude Platform Docs"
    url: "https://platform.claude.com/docs/en/build-with-claude/context-windows"
    publisher: "Anthropic"
    accessed: 2026-08-15
    primary: true
  - title: "What are tokens and how to count them?"
    url: "https://help.openai.com/en/articles/4936856-what-are-tokens-and-how-to-count-them"
    publisher: "OpenAI"
    accessed: 2026-08-15
    primary: true
  - title: "Effective context engineering for AI agents"
    url: "https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents"
    publisher: "Anthropic"
    accessed: 2026-08-15
    primary: true
---

A 1,000,000-token context window holds roughly **750,000 words** of English — about 2,500 paperback pages, or the complete Harry Potter series with room left over. A 200,000-token window holds about 150,000 words, or one long novel.

Those conversions come from OpenAI's own published rule of thumb: one token is about four characters of English, or about three quarters of a word. So the honest answer to "is 1M tokens a lot?" is yes, enormously — and also that you should almost never try to fill it, for reasons the model vendors document themselves.

Here is what the number actually means, what quietly consumes it, and why a full window is a worse window.

## What is a token, and why isn't it a word?

A token is the unit a language model reads in. Not a character, not quite a word — something in between.

OpenAI's published rules of thumb for English are worth memorising, because they turn an abstract number into something you can picture:

| Quantity | Tokens |
| --- | --- |
| 1 token | about 4 characters |
| 1 token | about ¾ of a word |
| 100 tokens | about 75 words |
| 1–2 sentences | about 30 tokens |
| 1 paragraph | about 100 tokens |
| 1,500 words | about 2,048 tokens |

OpenAI also publishes worked examples on real documents, which are more useful than any ratio. The Wayne Gretzky line "You miss 100% of the shots you don't take" is **11 tokens**. The OpenAI Charter is **476 tokens**. The entire US Declaration of Independence is **1,695 tokens**.

Hold onto that last one. It is the best mental yardstick available, because most people have a rough sense of how long the Declaration is.

> [!KEY] At 1,695 tokens for the Declaration of Independence, a 1M-token context window holds about **590 copies** of it. A 200k window holds about 118.

This is the same pattern that runs through most tech specifications: a headline number quoted without the condition that makes it meaningful. It is exactly why an [HDMI port badged 2.1 can legitimately carry a third of the bandwidth you assumed](/explainers/4k-144hz-hdmi-cable/), and it is worth the same suspicion here.

One wrinkle that surprises people: the same word can become different tokens depending on where it sits. OpenAI's documentation shows "red" mid-sentence, "Red" mid-sentence and "Red" at the start of a sentence producing three different token IDs. Capitalisation and leading spaces are part of the token. Which is why the ratios above are estimates, and why both vendors point you at a real tokenizer when the count matters.

## How big are the windows, actually?

Anthropic documents a **1M-token context window** on Claude Opus 5, Opus 4.8, Opus 4.7, Opus 4.6, Sonnet 5, Sonnet 4.6, Fable 5 and Mythos 5, available on the Claude API, Amazon Bedrock, Google Cloud and Microsoft Foundry. Other models, including Claude Sonnet 4.5 and Haiku 4.5, carry **200k tokens**.

Converted to something human:

| Window | Approx. words | Roughly equivalent to |
| --- | --- | --- |
| 200,000 tokens | ~150,000 | One long novel |
| 1,000,000 tokens | ~750,000 | A seven-book series, or 590 Declarations of Independence |

Output is capped separately. On models with a 1M-token window, a single request can generate up to **128k output tokens** — and that output is part of the same budget, not additional to it.

## What actually eats your context window?

This is the part that catches everyone, and it is the reason your window fills faster than your typing suggests.

Anthropic's documentation is unambiguous: everything in the request counts. The system prompt. Every message in the conversation, including tool results, images and documents. **Your tool definitions** — the descriptions of functions the model can call, which most people never think of as content at all. And the output the model generates, including its internal thinking.

So a conversation that feels like a handful of short questions can be carrying tens of thousands of tokens of accumulated history, tool schemas and file contents before you type a word.

> [!WARNING] Prompt caching does not buy you room. Anthropic states directly that cached prefixes still occupy the context window — caching changes what you *pay* for those tokens, not whether they count.

Images are in the budget too. A single request can include up to **600 images or PDF pages** on a 1M-token model, or **100** on a 200k-token model, though Anthropic notes you may hit separate request-size limits before the token limit.

## Why is a full context window a bad context window?

Because filling it makes the model worse, and this is not a criticism from outside — it is in the vendor's own documentation.

Anthropic's context windows page states that as token count grows, accuracy and recall degrade, and gives the effect a name: **context rot**. The conclusion it draws is the useful part: curating what is in context matters just as much as how much space is available.

The intuition is straightforward. A model retrieving a relevant detail from 5,000 tokens is searching a small, clean space. The same model retrieving the same detail from 900,000 tokens of loosely related material is searching a haystack you built. More context means more opportunity for the model to latch onto something adjacent but wrong.

> [!TIP] Treat the context window as a budget with a *quality* cost, not just a capacity limit. Ten thousand tokens of exactly the right material beats half a million tokens of everything you had lying around, every time.

Some models now track this themselves. Anthropic documents **context awareness** on Claude Sonnet 5, Sonnet 4.6, Sonnet 4.5 and Haiku 4.5, where the API injects the model's total budget into the system prompt and updates it after each tool call, so the model can pace a long task against the room that remains rather than guess.

## What should you actually do about it?

> [!ACTION] Practical habits
> 1. **Count, don't estimate**, when it matters. Both vendors publish tools — OpenAI's Tokenizer and tiktoken, Anthropic's token counting API — and all of them beat multiplying by 0.75.
> 2. **Attach the section, not the document.** Ten relevant pages outperform a 400-page PDF, and cost a fraction as much.
> 3. **Start a fresh conversation** when you change topic. You are otherwise paying for, and degrading against, history that no longer applies.
> 4. **Audit your tool definitions** if you are building something. They are permanent context on every single request, and they are easy to forget entirely.
> 5. **Watch for the ceiling.** If input alone exceeds the window, the Claude API returns a 400 "prompt is too long". On Claude 4.5 and newer, an over-budget request is accepted and generation stops with a `model_context_window_exceeded` stop reason instead.

## The number worth remembering

Not 1,000,000. That figure is a ceiling, and ceilings tell you what is possible rather than what is wise.

The number worth remembering is **1,695** — the Declaration of Independence, in tokens. Once you know what roughly 1,700 tokens looks like on a page, every other context figure becomes something you can picture instead of something you have to trust. And you stop being impressed by a big window for its own sake, which is the whole point.

*Figures current as of 15 August 2026, verified against Anthropic's Claude Platform documentation on context windows and OpenAI's Help Center documentation on tokens. Token-to-word conversions are estimates derived from OpenAI's published rules of thumb for English text; tokenizers differ between models and exact counts require a tokenizer. SpecWire does not run model evaluations.*
