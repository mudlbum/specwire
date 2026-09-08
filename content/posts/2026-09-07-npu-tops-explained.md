---
title: "What do NPU TOPS ratings measure, and can you compare two vendors' numbers?"
slug: npu-tops-explained
seo_title: "NPU TOPS explained: what 45 TOPS means"
meta: "NPU TOPS is a peak arithmetic figure, not a benchmark. Here's how Intel, AMD, Qualcomm and Apple each define it, and what the one standard test measured."
category: ai
date: 2026-09-07
updated: 2026-09-07
description: "Every AI PC is sold on a TOPS number. It is a calculated ceiling, not a measurement, and the four companies quoting it don't all attach the same conditions. Here is what each spec sheet actually says, and what happens when a standard benchmark runs on the same silicon."
image_alt: "Bar chart of published peak NPU TOPS for the Apple M4, Snapdragon X Elite, Intel Core Ultra 7 258V, AMD Ryzen AI 9 HX 370 and Snapdragon X2 Elite"
tags: [NPU, TOPS, Copilot+ PC, Snapdragon X Elite, Core Ultra 200V, Ryzen AI 300, Apple M4, MLPerf Client]
about: ["Microsoft Copilot+ PC", "Qualcomm Snapdragon X Elite", "Intel Core Ultra 7 258V", "AMD Ryzen AI 9 HX 370", "Apple M4", "MLCommons MLPerf Client", "UL Procyon"]
hero: chart
key_takeaways:
  - text: "TOPS stands for trillions of operations per second. It is a calculated peak, not a measured result: Microsoft's Copilot+ PC developer guide sets the bar at an NPU that can perform more than **40 TOPS**, and does not say at what numeric precision."
    source: 1
  - text: "Intel's ARK entry for the Core Ultra 7 258V is the only one of the four spec pages that states the precision: NPU Peak TOPS (Int8) **47**, with sparsity support listed as Yes, alongside a GPU figure of **64** and an overall figure of **115**."
    source: 2
  - text: "AMD's own page for the Ryzen AI 9 HX 370 lists NPU TOPS as up to **50** and overall TOPS as up to **80**, with no precision or sparsity condition given anywhere in the specification table."
    source: 3
  - text: "Qualcomm's Snapdragon X Elite product brief, DCN 87-71417-1 Rev F, rates every X Elite SKU at **45 TOPS**, and Qualcomm's current product table lists the newer Snapdragon X2 Elite at **80 TOPS** or **85 TOPS** depending on the part number."
    source: [4, 5]
  - text: "Apple's May 2024 M4 announcement quotes the Neural Engine at **38** trillion operations per second and describes it as 60x faster than the A11 Bionic, without stating a data type in either figure."
    source: 6
  - text: "In the first standardised NPU test, MLCommons' MLPerf Client v0.6, Intel measured its own Core Ultra 9 288V NPU at **18.55** tokens per second and a **1.09** second time to first token on Llama 2 7B, on a Zenbook S 14 plugged into mains power on 28 April 2025."
    source: [7, 8]
chart:
  type: bar
  title: "Published peak NPU TOPS, by manufacturer spec page"
  y_label: "TOPS (peak, as published)"
  source: "Apple, Qualcomm, Intel ARK, AMD spec pages, read 7 Sep 2026"
  annotate_last: false
  series:
    - label: "Peak NPU TOPS"
      points: [["Apple M4", 38], ["Snapdragon X Elite", 45], ["Core Ultra 7 258V", 47], ["Ryzen AI 9 HX 370", 50], ["Snapdragon X2 Elite", 80]]
