---
title: "Why a 16-core laptop CPU loses to an 8-core desktop"
slug: laptop-cores-vs-desktop-cores
seo_title: "16-Core Laptop vs 8-Core Desktop"
meta: "Intel's Core Ultra 9 285H has 16 cores. AMD's Ryzen 7 9700X has 8. Notebookcheck measured the desktop 21% faster. Here is what the core count hides."
category: computers
date: 2026-08-27
updated: 2026-08-27
description: "Core count is the most quoted number on a laptop spec sheet and one of the least informative. Two chips, sixteen cores against eight, and the eight wins."
image_alt: "Illustration for an article comparing laptop and desktop processor core counts and sustained power limits"
tags: [core count, Core Ultra 9 285H, Ryzen 7 9700X, TDP, Processor Base Power, sustained performance, Cinebench, laptop CPU]
about: ["Intel", "AMD", "Core Ultra 9 285H", "Ryzen 7 9700X", "Arrow Lake", "Zen 5", "Notebookcheck"]
hero: photo
key_takeaways:
  - text: "Intel's ARK page for the Core Ultra 9 285H lists **16 total cores** but only **6 performance-cores**, plus 8 efficient-cores and 2 low-power efficient-cores — three different core types with three different clock ceilings."
    source: 1
  - text: "The Core Ultra 9 285H has **16 cores and 16 threads**, because Intel lists Hyper-Threading as unsupported. AMD's 8-core Ryzen 7 9700X also has **16 threads**, because it supports SMT. Half the cores, identical thread count."
    source: [1, 2]
  - text: "Notebookcheck measured the same Core Ultra 9 285H at **991 points** in Cinebench 2024 multi-core in an MSI Prestige 16 AI Evo and **740 points** in an Asus ZenBook Duo — a **34%** spread from the chassis alone, with no change of silicon."
    source: 3
  - text: "Notebookcheck measured the 8-core Ryzen 7 9700X at **1,203 points** in the same Cinebench 2024 multi-core test, making the desktop part about **21%** faster than the best 16-core laptop result and **63%** faster than the thin-and-light one."
    source: [3, 4]
  - text: "Intel's own ARK entry gives the 285H a Processor Base Power of **45 W**, a Maximum Turbo Power of **115 W** and a Minimum Assured Power of **35 W** — a **3.3x** power range that the laptop maker, not Intel, decides."
    source: 1
  - text: "Intel states that from **12th Generation** onward the term TDP is replaced by Processor Base Power, and that its purpose is to give system integrators a target for thermal solution selection — it is a design instruction, not a performance rating."
    source: 5
faq:
  - q: "Does more cores always mean faster?"
    a: "No, and core count is one of the weakest predictors of finished performance in a laptop. A core only contributes work if it is given power and if the workload can use it. Intel's Core Ultra 9 285H carries 16 cores, but only 6 of them are performance-cores, and Notebookcheck measured the same chip 34% apart in two different laptops purely because of how much sustained power each chassis allowed. An 8-core desktop part that can hold its power indefinitely beats it."
  - q: "Why does the 285H have 16 cores but only 16 threads?"
    a: "Intel's ARK page lists Hyper-Threading Technology as not supported on the Core Ultra 9 285H, so each of its 16 cores runs one thread. AMD's Ryzen 7 9700X supports SMT, so its 8 cores run 16 threads. For any workload that scales with threads rather than cores, the two chips present the operating system with the same number of execution contexts, and the desktop part fills each of those contexts with a full-size core."
  - q: "What is the difference between a P-core and an E-core?"
    a: "They are physically different designs sharing one die. On the Core Ultra 9 285H, Intel lists the performance-cores at up to 5.4 GHz, the efficient-cores at up to 4.5 GHz, and the two low-power efficient-cores at up to 2.5 GHz. E-cores are smaller and cheaper in area and power, which is why a chip can carry a lot of them, and they exist to absorb background and parallel work rather than to match a P-core one for one. Counting them together as sixteen equal cores is where the spec sheet stops being useful."
  - q: "Is TDP the same as power consumption?"
    a: "Not quite. Intel's support documentation says TDP refers to power consumption under maximum theoretical load and exists so that system designers can pick an adequate thermal solution. From 12th Generation onward Intel renamed it Processor Base Power. It describes what the cooling has to handle at the base operating point, not what the chip draws at any given moment, and Intel publishes a separate Maximum Turbo Power figure for the short bursts above it."
  - q: "Should I ignore core count entirely when buying a laptop?"
    a: "Not entirely, but treat it as a ceiling rather than a promise. Core count tells you the maximum parallelism the silicon can offer. Sustained power and cooling tell you how much of that you actually get, and those are properties of the laptop, not the chip. The useful move is to look up a review of your exact model rather than the processor, because two machines with identical CPU names can differ by more than a third in a long multi-core run."
  - q: "Do these numbers apply to gaming or just rendering?"
    a: "The gap is widest in long, all-core workloads like rendering, compiling and video encode, which is what Cinebench 2024 multi-core measures. Games usually lean on a handful of threads and on the GPU, so the picture is different and much more title-dependent. Notebookcheck measured Cinebench 2024 single-core at 127 points on the 285H and 136 points on the Ryzen 7 9700X — about 7% apart, which is a far smaller gap than the multi-core one."
