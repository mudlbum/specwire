---
title: "Thunderbolt 5 vs USB4 v2: what changes at the port?"
slug: thunderbolt-5-vs-usb4-v2
seo_title: "Thunderbolt 5 vs USB4 v2: The Gap"
meta: "Thunderbolt 5 and USB4 Version 2.0 both signal at 80Gbps, but only one guarantees it. What Intel requires, what USB-IF merely permits, and what you get."
category: computers
date: 2026-08-30
updated: 2026-08-30
description: "USB4 Version 2.0 is a specification. Thunderbolt 5 is a certification programme built on top of it. That distinction decides whether the 80 Gbps on the box is a floor or a ceiling."
image_alt: "Illustration for an article comparing the Thunderbolt 5 certification requirements with the USB4 Version 2.0 specification"
tags: [Thunderbolt 5, USB4 Version 2.0, USB-C, PAM-3, Bandwidth Boost, DisplayPort 2.1, PCIe Gen 4, docks]
about: ["Intel", "USB Implementers Forum", "VESA", "Thunderbolt 5", "USB4", "DisplayPort 2.1", "OWC", "Macworld"]
hero: photo
key_takeaways:
  - text: "Intel's Thunderbolt 5 technology brief sets the PC speed requirement at **80 and 120 Gbps**, against **40 Gbps** for Thunderbolt 4, and raises the required PCIe throughput from **32 Gbps to 64 Gbps**."
    source: 1
  - text: "The USB-IF's 18 October 2022 announcement of USB4 Version 2.0 describes operation at **up to 80Gbps** using PAM3 encoding over existing **40Gbps** passive USB Type-C cables. The wording is a ceiling, not a floor."
    source: 2
  - text: "The **120 Gbps** figure is asymmetric. Intel's brief states that Bandwidth Boost dedicates **120 Gbps** to transmit while leaving **40 Gbps** for receive; evenly distributed, the link is **80 Gbps** in each direction."
    source: 1
  - text: "The USB-IF's Data Performance Language Usage Guidelines of January 2024 define **five** consumer marketing rates — **80, 40, 20, 10 and 5 Gbps** — and state that the term \"USB4 Version 2.0\" is not intended for use in product names or packaging."
    source: 3
  - text: "Macworld's Jon L. Jacobi measured OWC's Envoy Ultra at **6.44 GB/s** reading in AmorphousDiskMark on an M4 Pro MacBook Pro, but his real-world copy of roughly **330 GB** of .mov files wrote at only about **1.5 GB/s**."
    source: 6
  - text: "OWC's own product footnote rates the Envoy Ultra at over **6,000 MB/s** for initial writes and gives sustained write as **1,350 MB/s** on the 2 TB model and **1,700 MB/s** on the 4 TB model."
    source: 7
faq:
  - q: "Is Thunderbolt 5 the same thing as USB4 Version 2.0?"
    a: "No, though they share a physical layer. USB4 Version 2.0 is the specification published by the USB Implementers Forum on 18 October 2022. Thunderbolt 5 is Intel's certification programme built on top of it, announced on 12 September 2023, and Intel's own technology brief lists USB4 specification compliance as a Thunderbolt requirement. The specification says what a port may do; the certification says what it must do."
  - q: "Can a USB4 port be slower than 80 Gbps?"
    a: "Yes, and most are. The USB-IF's January 2024 language guidelines list five consumer rates — 80, 40, 20, 10 and 5 Gbps — and instruct vendors to state which one a product signals at. A laptop can carry a compliant USB4 port that tops out at 20 Gbps. Thunderbolt 5 has no such latitude: Intel's brief sets the PC speed requirement at 80 and 120 Gbps."
  - q: "Where does the 120 Gbps number come from?"
    a: "From asymmetric operation, which the USB-IF describes in its USB4 Version 2.0 announcement as an option for driving very-high-performance displays — up to 120 Gbps in one direction while retaining 40 Gbps in the other. Intel brands its implementation Bandwidth Boost. It is a redistribution of the same link, not extra capacity, and it favours the direction that feeds monitors. An external SSD does not benefit from it."
  - q: "Do I need a new cable for Thunderbolt 5?"
    a: "Not always. Intel's newsroom announcement states that PAM-3 signalling delivers the increase over today's printed circuit boards, connectors and passive cables up to 1 metre, and the USB-IF says 80Gbps runs over existing 40Gbps passive USB Type-C cables. Above 1 metre you are into certified active cables; Intel's brief lists universal cables up to 2 metres at 120 Gbps."
  - q: "Will a Thunderbolt 5 drive work on my older laptop?"
    a: "Usually, at the older port's speed, but check before you spend. OWC's own compatibility table gives the Envoy Ultra as over 6,000 MB/s on Thunderbolt 5, over 3,800 MB/s on USB4, over 2,800 MB/s on Thunderbolt 4 and up to 2,800 MB/s on Thunderbolt 3. Macworld's reviewer also found the drive would not enumerate at all on a Windows test bed until Asus shipped a BIOS and Thunderbolt firmware update."
  - q: "Is Thunderbolt 5 worth paying for today?"
    a: "It depends entirely on whether anything you own can saturate 40 Gbps. If you drive two high-refresh displays and a fast external SSD from one port, the extra headroom is real and the higher required charging ceiling — 140 W rather than 100 W — matters for larger laptops. If you use a dock for a keyboard, a monitor and Ethernet, Thunderbolt 4 already had far more bandwidth than you were using."