faq:
  - q: "What does TOPS actually stand for, and how is it calculated?"
    a: "Trillions of operations per second. For an NPU it is almost always worked out on paper: count the multiply-accumulate units, multiply by two because a multiply-accumulate is two operations, multiply by the clock speed. That gives a ceiling the hardware could reach if every unit were busy every cycle on the smallest data type it supports. Nothing in the figure tells you whether real software ever gets close."
  - q: "Is 47 TOPS from Intel the same as 50 TOPS from AMD or 45 TOPS from Qualcomm?"
    a: "Not necessarily, and you can't tell from the spec pages alone. Intel's ARK labels its 47 as Int8 and notes sparsity support. AMD's page for the Ryzen AI 9 HX 370 says up to 50 TOPS with no precision stated. Qualcomm's X Elite brief says 45 TOPS with no precision stated. Three numbers within 11% of each other could describe three different arithmetic conditions."
  - q: "Does Copilot+ PC certification test the NPU?"
    a: "Microsoft's published developer guidance says Copilot+ PCs have an NPU that can perform more than 40 trillion operations per second. That is a threshold on the manufacturer's rated figure, not a workload Microsoft runs on each machine. The same guide notes that many NPUs only support integer maths at low precision such as INT8, which is why models have to be quantised before they run on one."
  - q: "Why does an 80 TOPS chip only produce 20-odd tokens a second?"
    a: "Because generating text is mostly limited by how fast weights can be read from memory, not by how many multiplies the NPU can do. MLCommons quantises the MLPerf Client language models to 4-bit weights; every generated token still needs the whole model streamed through the chip once. Peak TOPS describes the arithmetic ceiling. Memory bandwidth sets the token rate, and no TOPS figure includes it."
  - q: "Which benchmark should I trust for NPU performance?"
    a: "MLPerf Client from MLCommons is the only vendor-neutral one, developed jointly by AMD, Intel, Microsoft, Nvidia and Qualcomm, and it reports two plain metrics: time to first token in seconds and tokens per second. Only runs that print the 'configuration tested by MLCommons' notice count as valid. UL's Procyon AI Computer Vision test is widely used too, but its score is a unitless index and vendors choose which precision to run."
  - q: "Does Apple's 38 TOPS for the M4 use the same yardstick as the PC chips?"
    a: "Apple's own announcement doesn't say. It states 38 trillion operations per second and a 60x improvement over the A11 Bionic, but gives no data type for either figure. Without one you cannot place it on the same axis as Intel's Int8 number with confidence, and neither Apple nor Intel publishes the calculation."
products:
  - name: "Intel Core Ultra 7 258V"
    url: "https://www.intel.com/content/www/us/en/products/sku/240957/intel-core-ultra-7-processor-258v-12m-cache-up-to-4-80-ghz/specifications.html"
    cta: "Intel ARK specifications"
    note: "The one spec page that labels its TOPS figure Int8 and lists sparsity support"
  - name: "AMD Ryzen AI 9 HX 370"
    url: "https://www.amd.com/en/products/processors/laptop/ryzen/ai-300-series/amd-ryzen-ai-9-hx-370.html"
    cta: "AMD product page"
    note: "NPU TOPS and overall TOPS under 'AI Engine Capabilities', no precision stated"
  - name: "Qualcomm Snapdragon X Elite"
    url: "https://www.qualcomm.com/laptops/products/snapdragon-x-elite"
    cta: "Qualcomm platform page"
    note: "Includes the comparison table covering every Snapdragon X, X Plus, X Elite and X2 part"
resources:
  - title: "Microsoft Learn: Develop AI applications for Copilot+ PCs"
    url: "https://learn.microsoft.com/en-us/windows/ai/npu-devices/"
    note: "The 40+ TOPS statement, plus Microsoft's own note on INT8 quantisation"
  - title: "Snapdragon X Elite Product Brief, DCN 87-71417-1 Rev F"
    url: "https://docs.qualcomm.com/doc/87-71417-1/87-71417-1_REV_F_Snapdragon_X_Elite_Product_Brief.pdf"
    note: "SKU table with NPU TOPS per part number, and the memory bandwidth figure"
  - title: "MLCommons: MLPerf Client benchmark"
    url: "https://mlcommons.org/benchmarks/client/"
    note: "How the only vendor-neutral NPU test works, what it quantises to, and what counts as a valid score"
  - title: "Intel Newsroom: full NPU support in MLPerf Client v0.6"
    url: "https://newsroom.intel.com/client-computing/intel-achieves-first-only-full-npu-support-mlperf-client-v0-6-benchmark"
    note: "Intel's own NPU tokens-per-second figure, with the test configuration in the small print"
  - title: "Apple Newsroom: Apple introduces M4 chip"
    url: "https://www.apple.com/newsroom/2024/05/apple-introduces-m4-chip/"
    note: "The 38 trillion operations per second claim in Apple's own words"
