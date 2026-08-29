# Daily post — the routine

Run by the scheduled Cowork task. Follow it in order. **Step 2 is the one that
matters**; everything else is mechanics.

---

## Step 0 — decide whether there is an article today

There is an article today if at least one of these is true:

- a standards body published or revised something (VESA, HDMI Forum, USB-IF,
  Bluetooth SIG, JEDEC, 3GPP);
- a product entered the public record via a manufacturer spec page, a datasheet,
  a certification listing or a published model card;
- an independent lab published a measurement that contradicts a widely repeated
  claim, or enough outlets have now tested a notable product to support a
  **review round-up**;
- there is an evergreen query in the backlog that nobody has answered honestly,
  and the primary documents to answer it exist and are readable today.

There is **no** article today if the only available angle requires restating
someone else's reporting, or asserting a measurement nobody published. Skip the
day. A thin post costs more than a missing one.

---

## Step 1 — pick the query, not the topic

Write to a question a person types, not a subject area. "Is 120 W fast charging
actually better" is a query. "Charging technology overview" is a subject area, and
subject areas rank nowhere.

Check `content/posts/` first. If a post already covers the query, **update it** —
new revision, new model, corrected figure — rather than publishing a near-duplicate.
Two articles competing for one query is self-inflicted cannibalisation.

Take the highest backlog item not yet covered. Prefer categories that are still
empty: the first post in a section is what makes that section appear in the nav.

**Restock as you go.** Each time you consume a backlog item, append at least one
new query you encountered during research to the bottom of the list. At a daily
cadence the list runs dry in about two weeks otherwise.

---

## Step 2 — read the primary documents and verify every figure

Non-negotiable, and not delegable to a search summary.

For each figure that will appear in the article:

1. Open the actual document — the standard, the manufacturer spec page, the
   datasheet, the model card, the lab's measurement page.
2. Read the figure **and its measurement condition**. A number without its test
   condition is not a fact. "1,000 nits" is meaningless until you know whether it
   is a 10% window, a full-screen flash, or sustained full-screen. "18-hour battery"
   is meaningless until you know the test loop and the screen brightness.
3. Record the **revision** and the date you read it. Spec revisions carrying the
   same name impose different requirements.
4. If a figure cannot be traced to a document, it does not go in the article. Do
   not soften it into a vaguer claim — delete it.

**Never present someone else's measurement as ours.** Attribute by name, inline.

---

## Step 3 — write

Follow `CLAUDE.md`: 1,100–1,800 words, answer the title question completely in the
first 120 words, question-form H2s, tables for comparative data, 3–5 callouts,
2–4 internal links, dated sourcing line at the close.

Re-read the **Voice** section of `CLAUDE.md` before writing, and again after. The
banned-phrase list is not decorative — a single "it's important to note" makes the
whole page read as machine-generated, and readers bounce.

Scaffold with:

```
python3 scripts/new_post.py "Headline" --category phones
```

Write the takeaways last, and write each as if it will be quoted alone with
everything else stripped away — because that is exactly what an answer engine does.

**Pick the hero deliberately.** Order is chart → photograph → typographic cover,
and `hero:` overrides it. Check the last three posts: if two led with a chart, set
`hero: photo` on this one even where a chart block exists.

**Add `video:` only when a video earns its place**, and `products:` whenever the
article discusses a buyable product — the reader should be able to check our
transcription against the manufacturer's own page.

---

## Step 4 — build, validate, publish

```
python3 build.py
python3 scripts/validate.py     # publication gate; must exit 0
git add -A && git commit -m "post: <slug>" && git push
```

On a OneDrive-mounted checkout, prefix both with `SW_DIST=/tmp/swdist`.

GitHub Actions rebuilds, revalidates and deploys. If `validate.py` fails, fix the
article — never the gate.

If `git push` fails with an authentication error, commit locally and report that
the remote has no stored credential. Do not embed a token, and do not ask anyone
to paste one into the conversation.

---

## Step 5 — after publishing

- Confirm the live URL renders and the hero image loaded.
- Add internal links **from** older relevant posts **to** the new one. New articles
  arrive orphaned, and an orphaned page gets crawled late and ranks slowly. This is
  the step most often skipped and it costs real traffic.
- If the piece supersedes an older one, update that post's `updated` date and link
  forward.

