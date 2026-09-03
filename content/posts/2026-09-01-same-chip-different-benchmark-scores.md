---
title: "Two phones, the same Snapdragon 8 Elite, and a 40% gap in the same benchmark"
slug: same-chip-different-benchmark-scores
seo_title: "Same Chip, Two Phones, Two Scores"
meta: "Same chip name, different benchmark scores? Qualcomm ships the Snapdragon 8 Elite in two core counts and two clock speeds — and that's before cooling."
category: phones
date: 2026-09-01
updated: 2026-09-01
description: "A chip name is a marketing label, not a configuration. Qualcomm's own product briefs describe two different Snapdragon 8 Elites, and the cooling around them does the rest."
image_alt: "Typographic cover reading: the same Snapdragon 8 Elite spans a 40 percent single-core benchmark range across 30 tested devices"
tags: [Snapdragon 8 Elite, Geekbench, benchmarks, thermal throttling, Qualcomm, SoC binning, 3DMark, smartphone performance]
about: ["Qualcomm", "Snapdragon 8 Elite", "Geekbench", "Primate Labs", "Notebookcheck", "OnePlus", "Asus ROG Phone"]
hero: photo
key_takeaways:
  - text: "Qualcomm's own product brief 87-83196-1 Rev D lists the Snapdragon 8 Elite peaking at **4.47 GHz**, then footnotes that the platform is also sold in a **4.32 GHz** CPU version."
    source: 1
  - text: "A second Qualcomm brief, 87-86431-1 Rev B, describes part number SM8750-3-AB as **2 prime cores** at 4.32 GHz plus **5 performance cores** at 3.53 GHz — that is **7 cores**, not 8, under the same retail name."
    source: [2, 3]
  - text: "Across the **30** Snapdragon 8 Elite devices in Notebookcheck's own benchmark database, Geekbench 6.7 single-core results run from **2,309 to 3,228** points — a spread of about **40%** on one chip name."
    source: 5
  - text: "Multi-core spreads almost as far. Notebookcheck's same **30** Snapdragon 8 Elite entries range from **7,656 to 10,401** points against an average of **9,143**."
    source: 5
  - text: "Geekbench is built to suppress this. Primate Labs' own documentation says Geekbench 6.1 and later insert a **5-second** gap between workloads to reduce the effect of thermals on the score."
    source: 4
  - text: "Under sustained load the gap widens. Notebookcheck measured the OnePlus 13 at roughly **46 °C** and recorded a drop in system performance of around **50%** through the 3DMark Wild Life stress test."
    source: 6
faq:
  - q: "Why do two phones with the same chip get different benchmark scores?"
    a: "Three reasons stack up. Qualcomm sells more than one hardware configuration under a single chip name — different peak clocks and, for the Snapdragon 8 Elite, different core counts. Each manufacturer then sets its own power and temperature limits in firmware. And the phone's physical cooling decides how long the chip can hold its peak before the limits bite. A short benchmark mostly measures the first two; a long one measures all three."
  - q: "Is my phone's chip a slower version of the one in the reviews?"
    a: "Possibly, and the only way to know is the manufacturer's spec page rather than the chip name. Qualcomm's Snapdragon 8 Elite page states plainly that maximum CPU speed varies by platform version and tells readers to consult OEM specifications for device CPU speed. If your phone maker publishes a clock speed and a core count, that is the number that applies to you."
  - q: "Does a higher Geekbench score mean the phone is faster in real use?"
    a: "For short bursts, mostly yes — opening apps, loading pages, applying a photo filter. For anything sustained, it tells you much less. Primate Labs designs Geekbench 6 to pause between workloads specifically so that heat build-up doesn't distort the result, which means the score describes a chip that has been kept comfortable. Gaming, video export and long camera sessions do not keep a chip comfortable."
  - q: "What does the '50% drop' in a stress test actually measure?"
    a: "It's the difference between the best and worst loops of a repeated graphics benchmark run back to back for around twenty minutes. Notebookcheck ran 3DMark Wild Life on the OnePlus 13 and reported system performance falling by roughly half over the run, at a measured surface temperature of about 46 °C. That is the phone protecting itself, not the chip failing."
  - q: "Should I buy the phone with the higher benchmark score?"
    a: "Only if you know which score you're reading. A single-core number tells you about snappiness, a multi-core number about heavy short tasks, and a stress-test stability figure about whether the phone can still do either after twenty minutes. A gaming phone with a vapour chamber and a thin flagship can post near-identical launch-day numbers and behave completely differently an hour later."
  - q: "Do RAM and storage explain some of the gap too?"
    a: "They contribute. Qualcomm's briefs specify support for LPDDR5X up to 5,300 MHz, up to 24 GB, and UFS 4.0 storage — but those are ceilings, not guarantees, and manufacturers buy to a price. Notebookcheck's Asus ROG Phone 9 Pro review unit carried 24 GB of LPDDR5X; plenty of phones with the same chip ship with a third of that. Storage speed in particular moves benchmark suites that touch the filesystem."