products:
  - name: "Intel Core Ultra 9 processor 285H"
    url: "https://www.intel.com/content/www/us/en/products/sku/241747/intel-core-ultra-9-processor-285h-24m-cache-up-to-5-40-ghz/specifications.html"
    cta: "Intel ARK page"
    note: "The full spec table including base, turbo and minimum assured power — check our transcription against it"
  - name: "AMD Ryzen 7 9700X"
    url: "https://www.amd.com/en/products/processors/desktops/ryzen/9000-series/amd-ryzen-7-9700x.html"
    cta: "AMD official page"
    note: "AMD's own specification list, including the 65 W default TDP and 95 °C maximum operating temperature"
resources:
  - title: "Intel ARK — Core Ultra 9 processor 285H specifications"
    url: "https://www.intel.com/content/www/us/en/products/sku/241747/intel-core-ultra-9-processor-285h-24m-cache-up-to-5-40-ghz/specifications.html"
    note: "Read the three separate core-count lines and the three separate power lines. They are the whole story."
  - title: "Intel support — Thermal Design Power (TDP) in Intel processors"
    url: "https://www.intel.com/content/www/us/en/support/articles/000055611/processors.html"
    note: "Intel's own FAQ explaining that TDP became Processor Base Power and what it is for"
  - title: "AMD — Ryzen 7 9700X product specifications"
    url: "https://www.amd.com/en/products/processors/desktops/ryzen/9000-series/amd-ryzen-7-9700x.html"
    note: "Eight identical Zen 5 cores, SMT enabled, 65 W default TDP"
  - title: "Notebookcheck — Intel Arrow Lake-H CPU analysis"
    url: "https://www.notebookcheck.net/Intel-Arrow-Lake-H-CPU-analysis-Core-Ultra-200H-makes-Lunar-Lake-almost-redundant.959328.0.html"
    note: "The same 285H measured in two laptops, with the sustained wattage each one settled at"
  - title: "Notebookcheck — Ryzen 7 9700X benchmarks and specifications"
    url: "https://www.notebookcheck.net/AMD-Ryzen-7-9700X-Processor-Benchmarks-and-Specs.862076.0.html"
    note: "Their measured Cinebench 2024 scores for the desktop part, in the same test suite"
sources:
  - title: "Intel Core Ultra 9 Processor 285H (24M Cache, up to 5.40 GHz) — Product Specifications"
    url: "https://www.intel.com/content/www/us/en/products/sku/241747/intel-core-ultra-9-processor-285h-24m-cache-up-to-5-40-ghz/specifications.html"
    publisher: "Intel"
    accessed: 2026-08-27
    primary: true
  - title: "AMD Ryzen 7 9700X — product specifications"
    url: "https://www.amd.com/en/products/processors/desktops/ryzen/9000-series/amd-ryzen-7-9700x.html"
    publisher: "AMD"
    accessed: 2026-08-27
    primary: true
  - title: "Intel Arrow Lake-H CPU analysis: Core Ultra 200H makes Lunar Lake almost redundant"
    url: "https://www.notebookcheck.net/Intel-Arrow-Lake-H-CPU-analysis-Core-Ultra-200H-makes-Lunar-Lake-almost-redundant.959328.0.html"
    publisher: "Notebookcheck"
    accessed: 2026-08-27
    primary: true
  - title: "AMD Ryzen 7 9700X Processor — Benchmarks and Specs"
    url: "https://www.notebookcheck.net/AMD-Ryzen-7-9700X-Processor-Benchmarks-and-Specs.862076.0.html"
    publisher: "Notebookcheck"
    accessed: 2026-08-27
    primary: true
  - title: "Thermal Design Power (TDP) in Intel Processors — support article 000055611"
    url: "https://www.intel.com/content/www/us/en/support/articles/000055611/processors.html"
    publisher: "Intel"
    accessed: 2026-08-27
    primary: true