---

## Backlog — evergreen queries worth answering properly

Ordered roughly by (demand × how badly it is currently served).

### Phones
1. ~~What does "120 W fast charging" actually get you, minute by minute?~~ — done, 29 Aug 2026, `/phones/120w-fast-charging-minute-by-minute/`
2. Does a 200 MP camera sensor take better photos than a 50 MP one?
3. What is pixel binning, and why does a 200 MP phone save 12 MP files?
4. IP68 vs IP69: what is actually tested, and what voids the warranty?
5. Why does the same chip score differently in two phones?
6. What is the real difference between a Snapdragon 8 Elite and an A-series chip?
7. mAh vs Wh: which battery number should you compare?
8. Does 5G mmWave matter where you live?

### Laptops & PCs
9. ~~Why does a laptop CPU with 16 cores lose to a desktop with 8?~~ — done, 27 Aug 2026, `/computers/laptop-cores-vs-desktop-cores/`
10. What does a TDP number promise, and what do the thermals actually allow?
11. Thunderbolt 5 vs USB4 v2: what changes at the port?
12. Does RAM speed matter, or only capacity?
13. PCIe 5.0 SSDs: faster on paper, faster in practice?
14. What is a process node, and does "2 nm" measure anything physical?

### AI
15. What does a context window actually hold, in pages of text?
16. What do NPU TOPS ratings measure, and are two vendors' numbers comparable?
17. How do you read a model card without trusting the launch chart?
18. On-device vs cloud AI: what genuinely runs on your phone?
19. What is quantisation, and what does it cost you in quality?

### Displays & TVs
20. What does ClearMR certify, and how do tiers map to perceived blur?
21. Is OLED burn-in still a real risk, and what do warranties cover?
22. Why won't my 4K 144 Hz work over this HDMI cable?
23. Contrast ratio: native, dynamic, and which number the box quotes.
24. Does local dimming zone count matter more than peak brightness?
25. Why does HDR look washed out in Windows?

### Audio & Wearables
26. ~~Does LDAC actually sound better than AAC?~~ — done, 28 Aug 2026, `/audio/does-ldac-actually-sound-better-than-aac/`
27. How is active noise cancellation measured, and by whom?
28. What does "30-hour battery life" assume about volume and ANC?
29. Bluetooth latency: why your video is out of sync.

### Explainers
30. Nits, cd/m² and lumens: which one describes a screen?
31. Gbps vs GB/s, and why cable marketing mixes them.
32. What 10-bit colour requires end to end, and whether you have it.
33. What DSC does to your signal, and when it engages without telling you.
34. Refresh rate vs frame rate vs response time — three different things.

### Added 27 August 2026 (found while researching #9)
35. P-cores vs E-cores: which one is running the thing you're waiting on?
36. Why did Intel drop Hyper-Threading, and does losing SMT cost you anything?
37. "Minimum Assured Power": the ARK field that decides your laptop's speed.
38. Why two laptops with the same CPU benchmark 34% apart.
39. What does a Cinebench score actually measure, and which version should you quote?

### Added 28 August 2026 (found while researching #26)
40. What is "Hi-Res Audio Wireless", who awards it, and what does the logo require?
41. Why does a codec's bitrate depend on the Bluetooth MTU, and what sets the MTU?
42. LC3 and LE Audio: does it fix the bitrate-versus-stability problem, or move it?
43. What does RSSI in dBm mean for your headphones, and where is the cliff?
44. Why does aptX Lossless claim 1,200 kbps when CD audio is 1,411 kbps?
45. Does Android's Developer options codec picker actually change what gets negotiated?

### Added 29 August 2026 (found while researching #1)
46. What is on the EU smartphone energy label, and how do you read a model's EPREL entry?
47. What does "battery endurance in cycles" measure, and why is 800 the floor?
48. Silicon-carbon batteries: what actually changed, and what does 10,000 mAh cost you?
49. Why does a phone charge faster on a generic USB-PD brick for the first ten minutes?
50. USB PD 3.1 EPR: which phones and laptops actually negotiate 28 V, 36 V or 48 V?
51. Dual-cell phone batteries: why 120 W needs two cells in series, and what it costs in capacity.
52. What is PPS, and why does Samsung's 45 W need it while Apple's 40 W does not?