products:
  - name: "OWC Envoy Ultra Thunderbolt 5 SSD"
    url: "https://www.owc.com/solutions/envoy-ultra"
    cta: "Official product page"
    note: "Read footnote 2 on that page — it is where the sustained write figures live"
  - name: "Intel JHL9580 Thunderbolt 5 Controller"
    url: "https://www.intel.com/content/www/us/en/products/sku/225921/intel-jhl9580-thunderbolt-5-controller/specifications.html"
    price: "$19.00"
    cta: "Intel ARK page"
    note: "The controller behind most Thunderbolt 5 docks, with its PCIe and DisplayPort configuration listed"
resources:
  - title: "Intel — Thunderbolt 5 Technology Brief"
    url: "https://www.intel.com/content/dam/www/central-libraries/us/en/documents/2023-09/thunderbolt-5-technology-brief.pdf"
    note: "Figure 2 is the requirement table. It is the single most useful page in this whole subject."
  - title: "USB-IF — USB4 Version 2.0 publication announcement"
    url: "https://www.usb.org/sites/default/files/2022-10/USB-IF%20USB%2080Gbps%20Announcement_FINAL_v2.pdf"
    note: "Two pages, and the source of the PAM3 and 120Gbps asymmetric claims"
  - title: "USB-IF — USB Data Performance Language Usage Guidelines, January 2024"
    url: "https://usb.org/sites/default/files/usb_data_performance_language_usage_guidelines_jan_2024.pdf"
    note: "The document telling vendors to write 'USB 80Gbps' on the box and not the specification name"
  - title: "VESA — DisplayPort 2.1 specification release"
    url: "https://vesa.org/featured-articles/vesa-releases-displayport-2-1-specification/"
    note: "Where UHBR20, DP40 and DP80 cables are defined, and what DSC saves"
  - title: "Intel ARK — JHL9580 Thunderbolt 5 Controller"
    url: "https://www.intel.com/content/www/us/en/products/sku/225921/intel-jhl9580-thunderbolt-5-controller/specifications.html"
    note: "PCIe x4 Gen 4, three DisplayPort sinks, DP2.1 with DSC 1.2 — the dock silicon, in Intel's own words"