sources:
  - title: "Develop AI applications for Copilot+ PCs (Windows AI developer guide)"
    url: "https://learn.microsoft.com/en-us/windows/ai/npu-devices/"
    publisher: "Microsoft Learn"
    accessed: 2026-09-07
    primary: true
  - title: "Intel Core Ultra 7 Processor 258V — Product Specifications"
    url: "https://www.intel.com/content/www/us/en/products/sku/240957/intel-core-ultra-7-processor-258v-12m-cache-up-to-4-80-ghz/specifications.html"
    publisher: "Intel ARK"
    accessed: 2026-09-07
    primary: true
  - title: "AMD Ryzen AI 9 HX 370 — product specifications"
    url: "https://www.amd.com/en/products/processors/laptop/ryzen/ai-300-series/amd-ryzen-ai-9-hx-370.html"
    publisher: "AMD"
    accessed: 2026-09-07
    primary: true
  - title: "Snapdragon X Elite Product Brief, DCN 87-71417-1 Rev F"
    url: "https://docs.qualcomm.com/doc/87-71417-1/87-71417-1_REV_F_Snapdragon_X_Elite_Product_Brief.pdf"
    publisher: "Qualcomm Technologies"
    accessed: 2026-09-07
    primary: true
  - title: "Snapdragon X Elite platform page and Snapdragon X series comparison table"
    url: "https://www.qualcomm.com/laptops/products/snapdragon-x-elite"
    publisher: "Qualcomm Technologies"
    accessed: 2026-09-07
    primary: true
  - title: "Apple introduces M4 chip"
    url: "https://www.apple.com/newsroom/2024/05/apple-introduces-m4-chip/"
    publisher: "Apple Newsroom"
    accessed: 2026-09-07
    primary: true
  - title: "Intel Achieves First, Only Full NPU Support in MLPerf Client v0.6 Benchmark"
    url: "https://newsroom.intel.com/client-computing/intel-achieves-first-only-full-npu-support-mlperf-client-v0-6-benchmark"
    publisher: "Intel Newsroom"
    accessed: 2026-09-07
    primary: true
  - title: "MLPerf Client Benchmark"
    url: "https://mlcommons.org/benchmarks/client/"
    publisher: "MLCommons"
    accessed: 2026-09-07
    primary: true
  - title: "MLCommons Releases MLPerf Client v0.6 With Expanded Hardware Support for AI PCs"
    url: "https://mlcommons.org/2025/04/mlperf-client-v0-6/"
    publisher: "MLCommons"
    accessed: 2026-09-07
    primary: true
  - title: "Unlocking Peak AI Performance with MLPerf Client v1.0 on AMD Ryzen AI Processors"
    url: "https://www.amd.com/en/developer/resources/technical-articles/2025/unlocking-peak-ai-performance-with-mlperf-client-on-ryzen-ai-.html"
    publisher: "AMD Developer"
    accessed: 2026-09-07
    primary: true
  - title: "Tested: Intel's Lunar Lake wants you to forget Qualcomm laptops exist"
    url: "https://www.pcworld.com/article/2463714/tested-intels-lunar-lake-wants-you-to-forget-snapdragon-ever-existed.html"
    publisher: "PCWorld, September 2024"
    accessed: 2026-09-07
  - title: "Intel Core Ultra 7 Processor 266V — Product Specifications"
    url: "https://www.intel.com/content/www/us/en/products/sku/240956/intel-core-ultra-7-processor-266v-12m-cache-up-to-5-00-ghz/specifications.html"
    publisher: "Intel ARK"
    accessed: 2026-09-07
    primary: true
---

A TOPS rating is arithmetic, not a test. It's the number of multiply-accumulate units in the NPU, times two, times the clock speed: the most operations the block could complete in a second if every unit were busy on every cycle. Nobody measures it. It's calculated, and the calculation depends on which data type you count, so 47 TOPS from Intel, 50 from AMD and 45 from Qualcomm are only comparable if all three were worked out the same way. Of those three spec pages, only Intel's says how. And when a standard benchmark finally ran on these chips, the number that came out wasn't in TOPS at all. It was 18.55 tokens per second.

## What is a TOPS, physically?

Almost every operation in a neural network is a multiply followed by an add: take a weight, multiply it by an input, add the result to a running total. Hardware people call that pair a multiply-accumulate, or MAC, and count it as two operations. An NPU is mostly a large grid of MAC units with some memory around them. So the peak figure is MAC count × 2 × clock frequency, and the "T" is just the word trillion.

Two things about that formula matter more than the result.

First, the count changes with the width of the numbers. A MAC unit built for 16-bit floating-point values can usually be split to do two 8-bit integer operations in the same cycle, and sometimes four 4-bit ones. So the same silicon can be honestly described as X TOPS at FP16, 2X at INT8 and 4X at INT4. The PC market has settled on INT8 by convention, and the spec pages below show how loosely the convention is followed.