products:
  - name: "Snapdragon 8 Elite Mobile Platform"
    url: "https://www.qualcomm.com/smartphones/products/8-series/snapdragon-8-elite-mobile-platform"
    cta: "Qualcomm platform page"
    note: "The specification table and the footnotes about clock speed and core count, straight from Qualcomm"
resources:
  - title: "Snapdragon 8 Elite Mobile Platform Product Brief (87-83196-1 Rev D)"
    url: "https://docs.qualcomm.com/doc/87-83196-1/87-83196-1_REV_D_Snapdragon_8_Elite_Mobile_Platform_Product_Brief.pdf"
    note: "Two pages, and the footnote on page one is the whole story"
  - title: "Snapdragon 8 Elite (SM8750-3-AB) Product Brief"
    url: "https://www.qualcomm.com/content/dam/qcomm-martech/dm-assets/documents/Snapdragon-8-Elite-SM8750-3-AB-Product-Brief.pdf"
    note: "The seven-core variant, with its core counts spelled out"
  - title: "Geekbench 6 Benchmark Internals"
    url: "https://www.geekbench.com/doc/geekbench6-benchmark-internals.pdf"
    note: "What the score is calibrated against, and why there's a gap between workloads"
  - title: "Geekbench 6 CPU Workloads"
    url: "https://www.geekbench.com/doc/geekbench6-cpu-workloads.pdf"
    note: "The sixteen tasks the number is actually an average of"
  - title: "Qualcomm document library for the Snapdragon 8 Elite"
    url: "https://docs.qualcomm.com/list?query=&product=1601111740063415"
    note: "Every published brief for this platform, with revision letters"
sources:
  - title: "Snapdragon 8 Elite Mobile Platform Product Brief, document 87-83196-1 Rev D"
    url: "https://docs.qualcomm.com/doc/87-83196-1/87-83196-1_REV_D_Snapdragon_8_Elite_Mobile_Platform_Product_Brief.pdf"
    publisher: "Qualcomm Technologies"
    accessed: 2026-09-01
    primary: true
  - title: "Snapdragon 8 Elite SM8750-3-AB Product Brief, document 87-86431-1 Rev B"
    url: "https://www.qualcomm.com/content/dam/qcomm-martech/dm-assets/documents/Snapdragon-8-Elite-SM8750-3-AB-Product-Brief.pdf"
    publisher: "Qualcomm Technologies"
    accessed: 2026-09-01
    primary: true
  - title: "Snapdragon 8 Elite Mobile Platform — specifications and footnotes"
    url: "https://www.qualcomm.com/smartphones/products/8-series/snapdragon-8-elite-mobile-platform"
    publisher: "Qualcomm Technologies"
    accessed: 2026-09-01
    primary: true
  - title: "Geekbench 6 Benchmark Internals, May 2024 edition"
    url: "https://www.geekbench.com/doc/geekbench6-benchmark-internals.pdf"
    publisher: "Primate Labs"
    accessed: 2026-09-01
    primary: true
  - title: "Asus ROG Phone 9 Pro review — benchmark tables and Snapdragon 8 Elite device range"
    url: "https://www.notebookcheck.net/Asus-ROG-Phone-9-Pro-review-This-smartphone-is-the-first-choice-for-every-gamer.924300.0.html"
    publisher: "Notebookcheck"
    accessed: 2026-09-01
    primary: true
  - title: "Snapdragon 8 Elite with a performance handicap? Verdict on the OnePlus 13"
    url: "https://www.notebookcheck.net/Snapdragon-8-Elite-with-a-performance-handicap-Verdict-on-the-OnePlus-13.934317.0.html"
    publisher: "Notebookcheck"
    accessed: 2026-09-01
    primary: true