sources:
  - title: "Thunderbolt 5 Technology Brief (document 6447TDBACG092023)"
    url: "https://www.intel.com/content/dam/www/central-libraries/us/en/documents/2023-09/thunderbolt-5-technology-brief.pdf"
    publisher: "Intel"
    accessed: 2026-08-30
    primary: true
  - title: "USB-IF Announces Publication of New USB4 Specification to Enable USB 80Gbps Performance"
    url: "https://www.usb.org/sites/default/files/2022-10/USB-IF%20USB%2080Gbps%20Announcement_FINAL_v2.pdf"
    publisher: "USB Implementers Forum"
    accessed: 2026-08-30
    primary: true
  - title: "USB Data Performance Language Usage Guidelines from USB-IF, January 2024"
    url: "https://usb.org/sites/default/files/usb_data_performance_language_usage_guidelines_jan_2024.pdf"
    publisher: "USB Implementers Forum"
    accessed: 2026-08-30
    primary: true
  - title: "Intel Introduces Thunderbolt 5 Connectivity Standard"
    url: "https://newsroom.intel.com/client-computing/intel-introduces-thunderbolt-5-standard"
    publisher: "Intel"
    accessed: 2026-08-30
    primary: true
  - title: "VESA Releases DisplayPort 2.1 Specification"
    url: "https://vesa.org/featured-articles/vesa-releases-displayport-2-1-specification/"
    publisher: "VESA"
    accessed: 2026-08-30
    primary: true
  - title: "OWC Envoy Ultra review: Super-fast Thunderbolt 5 storage for your new M4 Pro/Max Mac"
    url: "https://www.macworld.com/article/2524461/owc-envoy-ultra-thunderbolt-5-storage-for-your-new-mac.html"
    publisher: "Macworld"
    accessed: 2026-08-30
    primary: true
  - title: "OWC Envoy Ultra — product specifications and performance footnotes"
    url: "https://www.owc.com/solutions/envoy-ultra"
    publisher: "Other World Computing"
    accessed: 2026-08-30
    primary: true
  - title: "Intel JHL9580 Thunderbolt 5 Controller — Product Specifications"
    url: "https://www.intel.com/content/www/us/en/products/sku/225921/intel-jhl9580-thunderbolt-5-controller/specifications.html"
    publisher: "Intel"
    accessed: 2026-08-30
    primary: true
  - title: "USB4 — specification overview"
    url: "https://www.usb.org/usb4"
    publisher: "USB Implementers Forum"
    accessed: 2026-08-30
    primary: true
---

They are not rivals. USB4 Version 2.0 is the specification, published by the USB Implementers Forum on 18 October 2022. Thunderbolt 5 is Intel's certification programme sitting on top of it, announced on 12 September 2023, and Intel's own technology brief lists USB4 specification compliance as one of its requirements. The difference that matters to a buyer is a single verb. USB4 v2 *permits* 80 Gbps. Thunderbolt 5 *requires* it — plus 64 Gbps of PCIe, dual 6K displays, and at least 140 W of charging on one port.

So a port marked USB4 can legitimately be a 20 Gbps port. A port marked Thunderbolt 5 cannot.

## What does Thunderbolt 5 require that USB4 Version 2.0 only allows?

Intel's Thunderbolt 5 technology brief, document 6447TDBACG092023, puts the requirements in a table, and it is worth reading directly rather than through anyone's summary. Here is what it lists against the previous generation.

| Requirement | Thunderbolt 5 | Thunderbolt 4 |
| --- | --- | --- |
| PC speed requirement | 80 and 120 Gbps | 40 Gbps |
| PC video requirement | Dual 6K | Dual 4K |
| PCIe throughput | 64 Gbps | 32 Gbps |
| USB 3 throughput | 10 Gbps (up to 20 available) | 10 Gbps |
| Required charging on at least one port | Up to 140 W, available to 240 W | Up to 100 W, available to 140 W |
| Thunderbolt networking | 64 Gbps | 32 Gbps |
| Universal cable length | 2 m at 120 Gbps | 2 m at 40 Gbps |
| USB4 specification compliance | Required | Required |

Every line is mandatory for a machine to carry the logo, and Intel certifies each shipping computer, accessory and cable rather than trusting a vendor's declaration. The USB4 specification has no equivalent gate: it defines what a compliant implementation may do, and the implementer chooses how much to build.

> [!KEY]
> Thunderbolt 5 is a floor. USB4 is a range. That single structural difference explains almost every confusing spec sheet in this category.

## Why is a USB4 port not automatically an 80 Gbps port?

Because the specification version and the speed are separate facts, and the USB-IF has explicitly asked vendors to stop conflating them.

Its Data Performance Language Usage Guidelines, dated January 2024, define five consumer-facing marketing names: USB 80Gbps, USB 40Gbps, USB 20Gbps, USB 10Gbps and USB 5Gbps, each meaning the product signals at that rate. The same document then states that the terms USB4 Version 2.0, USB4 Version 1.0, USB 3.2, SuperSpeed Plus and Enhanced SuperSpeed are defined in the specifications but "are not intended to be used in product names, messaging, packaging or any other consumer-facing content."