Second, some NPUs support structured sparsity: if a model has been prepared so that a fixed fraction of its weights are zero, the hardware skips them and roughly doubles throughput. A spec page that says "sparsity support: yes" next to its TOPS number is telling you to ask which figure you're looking at.

> [!KEY]
> Peak TOPS is a ceiling derived from a datasheet, not a floor observed in a test. It tells you the arithmetic the block could do; it says nothing about how much of that arithmetic any real model manages to use, or how fast the memory can feed it.

If you've read our piece on [why the same phone chip scores differently in two handsets](/phones/same-chip-different-benchmark-scores/), the shape of the problem will be familiar: a headline number quoted without the condition that produces it, and the condition is where the information lives.

## What does each vendor's spec page actually say?

All four spec pages were read on 7 September 2026. Here is everything each one commits to in writing about NPU throughput.

| Chip | NPU figure, as published | Precision stated? | Sparsity mentioned? | Where it says so |
| --- | --- | --- | --- | --- |
| Intel Core Ultra 7 258V | NPU Peak TOPS (Int8): 47 | Yes, Int8 | Yes: "Sparsity Support: Yes" | Intel ARK, NPU Specifications |
| AMD Ryzen AI 9 HX 370 | NPU TOPS: up to 50 | No | No | AMD product page, AI Engine Capabilities |
| Qualcomm Snapdragon X Elite (all four SKUs) | 45 TOPS | No | No | Product brief 87-71417-1 Rev F; platform page |
| Qualcomm Snapdragon X2 Elite | 80 or 85 TOPS by part number | No | No | Qualcomm Snapdragon X comparison table |
| Apple M4 | 38 trillion operations per second | No | No | Apple Newsroom, 7 May 2024 |

Intel is the outlier, and in the useful direction. Its ARK entry for the 258V labels every AI figure with a data type and gives three of them: NPU Peak TOPS (Int8) 47, GPU Peak TOPS (Int8) 64, and an "Overall Peak TOPS (Int8)" of 115 that adds the CPU as well. It also lists "Sparsity Support: Yes" on the line below the NPU number, which is a hint that the 47 may be the sparse figure. Intel doesn't say either way. The sibling Core Ultra 7 266V's ARK page lists 48 for the same NPU block, so the figure does move with clock speed, exactly as the formula predicts.

AMD's page for the Ryzen AI 9 HX 370 has two lines under "AI Engine Capabilities": NPU TOPS "up to 50", overall TOPS "up to 80". That's it. No data type, no sparsity note, no footnote. AMD's own developer blog on its MLPerf Client runs calls the NPU "over 50 TOPS", a slightly different claim again.

Qualcomm's Snapdragon X Elite product brief, DCN 87-71417-1 Rev F, reads 45 in the "NPU TOPS" column for all four part numbers, with no precision anywhere in the document. The comparison table on the same platform page gives the Snapdragon X2 Elite parts 80 TOPS, except the X2E-90-100 and X2E-84-100, which get 85. Same NPU generation, two peaks, no explanation.

Apple's M4 announcement says the Neural Engine is "capable of up to 38 trillion operations per second" and "60x faster than the first Neural Engine in A11 Bionic". Neither figure carries a data type.

> [!WARNING]
> Three of these four vendors quote a peak without saying what precision it was calculated at. Put their numbers on one chart, as we have in the hero image, and you are comparing figures that may not share a unit. The chart is honest about what was published; it can't be honest about what was meant.

## Does Copilot+ PC certification pin the definition down?

No. Microsoft's Copilot+ PC developer guide on Microsoft Learn, last updated 17 November 2025, says these machines have an NPU that "can perform more than 40 trillion operations per second (TOPS)". That's the requirement in full: a threshold applied to the manufacturer's rated figure, not a workload Microsoft runs on each device before it earns the badge.

The same document does admit the underlying issue. Its section on model formats says many NPUs "only support integer math in lower bit format, such as INT8", which is why models trained in FP32 have to be quantised before the NPU will run them. Microsoft is telling developers INT8 is the common denominator. It just never requires anyone to quote their TOPS at it.

So a Copilot+ sticker tells you that somebody's calculation exceeded 40. It doesn't tell you whose arithmetic, or that the chip has ever been observed doing anything at that rate.

## What happens when a standard benchmark runs on the same silicon?

