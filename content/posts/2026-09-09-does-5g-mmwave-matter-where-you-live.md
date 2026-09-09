---
title: "Does 5G mmWave matter where you live? Check your phone before you check the map"
slug: does-5g-mmwave-matter-where-you-live
seo_title: "5G mmWave: does it matter where you live?"
meta: "Most phones sold outside the US have no mmWave antennas. Apple's own spec pages prove it. What 3GPP's FR2 spec says, and when the bands matter."
category: phones
date: 2026-09-09
updated: 2026-09-09
description: "Before you compare coverage maps, check whether your handset has the hardware. Apple lists mmWave bands on its US iPhone 17 Pro spec page and omits them from the UK one — same phone, different radios. Here is what 3GPP's FR2 specification actually requires, and who mmWave is really built for."
image_alt: "Bar chart comparing 3GPP minimum peak EIRP against spherical coverage EIRP for each 5G FR2 band"
tags: [mmWave, 5G, FR2, 3GPP, n260, n261, EIRP, spectrum]
about: ["3GPP", "ETSI", "5G NR", "Apple", "Verizon", "Opensignal"]
hero: chart
key_takeaways:
  - text: "3GPP defines mmWave as Frequency Range 2, and TS 38.101-2 version **19.4.0** (published by ETSI in April 2026) splits it into FR2-1 at 24250–52600 MHz and FR2-2 at 52600–71000 MHz — everything a phone does below 7125 MHz is FR1, no matter what the status bar says."
    source: 1
  - text: "Whether mmWave matters where you live starts with the handset, not the network: Apple's US spec page lists iPhone 17 Pro models A3256 and A3257 with 5G NR mmWave bands **n258**, n260 and n261, while Apple's UK page lists models A3523 and A3526 with no mmWave line at all and describes them as 5G sub-6GHz only."
    source: [2, 3]
  - text: "The standard itself concedes that mmWave is directional: 3GPP TS 38.101-2 v19.4.0 requires a power class 3 handset on band n261 to reach **22.4** dBm peak EIRP, but only 11.5 dBm at the 50th percentile of radiated power measured over the full sphere around the device — a gap of about 11 dB, or roughly 12x in power."
    source: 1
  - text: "The speed comes from channel width, not magic: TS 38.101-2 v19.4.0 Table 5.3.5-1 allows FR2 channel bandwidths up to **400** MHz per carrier on n257, n258, n260 and n261, where FR1 tops out at 100 MHz."
    source: 1
  - text: "A \"5G UWB\" icon does not mean mmWave. Verizon's own support page states that its 5G Ultra Wideband network uses both high-band mmWave and mid-band C-band spectrum, and Verizon defines high-band as roughly **24** GHz to 39 GHz — so the indicator covers two very different technologies."
    source: [4, 5]
  - text: "When Opensignal last published a US mmWave-specific breakdown, on 14 October 2021, its Verizon users spent a mean of **0.5%** of their time connected to mmWave 5G, against statistically tied scores of 0.3% for AT&T and T-Mobile, while averaging 607.2 Mbps download on those connections."
    source: 6
