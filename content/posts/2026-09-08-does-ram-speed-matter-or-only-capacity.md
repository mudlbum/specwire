---
title: "Does RAM speed matter, or only capacity?"
slug: does-ram-speed-matter-or-only-capacity
seo_title: "RAM speed vs capacity: what the labs measured"
meta: "Capacity first, always: Puget Systems measured 43-45% drops at 16 GB. Above that, faster DDR5 is worth 1-12% depending on the workload. The numbers, sourced."
category: computers
date: 2026-09-08
updated: 2026-09-08
description: "Capacity is a cliff and speed is a slope. Here is what JEDEC's DDR5 standard, Intel's and AMD's own spec pages, and two labs' measurements say about which number to spend on."
image_alt: "Two DDR5 memory modules lying on a desk next to a motherboard"
tags: [DDR5, RAM speed, RAM capacity, JEDEC, XMP, EXPO, CUDIMM, memory latency]
about: ["JEDEC", "DDR5 SDRAM", "Intel Core Ultra 200S", "AMD Ryzen 9000", "Puget Systems", "TechSpot"]
hero: photo
key_takeaways:
  - text: "Capacity is the number that can halve your performance: Puget Systems measured a **45%** lower Lightroom Classic score and a **43%** lower After Effects score at 16 GB versus 64 GB on a Ryzen 9 9950X3D2, published 1 June 2026, while 32 GB versus 64 GB was within 2.5% in every application except Lightroom's AI tools."
    source: 7
  - text: "Speed is worth low single digits in most desktop work: Puget Systems measured about **4%** overall between DDR5-7200 and DDR5-5600 on Intel's Core Ultra 270K Plus and 250K Plus, published 31 March 2026, and about **1%** between 6400 and 5600 on the non-Plus 285K and 265K."
    source: 5
  - text: "In CPU-limited games speed matters more: TechSpot measured up to **12%** more frames in Cyberpunk 2077 at 1080p moving a Ryzen 7 9700X from DDR5-6000 CL30 to DDR5-8000, published 7 April 2025, but the DDR5-8000 kit was only **2%** ahead of DDR5-6000 CL26."
    source: 6
  - text: "The official ceilings are lower than the box suggests: Intel's ARK lists the Core Ultra 9 285K at up to DDR5 **6400** MT/s and the Core Ultra 5 250K Plus at up to **7200** MT/s; AMD's spec page lists the Ryzen 9 9950X at DDR5-**5600** with two modules and DDR5-**3600** with four."
    source: [2, 3, 4]
  - text: "JEDEC's JESD79-5C revision of the DDR5 SDRAM standard, published 17 April 2024, extended the defined timing parameters from **6800** to **8800** MT/s; anything sold above that, and most kits sold above the CPU's listed speed, runs on an XMP or EXPO overclocking profile rather than the standard."
    source: 1
  - text: "Adding capacity can cost you speed: AMD's own spec page for the Ryzen 9 9950X drops the supported memory speed from DDR5-5600 to DDR5-3600 when all **4** slots are populated, a **36%** reduction in rated transfer rate."
    source: 4