For a year after the first Copilot+ PCs shipped, there was no vendor-neutral way to answer that. UL's Procyon AI Computer Vision test existed, and PCWorld ran it across the first wave of chips in September 2024, finding Lunar Lake and the Snapdragon X Elite "pretty evenly matched", Intel ahead on mains power and Qualcomm ahead on battery. But Procyon produces a unitless score, the vendor picks the precision, and PCWorld's generative-image variant, as they note, uses an INT8 model and didn't run on Arm at all.

The standard test arrived in April 2025, when MLCommons released MLPerf Client v0.6 with NPU support for the first time. Its release notes call it "the first open benchmark to span both GPU and NPU acceleration on consumer platforms" and list the working group as AMD, Intel, Microsoft, Nvidia and Qualcomm. The workload was Llama 2 7B. The metrics were two plain numbers: time to first token, in seconds, and tokens per second after that.

Only one NPU passed. Intel's newsroom post of 5 May 2025 says its Core Ultra Series 2 was the only NPU to achieve full compliance, and publishes its own measurement: a first token in 1.09 seconds and 18.55 tokens per second. The small print gives the machine (an Asus Zenbook S 14 with a Core Ultra 9 288V and 32 GB of LPDDR5X-8533), the date (28 April 2025) and the conditions (mains power, Balanced plan, Best Performance mode). That is what a properly conditioned figure looks like. It also came from a vendor, not a lab.

> [!NOTE]
> 18.55 tokens per second is a good result. By MLCommons' rule of thumb of 100 tokens to 75 English words, that's about 14 words a second, faster than most people read. The NPU isn't slow. The number you can feel just bears no visible relation to the number on the box.

Why doesn't a peak rating in the high forties translate into something bigger? Because generating a token isn't arithmetic-bound. Every token requires the model's weights to be read through once. MLCommons quantises the MLPerf Client language models to 4-bit integers, so a 7-billion-parameter model is about 3.5 GB of weights, and 18.55 tokens a second means streaming that 3.5 GB roughly 18 times a second, around 65 GB/s of sustained memory traffic. Qualcomm's X Elite brief rates that class of chip's memory at 135 GB/s. The token rate is set by how fast memory can deliver weights, and no TOPS figure includes memory at all. It's the same reason [a context window is really a memory budget](/ai/context-window-explained/), and why AMD's own MLPerf Client v1.0 write-up, published August 2025, credits the Ryzen AI Max+ 395's 61 tokens per second on Phi-3.5 to "its powerful GPU and memory bandwidth" rather than to its NPU.

## So what is a TOPS number good for?

Mainly for telling you which tier of silicon you're buying, and for one specific job: the prefill phase, when the model reads your prompt before answering. That part really is arithmetic-heavy, which is why AMD's hybrid execution path puts the NPU on prefill and the GPU on generation, and why the NPU's strongest MLPerf metric is time to first token rather than tokens per second.

Beyond that, treat it the way you'd treat a horsepower figure quoted without a dyno chart.

> [!ACTION]
> Before you let a TOPS number sway a purchase:
> - Find the precision. If the spec page doesn't say Int8, FP16 or similar next to the figure, you don't know what it is.
> - Look for a sparsity line. If it says "supported", ask whether the headline is the dense or the sparse figure.
> - Check the part number. Qualcomm publishes 80 and 85 TOPS for chips in the same family; the box may not say which you have.
> - Ask for a token rate. MLPerf Client publishes tokens per second and time to first token with the configuration attached.
> - Remember the memory. Bandwidth in GB/s predicts generation speed better than TOPS does, and it's usually on the same spec page.

> [!TIP]
> One sanity check: take the model size in gigabytes at the precision you'll run, divide the memory bandwidth by it, and you have a hard upper bound on tokens per second. No NPU rating can beat that number.

Intel tells you what its number means, AMD and Qualcomm tell you the number, and Apple tells you a number and a multiple. Until the other three write the data type next to the figure, two vendors' TOPS ratings share a unit only by assumption. For a comparison you can defend, wait for MLPerf Client results on the specific machine, with the "configuration tested by MLCommons" notice attached, and compare seconds and tokens instead.

Specifications current as of 7 September 2026, read from Intel ARK, AMD's and Qualcomm's product pages (brief DCN 87-71417-1 Rev F), Apple's 7 May 2024 press release, Microsoft Learn (updated 17 November 2025), Intel's 5 May 2025 newsroom post and MLCommons' MLPerf Client documentation. SpecWire has not tested any of these processors; every measured value above is attributed to the organisation that published it.