---

Because "Snapdragon 8 Elite" is a brand, not a configuration. Qualcomm publishes two product briefs under that one name: document 87-83196-1 Rev D lists a peak of 4.47 GHz, while 87-86431-1 Rev B describes part SM8750-3-AB as two prime cores at 4.32 GHz and five performance cores at 3.53 GHz — seven cores where the headline part has eight. Then each phone maker picks a power limit and a cooling design. Notebookcheck's own database shows the result: across 30 tested Snapdragon 8 Elite devices, Geekbench 6.7 single-core scores run from 2,309 to 3,228 points. Same name, roughly 40% apart.

## Is the Snapdragon 8 Elite even one chip?

No, and Qualcomm doesn't hide it. It just puts the disclosure in a footnote.

The flagship product brief — Qualcomm document 87-83196-1, revision D, covering part numbers SM8750-AB and SM8750-AC — leads with a prime core "up to 4.47 GHz". An asterisk on that same line notes the platform is also available in a 4.32 GHz CPU version, and that maximum CPU speed varies by platform version. The Snapdragon 8 Elite product page on qualcomm.com carries a second footnote confirming a seven-core CPU version exists. Both tell you to consult OEM specifications for the actual device speed.

The seven-core part gets its own document. Qualcomm brief 87-86431-1 revision B covers SM8750-3-AB and spells the configuration out: 2 prime cores up to 4.32 GHz, 5 performance cores up to 3.53 GHz.

| | Doc 87-83196-1 Rev D | Doc 87-86431-1 Rev B |
| --- | --- | --- |
| Part number | SM8750-AB, SM8750-AC | SM8750-3-AB |
| Prime core peak | up to 4.47 GHz* | up to 4.32 GHz |
| Performance cores | up to 3.53 GHz | 5 cores, up to 3.53 GHz |
| Stated core count | not stated in the brief | 2 + 5 = 7 |
| Memory | LPDDR5X to 5,300 MHz, to 24 GB | LPDDR5X to 5,300 MHz |
| Storage | UFS 4.0 | UFS 4.0 |
| Process | 3 nm | 3 nm |

\* Qualcomm's own footnote: also available in a 4.32 GHz CPU version.

Both documents are two-page marketing briefs, which is worth saying out loud. They're the most detailed public specification Qualcomm publishes for these parts, and neither one gives you cache sizes, sustained power limits or GPU clocks. The retail box gives you even less.

> [!KEY] The name is not the number
> One retail name, two published product briefs, two peak clocks and two core counts. Before cooling enters the picture at all, "Snapdragon 8 Elite" already describes at least two different processors.

## Why does Geekbench make every phone look similar?

Because it's designed to. This is the part almost nobody checks, and it's written plainly in Primate Labs' own documentation.

Geekbench 6 runs sixteen CPU workloads — file compression, PDF rendering, ray tracing, a few machine-learning tasks — and deliberately inserts a pause between each one. The stated reason, in the May 2024 edition of *Geekbench 6 Benchmark Internals*, is to minimise the effect thermal issues have on workload performance; without the gap, later workloads would score lower than earlier ones. In Geekbench 6.0 that gap was 2 seconds. From 6.1 onward it's 5 seconds.

So a Geekbench score is a burst measurement, taken from a chip that has been given time to cool between tasks. That's a legitimate design choice — it's measuring the processor rather than the chassis — but it means the number describes the best twenty seconds of your phone's life, not the twentieth minute.

Two more details from the same document change how you should read the score. The composite is a weighted mean, 65% integer and 35% floating point, so a chip that's strong at one and weak at the other gets averaged into the middle. And the whole scale is calibrated against a baseline of 2,500, which is a Dell Precision 3460 with a Core i7-12700. Double the score means double the performance on those workloads, which is a much narrower claim than "twice as fast".

> [!NOTE] A number without its condition isn't a fact
> This is the same trap as display brightness, where a peak nits figure is meaningless until you know the test patch. We unpack that one in [what nits, cd/m² and lumens actually measure](/explainers/nits-cd-m2-lumens-explained/). A benchmark score has a condition too: ambient temperature, cooling gaps, battery level and whether the phone had just been charging.

## How wide is the spread on one chip name?

Wide enough that the chip name is close to useless for predicting a score.