faq:
  - q: "Is 32 GB of RAM enough in 2026?"
    a: "For most desktop work, yes. Puget Systems' June 2026 capacity test found no measurable difference between 32 GB and 64 GB in Photoshop, After Effects or Premiere, and a 2.5% gap in Lightroom Classic and DaVinci Resolve. The exception was Lightroom's AI tools, which ran 15% slower at 32 GB. Gaming and office work were not part of that test, but they are lighter on memory than any of those applications."
  - q: "Is 16 GB of RAM enough?"
    a: "For a browser and office software it still works. For anything creative it is now the wrong purchase: Puget Systems measured 16 GB running 45% behind 64 GB in Lightroom Classic, 43% behind in After Effects and 20% behind in Photoshop, with Lightroom exports taking more than twice as long. Once the working set spills out of RAM, the machine is swapping to the SSD, and no CPU or memory speed recovers that."
  - q: "Does faster RAM improve gaming FPS?"
    a: "Sometimes, and only when the CPU is the bottleneck. TechSpot's April 2025 test on a Ryzen 7 9700X found up to 12% more average frames at 1080p in Cyberpunk 2077 going from DDR5-6000 CL30 to DDR5-8000, and a 17% improvement in 1% lows in Marvel Rivals from DDR5-5600 to DDR5-8000. At 4K, where the graphics card sets the pace, the same swaps were worth 5% or less. TechSpot also notes the 9800X3D is not particularly sensitive to memory because of its large cache."
  - q: "What is the difference between MT/s and MHz for RAM?"
    a: "MT/s is megatransfers per second, the number of data transfers on the bus. DDR stands for double data rate, meaning two transfers per clock cycle, so DDR5-6000 runs a 3,000 MHz clock and moves data 6,000 million times a second. Marketing uses the two interchangeably; the standards body JEDEC and both CPU makers quote MT/s. If a listing says 6000 MHz it means 6000 MT/s."
  - q: "Do I need XMP or EXPO enabled?"
    a: "If you bought a kit rated above the CPU's official speed, yes, or it will boot at a JEDEC default such as 4800 or 5600. XMP is Intel's profile format and EXPO is AMD's; both are overclocking profiles stored on the module, and both are outside what JEDEC's JESD79-5C standard guarantees. The CPU makers list the speeds they validate on their spec pages: DDR5-5600 for a Ryzen 9 9950X, 6400 for a Core Ultra 9 285K, 7200 for the Core Ultra 200S Plus parts."
  - q: "Should I buy two modules or four?"
    a: "Two. Both CPU makers reduce the supported speed when all four slots are filled. AMD's spec page for the Ryzen 9 9950X gives DDR5-5600 for two modules and DDR5-3600 for four, and Puget Systems notes that Intel's 200S parts fall to at best 4800 MT/s with more than two DIMMs. If you need more capacity later, replace the pair with a larger pair."
chart:
  type: bar
  title: "Performance lost at 16 GB versus 64 GB, by application (Puget Systems, June 2026)"
  y_label: "Overall score reduction, %"
  source: "Puget Systems, 'When Does RAM Capacity Impact Performance?', 1 June 2026, Ryzen 9 9950X3D2"
  annotate_last: false
  series:
    - label: "Score reduction at 16 GB"
      points: [["Premiere", 7], ["DaVinci Resolve", 9], ["Photoshop", 20], ["After Effects", 43], ["Lightroom Classic", 45]]
products:
  - name: "Intel Core Ultra 9 285K"
    url: "https://www.intel.com/content/www/us/en/products/sku/241060/intel-core-ultra-9-processor-285k-36m-cache-up-to-5-70-ghz/specifications.html"
    cta: "Intel ARK specifications"
    note: "Memory Specifications section: up to DDR5 6400 MT/s, 2 channels, 256 GB"
  - name: "Intel Core Ultra 5 250K Plus"
    url: "https://www.intel.com/content/www/us/en/products/sku/245694/intel-core-ultra-5-processor-250k-plus-30m-cache-up-to-5-30-ghz/specifications.html"
    cta: "Intel ARK specifications"
    note: "The 7200 MT/s figure is on this page, with no rank or slot condition stated"
  - name: "AMD Ryzen 9 9950X"
    url: "https://www.amd.com/en/products/processors/desktops/ryzen/9000-series/amd-ryzen-9-9950x.html"
    cta: "AMD product page"
    note: "Connectivity section lists Max Memory Speed by slot count and rank"
resources:
  - title: "JEDEC press release: JESD79-5C DDR5 SDRAM standard"
    url: "https://www.jedec.org/news/pressreleases/jedec-updates-jesd79-5c-ddr5-sdram-standard-elevating-performance-and-security"
    note: "What the April 2024 revision added, including the 6800 to 8800 MT/s extension"
  - title: "Puget Systems: 7200 vs 5600 Mbps RAM for Core Ultra 200S Plus"
    url: "https://www.pugetsystems.com/labs/articles/7200-vs-5600-mbps-ram-for-core-ultra-200s-plus-processors/"
    note: "Full test setup and per-application charts for the speed comparison"
  - title: "Puget Systems: When Does RAM Capacity Impact Performance?"
    url: "https://www.pugetsystems.com/labs/articles/when-does-ram-capacity-impact-performance/"
    note: "The 16 / 32 / 64 GB comparison, with the bcdedit method explained"
  - title: "TechSpot: Is DDR5-8000 Worth It? The Ryzen AM5 Test"
    url: "https://www.techspot.com/review/2972-ddr5-8000-worth-it/"
    note: "Game-by-game charts at 1080p and 4K, plus the UCLK 1:1 versus 2:1 explanation"
  - title: "AMD Ryzen 9 9950X specifications"
    url: "https://www.amd.com/en/products/processors/desktops/ryzen/9000-series/amd-ryzen-9-9950x.html"
    note: "The clearest example of a spec page that conditions memory speed on slot count"