Which is sensible guidance that the market has spent years ignoring. When you see "USB4" on a laptop listing, you have been told which architecture the port implements and nothing at all about its speed. The number is the specification you want, and the number is the thing most listings omit.

> [!WARNING]
> "USB4 v2 support" on a spec sheet does not mean 80 Gbps. Look for the rate in Gbps, printed as its own line. If a manufacturer will not state it, assume the cheaper option.

## Where does 120 Gbps come from, and can you use it for data?

From asymmetry, and mostly no.

The USB-IF's 2022 announcement describes an option where the USB Type-C signal interface can be configured to deliver up to 120 Gbps in one direction while retaining 40 Gbps in the other, and says it exists for applications like driving very-high-performance displays. Intel brands its implementation Bandwidth Boost and describes it the same way: evenly distributed, the link runs 80 Gbps upstream and downstream; when display traffic spikes, it rebalances to 120 Gbps transmit and 40 Gbps receive.

Nothing is created. Eight lanes of 40 Gbps get reallocated four-and-four or six-and-two, and video is the traffic that runs one way.

For storage, which reads and writes in both directions, the ceiling stays at 80 Gbps. Macworld's Jon L. Jacobi made the point flatly in his Envoy Ultra review: 120 Gbps is unidirectional for displays, and bidirectional work like storage is limited to 80 Gbps. If you have seen a dock advertised as 120 Gbps and assumed your SSD would see it, that is the misreading the marketing invites.

On the display side the headroom is genuine. Intel says Bandwidth Boost gives up to 50% more video bandwidth than DisplayPort 2.1 at UHBR20, and VESA's own DisplayPort 2.1 release puts UHBR20 at 20 Gbps per lane across four lanes for a maximum throughput of 80 Gbps. That is the comparison Intel is drawing, and for once the marketing claim maps cleanly onto two published documents. It is also why the same reasoning that governs [whether a given cable can carry 4K at 144 Hz](/explainers/4k-144hz-hdmi-cable/) applies here — link rate, lane count, and whether compression is engaged.

## What does 80 Gbps actually deliver to a drive?

Considerably less than 10 GB/s, and the reason is stacked allocations.

Thunderbolt tunnels several protocols over one link. Intel's requirement table gives storage 64 Gbps of PCIe, not the full 80. Intel's ARK entry for the JHL9580 controller — the silicon inside most Thunderbolt 5 docks, at a $19.00 recommended customer price — lists its PCIe configuration as x4 Gen 4. Sixty-four gigabits per second is 8 GB/s before protocol overhead, and no shipping portable SSD is close to saturating it.

Macworld's measurements on an M4 Pro MacBook Pro give the practical shape of it. Jacobi recorded 5.2 GB/s both reading and writing in Blackmagic Disk Speed Test, 6.44 GB/s reading in AmorphousDiskMark, and near 7 GB/s reading with 5.57 GB/s writing in ATTO. Then he copied about 330 GB of .mov files and watched reads hold near 6 GB/s while writes fell to roughly 1.5 GB/s.

That write collapse is not a Thunderbolt problem. It is the SSD's cache running out, and OWC says so itself in footnote 2 of the Envoy Ultra product page: initial data rates over 6,000 MB/s, but longer write sessions sustain 1,350 MB/s on the 2 TB model and 1,700 MB/s on the 4 TB. Reads stay above 6,000 MB/s end to end.

| Measurement | Figure | Who measured it |
| --- | --- | --- |
| Blackmagic Disk Speed Test, read and write | 5.2 GB/s | Macworld |
| AmorphousDiskMark, read | 6.44 GB/s | Macworld |
| ATTO, read / write | ~7 GB/s / 5.57 GB/s | Macworld |
| Real-world 330 GB .mov copy, read | ~6 GB/s | Macworld |
| Real-world 330 GB .mov copy, write | ~1.5 GB/s | Macworld |
| Sustained write, 2 TB / 4 TB | 1,350 / 1,700 MB/s | OWC, own footnote |