---

Intel's Core Ultra 9 285H is a 16-core laptop chip. AMD's Ryzen 7 9700X is an 8-core desktop chip. Notebookcheck measured the 8-core desktop at 1,203 points in Cinebench 2024 multi-core, against 991 points for the best-cooled 285H laptop in its test set. The desktop is roughly 21% faster with half the cores.

Two things explain it, and neither is a mystery once you read the spec sheets properly. Only 6 of the laptop's 16 cores are performance-cores, and because Intel lists Hyper-Threading as unsupported on this part, all 16 cores produce exactly 16 threads — the same thread count the 8-core desktop chip delivers via SMT. Then the laptop's sustained power collapses under load, and a core you cannot feed does not compute.

## What is Intel actually counting when it says 16 cores?

Three different things, stacked into one number.

Intel's ARK entry for the Core Ultra 9 285H, which we read on 27 August 2026, breaks the 16 into 6 performance-cores, 8 efficient-cores and 2 low-power efficient-cores. Those three groups do not run at the same speed and were never designed to. Intel lists the P-cores at up to 5.4 GHz, the E-cores at up to 4.5 GHz, and the low-power E-cores at up to 2.5 GHz. The base frequencies fan out even harder: 2.9 GHz, 2.7 GHz, and 1.0 GHz respectively.

So "16 cores" is a sum across three tiers of silicon with a 2.2x spread in maximum clock between the fastest and slowest. AMD's Ryzen 7 9700X, by contrast, has 8 Zen 5 cores that are all the same core, all the way up to a 5.5 GHz boost.

| | Intel Core Ultra 9 285H | AMD Ryzen 7 9700X |
| --- | --- | --- |
| Segment | Mobile (BGA, soldered) | Desktop (socket AM5) |
| Cores | 16 (6 P + 8 E + 2 LP E) | 8 (all Zen 5) |
| Threads | 16 | 16 |
| Max boost | 5.4 GHz (P-core) | 5.5 GHz |
| Slowest core ceiling | 2.5 GHz (LP E-core) | 5.5 GHz |
| Manufacturer power figure | 45 W base / 115 W turbo / 35 W minimum assured | 65 W default TDP |
| Max operating temperature | 110 °C | 95 °C |
| Process | TSMC N3B | TSMC 4 nm (CPU dies) |

> [!KEY] The thread count is the tell
> Intel's ARK page lists Intel Hyper-Threading Technology as **No** for the 285H, giving 16 cores and 16 threads. AMD lists SMT as supported on the 9700X, giving 8 cores and 16 threads. Two chips, one thread count, and the desktop fills every one of those threads with a full-size core.

That comparison is not meant to declare a winner between Intel and AMD. It is meant to show that the number buyers compare most often is the one that survives translation the worst.

## Why does the same chip score 34% apart in two laptops?

Because the laptop, not the processor, sets the power limit.

Notebookcheck tested the Core Ultra 9 285H in two machines for its Arrow Lake-H analysis. In the MSI Prestige 16 AI Evo, it recorded an initial spike to 115 W settling to 45 W, and the chip scored 991 points in Cinebench 2024 multi-core. In the Asus ZenBook Duo, the same processor peaked at 60 W and stabilised at just 24 W, scoring 740 points. Same part number, same stepping, same firmware generation. A 34% performance gap decided entirely by chassis, fan and vendor power policy.

| Cinebench 2024, multi-core (measured by Notebookcheck) | Score | Sustained power |
| --- | --- | --- |
| AMD Ryzen 7 9700X, desktop test system | 1,203 | 65 W default TDP, per AMD |
| Core Ultra 9 285H, MSI Prestige 16 AI Evo | 991 | settles at 45 W |
| Core Ultra 9 285H, Asus ZenBook Duo | 740 | settles at 24 W |

SpecWire has not tested any of these machines. Every figure above is Notebookcheck's own measurement, read from its published results on 27 August 2026.

> [!WARNING] The CPU name on the sticker is not a performance spec
> If you buy a laptop on the strength of "Core Ultra 9, 16 cores", you have chosen a range, not a result. In Notebookcheck's numbers that range ran from 740 to 991 points. Nothing on the box distinguishes the two.

## What does a TDP number actually promise?

Not what most people assume, and Intel says so in its own documentation.

Intel's support article 000055611 states that from the 12th Generation onward the term TDP is replaced by *Processor Base Power*, and that the purpose of defining it is "to provide system designers/integrators with a power target in order to help with proper thermal solution selection." It is an instruction to whoever builds the laptop. It is not a promise to whoever buys it.