sources:
  - title: "JEDEC Updates JESD79-5C DDR5 SDRAM Standard: Elevating Performance and Security for Next-Gen Technologies"
    url: "https://www.jedec.org/news/pressreleases/jedec-updates-jesd79-5c-ddr5-sdram-standard-elevating-performance-and-security"
    publisher: "JEDEC Solid State Technology Association"
    accessed: 2026-09-08
    primary: true
  - title: "Intel Core Ultra 9 Processor 285K — Product Specifications"
    url: "https://www.intel.com/content/www/us/en/products/sku/241060/intel-core-ultra-9-processor-285k-36m-cache-up-to-5-70-ghz/specifications.html"
    publisher: "Intel ARK"
    accessed: 2026-09-08
    primary: true
  - title: "Intel Core Ultra 5 Processor 250K Plus — Product Specifications"
    url: "https://www.intel.com/content/www/us/en/products/sku/245694/intel-core-ultra-5-processor-250k-plus-30m-cache-up-to-5-30-ghz/specifications.html"
    publisher: "Intel ARK"
    accessed: 2026-09-08
    primary: true
  - title: "AMD Ryzen 9 9950X — product specifications"
    url: "https://www.amd.com/en/products/processors/desktops/ryzen/9000-series/amd-ryzen-9-9950x.html"
    publisher: "AMD"
    accessed: 2026-09-08
    primary: true
  - title: "7200 vs 5600 Mbps RAM For Core Ultra 200S Plus Processors"
    url: "https://www.pugetsystems.com/labs/articles/7200-vs-5600-mbps-ram-for-core-ultra-200s-plus-processors/"
    publisher: "Puget Systems, 31 March 2026"
    accessed: 2026-09-08
    primary: true
  - title: "Is DDR5-8000 Worth It? The Ryzen AM5 Test"
    url: "https://www.techspot.com/review/2972-ddr5-8000-worth-it/"
    publisher: "TechSpot, 7 April 2025"
    accessed: 2026-09-08
    primary: true
  - title: "When Does RAM Capacity Impact Performance?"
    url: "https://www.pugetsystems.com/labs/articles/when-does-ram-capacity-impact-performance/"
    publisher: "Puget Systems, 1 June 2026"
    accessed: 2026-09-08
    primary: true
---

Capacity first, and it isn't close. Run out of RAM and the machine starts paging to the SSD; Puget Systems measured a Ryzen 9 9950X3D2 losing 45% of its Lightroom Classic score and 43% of its After Effects score at 16 GB versus 64 GB. Have enough, and speed becomes a slope rather than a cliff: the same lab measured about 4% between DDR5-7200 and DDR5-5600 across creative work on Intel's Core Ultra 200S Plus chips, and TechSpot found up to 12% in a CPU-limited game on a Ryzen 7 9700X. So buy the capacity your work needs, then buy the fastest kit your CPU maker actually lists. Here's what each of those numbers means and who measured it.

## What does a RAM speed number actually measure?

DDR5-6000 means 6,000 megatransfers per second, or MT/s: the number of times per second the module can move a word of data across the bus. The "double data rate" in DDR means two transfers per clock cycle, so DDR5-6000 runs a 3,000 MHz clock. Retail listings that say "6000 MHz" are wrong by a factor of two, and nobody fixes it.

The organisation that defines what a DDR5 module is, JEDEC, publishes the standard as JESD79-5. Its current revision, JESD79-5C of 17 April 2024, extended the defined timing parameters from 6800 to 8800 MT/s; the previous version, JEDEC's own press release says, covered full timings only to 6400. Those are the speeds a module is guaranteed to run at without anyone overclocking anything.

Everything faster than the CPU's rated speed runs on a profile instead: Intel's XMP or AMD's EXPO, a table stored on the module that the BIOS applies when you turn it on. That's an overclock with a friendly name, which is why a DDR5-8000 kit boots at a much lower JEDEC speed until you enable it.

> [!KEY]
> Three different numbers get called "RAM speed": the JEDEC standard's ceiling (8800 MT/s as of JESD79-5C), the CPU maker's validated speed (5600 to 7200 MT/s on current desktop parts), and the kit's XMP or EXPO profile (whatever the box says). Only the middle one is a promise from the company whose memory controller has to do the work.

## What speed do the CPU makers actually promise?

Lower than most kits on the shelf. All three spec pages were read on 8 September 2026.