> [!TIP]
> When a drive quotes one big number, look for the sustained figure. It is nearly always in a footnote, and for large-file work it is the only number that describes your actual afternoon.

## Does the cable have to change?

Less than you would expect, which is the quiet achievement here.

Both Intel and the USB-IF got to 80 Gbps by changing the encoding rather than the wire. The signalling moved to PAM-3, three-level pulse amplitude modulation, which carries more data per clock cycle at a lower baud rate than the two-level scheme it replaced. The USB-IF's announcement says 80Gbps runs over existing 40Gbps passive USB Type-C cables as well as newly defined 80Gbps active ones, and Intel's newsroom post says PAM-3 delivers the increase over today's printed circuit boards, connectors and passive cables up to 1 metre. Beyond a metre you need a certified active cable; Intel's table lists universal cables to 2 metres at 120 Gbps.

The display side has its own cable tiers, certified separately. VESA's DisplayPort 2.1 release, published 17 October 2022, defines DP40 cables as supporting UHBR10 across four lanes for 40 Gbps, and DP80 cables as supporting UHBR20 across four lanes for 80 Gbps. VESA also notes that DisplayPort 2.1 mandates its Display Stream Compression codec, which it says can cut transport bandwidth by more than 67% without visual artefacts.

> [!NOTE]
> Compression is doing quiet work in nearly every high-bandwidth link you own now. A port that "supports" a resolution and refresh rate may only reach it with DSC engaged, which is a defensible engineering choice and an undisclosed one.

## Should you pay for Thunderbolt 5?

Only if something you own can fill 40 Gbps, and most setups cannot.

The honest test is what hangs off the port at the same time. Two high-refresh displays plus a fast external SSD plus charging is a genuine case for the extra headroom, and the raised charging requirement matters independently: Thunderbolt 5 requires up to 140 W on at least one port where Thunderbolt 4 required 100 W, which is the difference between a large laptop charging properly through the dock and charging slowly.

A dock running a keyboard, a mouse, one monitor and Ethernet was never bandwidth-constrained on Thunderbolt 4 either.

And treat compatibility as something to verify rather than assume. Macworld's reviewer found the Envoy Ultra failed to appear in the BIOS, Disk Manager or Thunderbolt utility on a Windows test bed until Asus shipped a BIOS and Thunderbolt firmware update, despite the drivers being current. The certification programme is strict about what ships; it cannot retroactively fix what already shipped.

> [!ACTION]
> Before buying: find the rate in Gbps on the spec sheet rather than the specification name; check whether your workload is bidirectional, because 120 Gbps is transmit-only; look up the drive's sustained write, not its peak; and confirm your laptop's own port is certified Thunderbolt 5 rather than USB4, because the same silicon can present either.

The pattern here is the one that runs through most port marketing. A number describes a link's theoretical capacity under ideal conditions, then gets printed as though it describes your file copy. The same gap between a headline figure and delivered performance shows up in processors, which is [why two laptops with the same CPU can benchmark 34% apart](/computers/laptop-cores-vs-desktop-cores/), and in displays, where [what a DisplayHDR tier actually certifies](/displays/displayhdr-tiers-explained/) is narrower than the badge implies. Radio marketing does it too: 3GPP's own FR2 specification concedes an 11 dB gap between a phone's beam-peak and all-directions power, which is [why mmWave 5G is a venue technology rather than a coverage one](/phones/does-5g-mmwave-matter-where-you-live/).

Read the requirement table. It is two pages, it is free, and it settles arguments.

*Specifications current as of 30 August 2026. Intel's Thunderbolt 5 Technology Brief (document 6447TDBACG092023), Intel's 12 September 2023 newsroom announcement, the Intel ARK entry for the JHL9580 controller, the USB-IF's 18 October 2022 USB4 Version 2.0 announcement, the USB-IF Data Performance Language Usage Guidelines of January 2024, VESA's 17 October 2022 DisplayPort 2.1 release and OWC's Envoy Ultra product page were all read on that date. SpecWire has not tested any of this hardware; every measured value above is attributed to Macworld, whose Envoy Ultra review by Jon L. Jacobi was published 20 December 2024 and edited 15 February 2026.*