Look at what Intel publishes for this one part number: Processor Base Power 45 W, Maximum Turbo Power 115 W, Minimum Assured Power 35 W. That last field is the one nobody reads and the one that matters most. Intel is telling laptop makers they may configure this chip anywhere from 35 W to 115 W and still call it a Core Ultra 9 285H. That is a 3.3x range, and the customer never sees which end of it they bought.

AMD's approach on the desktop side is simpler for the same reason the physics is simpler. AMD lists a Default TDP of 65 W for the 9700X and a maximum operating temperature of 95 °C, and because the part drops into an AM5 socket with a cooler of the buyer's choosing, there is no third party silently reconfiguring it downward to fit a 14 mm chassis.

> [!NOTE] Where the two numbers come from
> Intel's 110 °C maximum operating temperature for the 285H is higher than AMD's 95 °C for the 9700X, which sounds like an advantage and is not. A mobile chip is allowed to run hotter because the alternative is running slower. A desktop chip has room for a heatsink the size of a fist.

This is the same failure mode as a badge that gets quoted without its test condition. It is why [two phones can both be IP68 and be rated for depths four times apart](/phones/ip68-rating-explained/), why [an HDMI 2.1 port is allowed to carry a fraction of the bandwidth the number implies](/explainers/4k-144hz-hdmi-cable/), why [a headline of 990 kbps LDAC often arrives as 330](/audio/does-ldac-actually-sound-better-than-aac/), why [a 120W charging rating survives for a few minutes of the charge](/phones/120w-fast-charging-minute-by-minute/), and why [a USB4 port is allowed to run at a quarter of the 80 Gbps its own specification permits](/computers/thunderbolt-5-vs-usb4-v2/). The number is real. The condition attached to it is what makes it mean something, and the condition is the part that falls off in a comparison table.

## Is the desktop winning on silicon or on cooling?

Mostly on cooling, and the single-core numbers prove it.

Notebookcheck measured Cinebench 2024 single-core at 127 points for the Core Ultra 9 285H, in both laptops, and 136 points for the Ryzen 7 9700X. That is about a 7% gap. One thread, brief load, and the laptop is nearly competitive because a single core fits comfortably inside even a 24 W budget.

Now run all the threads for ten minutes. The desktop holds its clocks. The laptop spends its first few seconds at 115 W looking excellent in a short benchmark, then drops to whatever the fans and the heatpipes can actually remove, and lives there for the rest of the job. The multi-core gap widens from 7% to 21%, or to 63% if the laptop is a thin one.

Which reframes the buying question. You are not choosing between 16 cores and 8 cores. You are choosing between a machine that can sustain its power indefinitely and one that cannot, and the core count on the sticker tells you nothing about which you are getting.

> [!TIP] Short benchmarks flatter thin laptops
> Any single-run benchmark that finishes in under a minute is measuring the boost window, not the machine. Look for a loop test — the same benchmark repeated until the score stops falling — because that is the number your actual render or compile will live at.

## What should you check before buying?

The processor page is the wrong document. You want the review of your exact model.

> [!ACTION] Five things worth ten minutes before you spend
> 1. **Find the sustained wattage**, not the peak. A published sustained figure of 45 W versus 24 W predicts your multi-core performance far better than the CPU name does.
> 2. **Read the core breakdown**, not the total. Six P-cores plus ten E-cores is a very different machine from ten P-cores, even though both say sixteen.
> 3. **Check the thread count separately.** SMT and Hyper-Threading are per-SKU decisions, and Intel disabled them on this generation of H-series parts.
> 4. **Look for a loop or sustained-load test** in the review, and take the last score in the loop as the real one.
> 5. **Compare against a desktop if the work is long.** If your jobs run for minutes rather than seconds, an 8-core desktop at a lower price may finish first.

None of this makes core count useless. It sets the ceiling, and a 16-core chip in a genuinely well-cooled 16-inch chassis will beat an 8-core one in the same class. What it does not do is survive being lifted out of the spec sheet on its own, which is precisely how it is usually quoted.

The honest version of the laptop spec line would read something like: sixteen cores, six of which are fast, configurable by the manufacturer anywhere between 35 W and 115 W, currently set to whatever we felt like. Nobody is going to print that. But it is what the ARK page says, in public, for anyone who scrolls past the first row.

*Specifications current as of 27 August 2026, verified against Intel ARK product 241747 and Intel support article 000055611 (last reviewed 4 April 2023), and AMD's Ryzen 7 9700X product page. Performance figures are Notebookcheck's own measurements, read 27 August 2026. SpecWire operates no test lab and has benchmarked nothing.*