| Processor | Rated memory speed, per the maker's spec page | Condition stated | Max capacity |
| --- | --- | --- | --- |
| Intel Core Ultra 9 285K | Up to DDR5 6400 MT/s | None on the page | 256 GB, 2 channels |
| Intel Core Ultra 5 250K Plus | Up to DDR5 7200 MT/s | None on the page | 256 GB, 2 channels |
| AMD Ryzen 9 9950X | DDR5-5600 | 2 modules, single or dual rank | 256 GB, 2 channels |
| AMD Ryzen 9 9950X | DDR5-3600 | 4 modules, single or dual rank | 256 GB, 2 channels |

AMD's page is the honest one. It lists four configurations and gives each its own speed, and the drop from 5600 to 3600 when you fill all four slots is a 36% cut in rated transfer rate. That's the most important number in this article for anyone planning to "add more RAM later": on AM5, adding two modules to two existing ones costs you a third of your memory speed on paper.

Intel's ARK pages give a single figure with no rank or slot condition. Puget Systems, which builds workstations on these chips, fills in the gap in its March 2026 test: the 6400 and 7200 MT/s figures apply to one module per channel using CUDIMMs, modules with a clock driver on board, and with more than two DIMMs the Intel parts fall to at best 4800 MT/s.

> [!WARNING]
> "Up to DDR5 7200 MT/s" on a spec page is the best case, not the default. Two dual-rank modules, or four of anything, and you are below it. The spec page will not tell you that; the motherboard's memory QVL will.

## How much does speed actually change, once you have enough capacity?

For most desktop software, a few percent. Puget Systems published the clearest recent measurement on 31 March 2026: the Core Ultra 7 270K Plus and Core Ultra 5 250K Plus at their rated DDR5-7200, then at DDR5-5600, both at JEDEC timings on an ASUS ProArt Z890 board with an RTX 5080.

| Workload (Puget Systems, 31 March 2026) | 7200 → 5600 on Core Ultra 200S Plus | 6400 → 5600 on non-Plus 285K / 265K |
| --- | --- | --- |
| Photo and video (Lightroom, Photoshop, After Effects, Premiere, Resolve) | about 3% | about 1% |
| Game development (Unreal shaders, lighting, code compile) | 5% overall; shader compile up to 11% | 1-3% |
| CPU rendering (Cinebench 2026, V-Ray, Blender) | 3% on the 270K Plus, 2% on the 250K Plus | under 1% |
| AI (MLPerf Client, llama.cpp) | about 4% average; llama token generation 16% | about 2% average; token generation 7-10% |
| Weighted overall | about 4% | about 1% |

The pattern is worth reading twice. Photoshop and After Effects barely noticed. Building lighting in Unreal Engine "showed virtually no scaling", in Puget's words. The two things that cared were shader compilation and generating tokens from a local language model, and those are the two workloads that stream large amounts of data through the CPU with no way to hide the wait in cache. We covered why that same limit caps [NPU throughput regardless of the TOPS number](/ai/npu-tops-explained/): bandwidth sets the token rate, and RAM speed is bandwidth.

Games behave like the token generator when the graphics card isn't the bottleneck. TechSpot's Steven Walton tested a Ryzen 7 9700X on 7 April 2025 across DDR5-5600, DDR5-6000 at CL40, CL30, CL28 and CL26, and DDR5-8000. At 1080p, Cyberpunk 2077 gained up to 12% from the DDR5-6000 CL30 review kit to DDR5-8000; Marvel Rivals gained 9% on average frames and 17% on 1% lows from the DDR5-5600 base to DDR5-8000; Counter-Strike 2 gained 4%. At 4K, the Cyberpunk gap shrank to 5% and the Counter-Strike results were, in TechSpot's phrase, "nearly entirely GPU-limited".

> [!NOTE]
> TechSpot didn't include the Ryzen 7 9800X3D, and says why: its stacked cache makes it "not particularly sensitive to memory performance". A large cache is a memory-speed substitute. If you own an X3D chip, the whole speed question is worth less to you than to everyone else.

## Why did DDR5-8000 barely beat DDR5-6000 CL26?

Because "speed" is two numbers, and the second one is latency. CL, or CAS latency, is how many clock cycles the module takes to start returning data after a request. A CL26 kit at 6000 MT/s answers in 26 cycles of a 3,000 MHz clock, about 8.7 nanoseconds; a CL38 kit at 8000 MT/s takes 38 cycles at 4,000 MHz, about 9.5 nanoseconds. The faster kit moves more data per second once it starts, but starts later.