faq:
  - q: "How do I know if my phone supports 5G mmWave?"
    a: "Look up your exact model number on the manufacturer's own specification page, not the marketing page. Apple splits its iPhone 17 Pro tech specs by model: A3256 and A3257 list a line reading '5G NR mmWave (Bands n258, n260, n261)', and A3523 and A3526 have no such line. On Android, check the band list for any n-number at or above n257. If the spec sheet only names bands below n100, the phone has no mmWave radio and no software setting will add one."
  - q: "What frequencies count as 5G mmWave?"
    a: "3GPP calls it Frequency Range 2. In TS 38.101-2 version 19.4.0, FR2-1 runs from 24250 MHz to 52600 MHz and FR2-2 from 52600 MHz to 71000 MHz. The bands phones actually use are n257 (26.5–29.5 GHz), n258 (24.25–27.5 GHz), n260 (37–40 GHz) and n261 (27.5–28.35 GHz). Band n263 covers 57–71 GHz and is unlicensed, subject to regional rules."
  - q: "Why is mmWave so much faster than regular 5G?"
    a: "Mostly because the channels are wider. 3GPP TS 38.101-2 v19.4.0 permits carriers up to 400 MHz wide on n257, n258, n260 and n261, and operators aggregate several of them. Sub-6 GHz 5G is capped at 100 MHz per carrier by the companion spec, TS 38.101-1. More spectrum in one pipe means more bits per second, before any cleverness in the radio."
  - q: "Why does mmWave drop when I hold the phone differently?"
    a: "Because the antennas are directional and your hand is in the way. 3GPP's spherical coverage requirement makes this explicit: on band n261, a power class 3 handset must manage 22.4 dBm peak EIRP pointed at the beam, but only 11.5 dBm at the 50th percentile of power radiated over the whole sphere. The standard is telling you that half the directions around the phone are around 11 dB weaker than the best one."
  - q: "Does the 5G UW or 5G UC icon mean I am on mmWave?"
    a: "No. Verizon's own 5G FAQs say the 5G Ultra Wideband network uses high-band mmWave and mid-band C-band spectrum together, and C-band sits at 3.7–3.98 GHz — nowhere near millimetre wavelengths. The icon tells you that you are on Verizon's faster tier, not which spectrum is carrying the data. To see the actual band you need a field-test or network-monitor app."
  - q: "Should I pay more for a phone with mmWave?"
    a: "Only if you spend real time in the places it is deployed: stadiums, arenas, airports, transit hubs and a handful of dense downtown blocks. Verizon's own description of high-band is that the waves travel shorter distances and suit dense urban settings and busy venues. Outside the US, most flagship phones are not sold with mmWave hardware at all, which makes the question moot in much of the world."
chart:
  type: grouped_bar
  title: "FR2 handset EIRP: beam peak vs all directions"
  y_label: "EIRP, dBm"
  source: "ETSI TS 138 101-2 V19.4.0 (2026-04), Tables 6.2.1.3-1 and 6.2.1.3-3"
  series:
    - label: "Min peak EIRP, power class 3"
      points: [["n257", 22.4], ["n258", 22.4], ["n259", 18.7], ["n260", 20.6], ["n261", 22.4], ["n262", 16.0], ["n263", 14.1]]
    - label: "Min EIRP at 50th-percentile CDF"
      points: [["n257", 11.5], ["n258", 11.5], ["n259", 5.8], ["n260", 8.0], ["n261", 11.5], ["n262", 2.9], ["n263", 2.3]]
products:
  - name: "iPhone 17 Pro (US models A3256 / A3257)"
    url: "https://www.apple.com/iphone-17-pro/specs/"
    cta: "Apple technical specifications"
    note: "Cellular and Wireless section lists 5G NR mmWave bands n258, n260, n261"
  - name: "iPhone 17 Pro (models A3523 / A3526)"
    url: "https://www.apple.com/uk/iphone-17-pro/specs/"
    cta: "Apple UK technical specifications"
    note: "Same phone, no mmWave line — described as 5G sub-6GHz with 4x4 MIMO"