Notebookcheck maintains its own measured database and prints the range alongside every result. In its Asus ROG Phone 9 Pro review, the Snapdragon 8 Elite reference line covers 30 devices the lab has tested with that chip:

| Geekbench 6.7 | Lowest of 30 | Average of 30 | Highest of 30 | Spread |
| --- | --- | --- | --- | --- |
| Single-core | 2,309 | 3,046 | 3,228 | ~40% |
| Multi-core | 7,656 | 9,143 | 10,401 | ~36% |

*Range and averages measured and published by Notebookcheck across 30 Snapdragon 8 Elite devices.*

The ROG Phone 9 Pro itself landed at 3,215 single-core and 10,323 multi-core — near the top of both ranges. Notebookcheck's review notes the unit ran a 4.32 GHz top clock with 24 GB of LPDDR5X, which is a useful reminder that the headline 4.47 GHz figure isn't what most flagships actually shipped.

A 40% single-core gap is not measurement noise. On a benchmark explicitly engineered to neutralise thermal differences, that spread is silicon configuration and firmware policy showing through.

> [!WARNING] Beware the launch-day chart
> Chip announcement slides quote the fastest bin, tested on a reference design with cooling no retail phone has. Qualcomm's brief claims a 45% CPU performance gain over the Snapdragon 8 Gen 3, and immediately adds that results vary depending on OEM implementation. That sentence is doing an enormous amount of work.

## What happens when the benchmark stops being polite?

The gap stops being 40% and starts being catastrophic.

3DMark's Wild Life stress test does the opposite of Geekbench: it loops the same graphics scene back to back and reports how much performance survives. Notebookcheck ran it on the OnePlus 13 and measured around 46 °C on the body under load, with system performance dropping roughly 50% over the run. The lab's verdict noted the phone was at times falling below its predecessor, the OnePlus 12, despite the newer and nominally much faster chip.

Nothing was broken. A phone that hits its thermal ceiling reduces clocks until it stops heating up, which is exactly what you want it to do — the alternative is a hot device and a cooked battery. But it means the chip in a 9 mm glass slab and the chip in a gaming phone with a vapour chamber converge on very different steady-state performance, no matter how close their launch-day scores were.

This is the same physics we covered in [why a 16-core laptop CPU loses to an 8-core desktop](/computers/laptop-cores-vs-desktop-cores/). Cores and clocks describe what a processor could do. The thermal budget of the box around it decides what it will do, and phones have the smallest budget of anything you own.

> [!TIP] Read stability, not the peak
> When a review publishes a stress-test result, the useful number is the stability percentage — the worst loop divided by the best. A phone at 95% stability with a slightly lower peak will feel faster in a long gaming session than one at 55% stability with a higher opening score.

## What should you actually check before buying?

Skip the chip name. It's the least informative line on the spec sheet.

> [!ACTION] Four things worth two minutes each
> - Find the manufacturer's own spec page and look for a published CPU clock and core count. Qualcomm tells you to do this; take the hint.
> - Check whether the RAM is LPDDR5X and how much of it there is. The brief's 24 GB ceiling is a ceiling, not a promise.
> - Look for a stress-test stability figure in a review from a lab that publishes its own measurements, not a summary of someone else's.
> - Note the ambient temperature the review mentions, if any. A benchmark run in a 30 °C room is a different test from one run in a 20 °C room.

None of this makes benchmark scores worthless. A 2,309 and a 3,228 on the same test really are different, and the phone posting 3,228 really is quicker at the things Geekbench measures. The mistake is reading the chip name and assuming you know which one you're getting — Qualcomm has published two product briefs and two footnotes telling you that you don't.

Worth noting that this spread is larger than the gap between vendors. Set Qualcomm's platform against Apple's and the two chips land within about ten percent of each other, which is why [comparing a Snapdragon 8 Elite with an A-series chip turns into an argument about disclosure](/phones/snapdragon-8-elite-vs-apple-a-series/) rather than performance.

*Specifications current as of 1 September 2026, verified against Qualcomm product briefs 87-83196-1 Rev D and 87-86431-1 Rev B, the Qualcomm Snapdragon 8 Elite platform page, and Primate Labs' Geekbench 6 Benchmark Internals (May 2024). Benchmark ranges and stress-test figures were measured and published by Notebookcheck; SpecWire does not test hardware.*