On AMD's platform there's a second penalty. TechSpot explains that the memory controller on Zen 5's I/O die runs 1:1 with the memory clock up to 3,000 MHz, which is DDR5-6000. Push to DDR5-8000 and the controller drops to a 2:1 ratio, running at 2,000 MHz, a third slower than it was. The extra bandwidth has to pay back that loss before it shows a gain. In TechSpot's Cyberpunk test the DDR5-8000 kit finished 2% ahead of DDR5-6000 CL26; in Counter-Strike 2 and Marvel Rivals the two were, in their words, nearly identical. TechSpot also found only about half of the 21 X870 and X870E boards it tested would run DDR5-8000 at all.

This is the same lesson as [why the same chip scores differently in two phones](/phones/same-chip-different-benchmark-scores/): the headline figure is real, and the condition it runs under decides whether you ever see it.

> [!TIP]
> Compare kits by dividing CL by the clock in MHz (half the MT/s figure) to get first-word latency in nanoseconds. DDR5-6000 CL30 is 10.0 ns; DDR5-6000 CL26 is 8.7 ns; DDR5-8000 CL38 is 9.5 ns. Two kits with the same nanosecond figure will feel the same in latency-bound work, whatever the MT/s on the box.

## Where does capacity stop mattering?

At the point where your working set fits, and not a gigabyte before. Puget Systems' Peter Emery tested this on 1 June 2026 using a Ryzen 9 9950X3D2 with two 32 GB DDR5-5600 modules, then used Windows' `bcdedit` boot parameters to cap the same machine at 32 GB and 16 GB. Same modules, same speed, same everything else.

| Application (Puget Systems, 1 June 2026) | 32 GB vs 64 GB | 16 GB vs 64 GB |
| --- | --- | --- |
| Lightroom Classic, overall | 2.5% lower (AI tools 15% lower) | 45% lower; exports 118% slower |
| Photoshop, overall | no difference | 20% lower; filters 31% lower |
| After Effects, overall | no difference | 43% lower; 2D compositions 58% lower |
| Premiere Pro, overall | no difference | 7% lower; RAW footage 14% lower |
| DaVinci Resolve, overall | 2.5% lower | 9% lower; Fusion 31% lower |

Notice the shape of that table. Going from 64 GB to 32 GB cost almost nothing, because 32 GB still held the working set. Going to 16 GB cost between 7% and 45% because it didn't, and the machine was reading from the SSD instead. That's the cliff. Capacity is binary in a way speed never is: either the data fits or the computer is doing something else entirely.

Puget's own recommendation for professionals is 64 GB, and it flags Lightroom's AI tools and Resolve's Fusion page as the places 32 GB starts to bite. Nothing in that table suggests a home user with a browser, a game and a video call open is losing anything at 32 GB.

> [!ACTION]
> Before you pay for a faster kit:
> - Check the CPU maker's spec page for the rated speed and, on AMD, the slot-count condition. That's the speed the memory controller is validated for.
> - Buy two modules, not four. Both makers cut the rated speed when all four slots are filled.
> - Decide capacity from the worst application you run, not the average. 32 GB covers most desktops; 64 GB is the floor for RAW video, Fusion and Lightroom's AI tools, per Puget's June 2026 measurements.
> - Compare kits on nanoseconds, not just MT/s. CL divided by clock MHz.
> - If you own an X3D chip, stop worrying about speed. TechSpot says the cache does that job for you.

One more reason to get the capacity decision right the first time: the price. Puget's June 2026 article notes a single Kingston DDR5-5600 32 GB module that cost $98 in May 2025 was $478 a year later. At that price the 4% you'd gain from a faster kit is a rounding error against the 45% you'd lose from a smaller one. We've written before about how [a laptop's power limit, not its core count, decides its speed](/computers/laptop-cores-vs-desktop-cores/), and memory follows the same rule: the number that constrains you is rarely the one printed largest.

Specifications current as of 8 September 2026, read from JEDEC's 17 April 2024 JESD79-5C press release, Intel ARK for the Core Ultra 9 285K and Core Ultra 5 250K Plus, AMD's Ryzen 9 9950X product page, Puget Systems' articles of 31 March 2026 and 1 June 2026, and TechSpot's review of 7 April 2025. SpecWire has not tested any of this hardware; every measured value above is attributed to the lab that took it.