resources:
  - title: "ETSI TS 138 101-2 V19.4.0 — NR UE radio transmission and reception, Range 2"
    url: "https://www.etsi.org/deliver/etsi_ts/138100_138199/13810102/19.04.00_60/ts_13810102v190400p.pdf"
    note: "Table 5.2-1 is the FR2 band list; 6.2.1.3-3 is the spherical coverage requirement"
  - title: "Apple: iPhone 17 Pro technical specifications (US)"
    url: "https://www.apple.com/iphone-17-pro/specs/"
    note: "The model-number split is under Cellular and Wireless, and it is the fastest way to check a handset"
  - title: "Verizon: 5G and 5G Ultra Wideband mobile networks FAQs"
    url: "https://www.verizon.com/support/5g-mobile-faqs/"
    note: "The operator saying in its own words that Ultra Wideband means mmWave and C-band together"
  - title: "Verizon: 5G spectrum and frequency bands explained"
    url: "https://www.verizon.com/about/news/5g-frequency-bands-explained"
    note: "Low, mid and high band defined by the operator, with the 24–39 GHz high-band range"
  - title: "Opensignal: Quantifying the mmWave 5G experience in the US"
    url: "https://www.opensignal.com/2021/10/14/quantifying-the-mmwave-5g-experience-in-the-us-october-update"
    note: "Dated October 2021, but still the clearest published per-carrier time-on-mmWave figures"
sources:
  - title: "ETSI TS 138 101-2 V19.4.0 (2026-04) — 5G; NR; User Equipment (UE) radio transmission and reception; Part 2: Range 2 Standalone (3GPP TS 38.101-2 version 19.4.0 Release 19)"
    url: "https://www.etsi.org/deliver/etsi_ts/138100_138199/13810102/19.04.00_60/ts_13810102v190400p.pdf"
    publisher: "ETSI / 3GPP"
    accessed: 2026-09-09
    primary: true
  - title: "iPhone 17 Pro and 17 Pro Max — Technical Specifications (US)"
    url: "https://www.apple.com/iphone-17-pro/specs/"
    publisher: "Apple"
    accessed: 2026-09-09
    primary: true
  - title: "iPhone 17 Pro and 17 Pro Max — Technical Specifications (United Kingdom)"
    url: "https://www.apple.com/uk/iphone-17-pro/specs/"
    publisher: "Apple"
    accessed: 2026-09-09
    primary: true
  - title: "5G and 5G Ultra Wideband mobile networks FAQs"
    url: "https://www.verizon.com/support/5g-mobile-faqs/"
    publisher: "Verizon"
    accessed: 2026-09-09
    primary: true
  - title: "5G spectrum and frequency bands: What they are and why they matter"
    url: "https://www.verizon.com/about/news/5g-frequency-bands-explained"
    publisher: "Verizon"
    accessed: 2026-09-09
    primary: true
  - title: "Quantifying the mmWave 5G experience in the US — October update"
    url: "https://www.opensignal.com/2021/10/14/quantifying-the-mmwave-5g-experience-in-the-us-october-update"
    publisher: "Opensignal"
    accessed: 2026-09-09
    primary: true
---

For most people, no — and the reason is usually sitting in your pocket rather than on a coverage map. 5G mmWave is 3GPP's Frequency Range 2, which TS 38.101-2 version 19.4.0 defines as 24250–52600 MHz (FR2-1) and 52600–71000 MHz (FR2-2). Handsets built for markets outside the United States mostly do not include the antennas for it. Apple's own specification pages make the point better than any analysis could: the US iPhone 17 Pro, models A3256 and A3257, lists "5G NR mmWave (Bands n258, n260, n261)". The same phone sold in the UK, models A3523 and A3526, has no mmWave line at all and is described as 5G sub-6GHz. So check the hardware first. If the radio isn't there, the map is irrelevant.

> [!KEY]
> mmWave is FR2, and FR2 starts at 24250 MHz. Everything your phone does below 7125 MHz — including C-band, n41, n77 and n78 — is FR1, no matter which icon the status bar shows.

## What counts as mmWave, exactly?

3GPP splits 5G NR into two frequency ranges and writes a separate radio specification for each. TS 38.101-2, published by ETSI as TS 138 101-2 and currently at version 19.4.0 (April 2026, Release 19), is the FR2 half. Its Table 5.2-1 is the complete list of bands a phone can use:

| Band | Frequency range | Duplex | Where you'll meet it |
| --- | --- | --- | --- |
| n257 | 26.5–29.5 GHz | TDD | Japan, parts of Asia |
| n258 | 24.25–27.5 GHz | TDD | Europe's 26 GHz pioneer band |
| n259 | 39.5–43.5 GHz | TDD | Rare in handsets |
| n260 | 37–40 GHz | TDD | US 39 GHz licences |
| n261 | 27.5–28.35 GHz | TDD | US 28 GHz licences |
| n262 | 47.2–48.2 GHz | TDD | Rare in handsets |
| n263 | 57–71 GHz | TDD | Unlicensed, region-dependent |

Every FR2 band is time-division duplex, meaning uplink and downlink share the same frequencies and take turns. That is one reason mmWave upload figures often disappoint relative to the download headline.

The reason mmWave is fast is unglamorous: there is simply more room up there. Table 5.3.5-1 of the same specification permits channel bandwidths of 50, 100, 200 and 400 MHz on the main handset bands, with 400 MHz optional in this release. The FR1 companion specification caps a single carrier at 100 MHz. Four times the pipe, before anyone gets clever with modulation. It's the same story as the [Gbps figures printed on cables and ports](/computers/thunderbolt-5-vs-usb4-v2/): a big number that describes the width of the road, not the traffic on it.

## Why does mmWave fall over when you move your hand?

Because the specification expects it to. This is the most quietly honest table in 3GPP's FR2 document, and almost nobody reads it.

TS 38.101-2 v19.4.0 sets two separate power requirements for a power class 3 handset — the ordinary phone class. Table 6.2.1.3-1 gives the minimum *peak* EIRP: the strength the phone must manage in its best direction, with the beam aimed at the network. Table 6.2.1.3-3 gives the *spherical coverage* requirement: the minimum EIRP at the 50th percentile of radiated power measured over the full sphere around the device.

| Band | Min peak EIRP | Min EIRP at 50th-percentile CDF | Gap |
| --- | --- | --- | --- |
| n257 | 22.4 dBm | 11.5 dBm | 10.9 dB |
| n258 | 22.4 dBm | 11.5 dBm | 10.9 dB |
| n259 | 18.7 dBm | 5.8 dBm | 12.9 dB |
| n260 | 20.6 dBm | 8.0 dBm | 12.6 dB |
| n261 | 22.4 dBm | 11.5 dBm | 10.9 dB |
| n262 | 16.0 dBm | 2.9 dBm | 13.1 dB |
| n263 | 14.1 dBm | 2.3 dBm | 11.8 dB |

Read the n261 row again. The standard demands 22.4 dBm when the beam is pointed correctly and 11.5 dBm across the median of all directions. That's an 11 dB spread, which is roughly twelve times the power. The specification is not describing a defect. It is describing a phone with a handful of small directional antenna arrays, some of which your palm is always covering, and it sets the bar accordingly.

> [!WARNING]
> If you have ever watched a mmWave connection collapse when you put the phone to your ear or stepped behind a pillar, you weren't unlucky. You were on the wrong side of that 11 dB.

## Does the 5G UW icon mean I'm on mmWave?

No, and this is the single most common misreading. Verizon's own 5G support FAQ states that its 5G Ultra Wideband network uses high-band mmWave *and* mid-band C-band spectrum. Verizon's spectrum explainer, published in June 2023, puts high-band at roughly 24 GHz to 39 GHz and C-band in the mid-band group, between 2.4 GHz and 4.2 GHz.

So a "5G UW" indicator means you are on the operator's premium tier. It does not tell you whether the bits are arriving on a 28 GHz beam from a lamp post fifty metres away or on a 3.7 GHz carrier from a conventional tower two kilometres out. Both light the same icon. Both feel fast. Only one of them is mmWave, and the two behave completely differently when you walk around a corner.

> [!TIP]
> To find the actual band, use a network-monitor or field-test app that reports the NR ARFCN or band number. n260 and n261 are mmWave. n77, n78 and n41 are not, however fast they feel.

## How much of the time is anyone actually on it?

Here is where SpecWire has to be straight with you: the honest per-carrier numbers are old, and nobody has replaced them with anything we can open and read.

The clearest published figures come from Opensignal, which measured its own US users' handsets over a 90-day window and published the analysis on 14 October 2021. Opensignal found its Verizon users spent a mean of 0.5% of their time actively connected to mmWave 5G, with AT&T and T-Mobile statistically tied at 0.3%. On those connections, Opensignal measured a 607.2 Mbps average download speed for Verizon users — more than twice what it saw on AT&T or T-Mobile — while uploads ran the other way, with Verizon at 28.1 Mbps against 35.5 and 37.8 Mbps for AT&T and T-Mobile.

That is a five-year-old measurement and we are not going to dress it up as current. Networks have been built out since. But the shape of the finding — a very fast connection you touch for a very small fraction of your day — matches what mmWave physically is, and Opensignal made the same point at the time: mmWave's job is to add capacity in dense places for short periods, not to blanket a city.

> [!NOTE]
> Opensignal also noted, from an earlier analysis, that in locations where mmWave was available its users consumed 4.5 times more data than on 4G and 2.4 times more than on sub-6 GHz 5G in the same period. That's the case for mmWave in one line: it is a capacity tool for crowds, not a coverage tool for people.

## So where does mmWave genuinely matter?

Three situations, and they are narrow.

You spend real time inside dense venues. Stadiums, arenas, convention centres, big airports and some transit stations are where operators actually hang mmWave radios, because that is where thousands of phones compete for the same tower. Verizon's own description of high-band says exactly this: shorter distances, dense urban settings and busy venues.

You are buying a US handset and the price difference is zero. On iPhone the mmWave hardware is bundled into the US models rather than sold as an upgrade, so there is nothing to weigh up. Just don't pay a premium on the used market for a US model if you live somewhere with no FR2 deployment — you'd be buying antennas that will never see a signal, and possibly a phone locked out of bands your local operator does use.

You're using 5G fixed wireless at a fixed address. A home receiver can be mounted in a window and aimed. That removes the two things that break mmWave on a phone — your hand, and walking. It's a different product with different physics, even though the band numbers match.

> [!ACTION]
> Before you buy for mmWave, in order:
> 1. Find your exact model number on the manufacturer's own spec page and look for a band at n257 or above.
> 2. Check your operator's coverage tool for a *high-band* or *mmWave* layer specifically — not the general 5G layer.
> 3. Ask whether the venues you actually visit are on that layer. If they aren't, mmWave is a spec-sheet line, not a feature.

## The number nobody publishes

Notice what's missing from all of this. Operators publish coverage maps that merge mmWave into a broader 5G footprint. Chipmakers publish modem peak rates — Qualcomm rates the Snapdragon 8 Elite Gen 5 modem at 12.5 Gbps down, a figure we picked apart in our [comparison of Snapdragon and Apple's published silicon specs](/phones/snapdragon-8-elite-vs-apple-a-series/) — that no carrier delivers to a phone. Phone makers list band numbers without saying which ones are deployed near you.

What nobody publishes is the one figure a buyer needs: how much of *your* week would land on FR2. That number depends on your commute, and no marketing department is going to produce it. This is the same structural gap you get with [IP ratings, where the certification tells you what was tested and not what your phone will survive](/phones/ip68-rating-explained/): the published number is real, and it answers a narrower question than the one you were asking.

The good news is that the check is quick. Model number, band list, one look for an n-number at 257 or above. If it's absent, you have your answer, and you can stop reading coverage maps entirely.

*Specifications current as of 9 September 2026. Band definitions and EIRP requirements read from ETSI TS 138 101-2 V19.4.0 (April 2026), carrying 3GPP TS 38.101-2 version 19.4.0 Release 19. Handset band lists read from Apple's US and UK iPhone 17 Pro technical specification pages. Network measurements are Opensignal's own, published 14 October 2021; SpecWire operates no test lab and has not measured any network.*
