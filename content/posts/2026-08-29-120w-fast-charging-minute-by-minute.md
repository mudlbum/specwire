---
title: "What 120W fast charging actually gets you, minute by minute"
slug: 120w-fast-charging-minute-by-minute
seo_title: "What 120W Fast Charging Really Buys"
meta: "A 120W brick holds 120W for minutes, not an hour. Here is what GSMArena measured at 15 and 30 minutes, and why full-charge time barely tracks wattage."
category: phones
date: 2026-08-29
updated: 2026-08-29
description: "The wattage on the charger is a ceiling that exists for the first slice of the charge. What matters is how much energy lands in the battery in the fifteen minutes you actually have."
image_alt: "Illustration for an article about smartphone fast charging wattage and how charging power tapers over time"
tags: [fast charging, 120W, HyperCharge, USB Power Delivery, charging curve, battery, smartphone charging, Ecodesign]
about: ["Xiaomi", "USB Implementers Forum", "Apple", "GSMArena", "European Commission", "HyperCharge", "USB Power Delivery"]
hero: photo
key_takeaways:
  - text: "Xiaomi's own specification for its 120W HyperCharge Combo (model MDY-14-EE) reaches **120.0 W** only on a **20.0 V ⎓ 6.0 A** rail. Its other listed rails are **66.0 W** at 11 V, **27.0 W** at 9 V and **15.0 W** at 5 V — the brick spends most of a charge on the lower ones."
    source: 1
  - text: "The USB Implementers Forum states that before USB PD Revision 3.1, USB Power Delivery was capped at **100 W** using **20 V** over Type-C cables rated at **5 A**. A 20 V ⎓ 6 A phone charger is therefore outside the USB-C current rating and runs a proprietary protocol."
    source: [2, 1]
  - text: "GSMArena's own charging test put the 100W Xiaomi 17 Pro Max at **44%** after 15 minutes and **82%** after 30, full in **39 minutes** from flat. The 45W-rated Galaxy S25 Ultra reached **41%** and **72%** over the same intervals."
    source: 3
  - text: "Two phones with identical **7,500 mAh** packs split badly in GSMArena's test: the 100W Xiaomi 17 Pro Max finished in **39 minutes**, the 80W Oppo Find X9 Pro in **1 hour 7 minutes** — **72%** longer for a **20%** lower rating."
    source: 3
  - text: "Apple's own fast-charge page quotes iPhone 17 Pro Max at **50%** in around **20 minutes** with a **40 W** or higher adapter, measured by Apple from a drained unit. Apple publishes no 100% figure at all."
    source: 4
  - text: "Regulation (EU) 2023/1670 has required, since **20 June 2025**, that smartphone batteries withstand at least **800** charge and discharge cycles while retaining at least **80%** of initial capacity, with the cycle count printed on the energy label."
    source: 5
faq:
  - q: "Does a 120W charger charge my phone twice as fast as a 60W one?"
    a: "No, and the gap is far smaller than the ratio suggests. Peak wattage is only drawn at a low state of charge, and it falls away as the cell voltage rises. In GSMArena's own charging test, the 100W Xiaomi 17 Pro Max reached 44% in fifteen minutes and the 45W Galaxy S25 Ultra reached 41% — three percentage points apart on paper, despite more than double the rating. The Xiaomi is moving more charge because its pack is half again as large, but nothing close to twice as fast."
  - q: "Why does my phone say 120W but the charge slows down after ten minutes?"
    a: "Lithium-ion cells are charged at roughly constant current until they hit their voltage limit, then held at that voltage while the current decays. Peak power lives in the first part of that curve. Once the pack is past about half full, the charger is no longer allowed to push the same current into it, so wattage falls regardless of what the brick can supply. This is why manufacturers quote 0–50% times far more often than 0–100% times."
  - q: "Is 120W charging bad for the battery?"
    a: "Fast charging generates more heat and heat is what ages a lithium-ion cell, but the effect is now bounded by regulation in the EU. Regulation (EU) 2023/1670 requires batteries in smartphones placed on the EU market since 20 June 2025 to survive at least 800 charge and discharge cycles while keeping at least 80% of their initial capacity, and the actual cycle figure has to appear on the energy label. If you want a specific model's number rather than the floor, look it up in the EPREL database using the QR code on that label."
  - q: "Do I have to use the charger that came in the box?"
    a: "For the headline speed, usually yes. Xiaomi's 120W adapter lists a 20.0 V ⎓ 6.0 A rail, and 6 A is above the 5 A that USB-IF specifies for Type-C cables in the classic 100 W USB Power Delivery arrangement. A generic USB-PD charger and cable will still charge the phone, but over the standard PD profiles the phone advertises separately — Xiaomi's own spec sheets list PD3.0 and PD2.0 as a distinct line from HyperCharge."
  - q: "Why is percentage a bad way to compare charging speed?"
    a: "Because a percent is a fraction of a pack, not a quantity of energy. Forty-four per cent of the Xiaomi 17 Pro Max's 7,500 mAh is about 3,300 mAh; 41% of the Galaxy S25 Ultra's 5,000 mAh is about 2,050 mAh. Near-identical percentages, roughly 60% more charge moved. Neither figure is energy either, since mAh omits voltage, but the comparison at least stops flattering small batteries."
  - q: "Has 120W charging gone away?"
    a: "It has become much less common on flagships while battery capacities have grown sharply. Xiaomi's 15T Pro is listed at 90W HyperCharge with a 5,500 mAh pack, and the Redmi Note 17 Pro Max at 100W HyperCharge with a 10,000 mAh silicon-carbon pack. Xiaomi still sells a standalone 120W adapter. The trend is toward more stored energy at a slightly lower peak rather than the other way around."
products:
  - name: "REDMI Note 17 Pro Max 5G"
    url: "https://www.mi.com/global/product/redmi-note-17-pro-max-5g/specs/"
    cta: "Xiaomi spec page"
    note: "10,000 mAh silicon-carbon pack, 100W HyperCharge, PD3.0/PD2.0 listed separately — check our transcription against it"
  - name: "Xiaomi 120W HyperCharge Combo (Type-A)"
    url: "https://www.mi.com/global/product/xiaomi-120w-hypercharge-combo-type-a/"
    cta: "Xiaomi spec page"
    note: "The full output rail list, including the 20.0 V ⎓ 6.0 A line that makes 120 W possible"
  - name: "Xiaomi 15T Pro"
    url: "https://www.mi.com/global/product/xiaomi-15t-pro/specs/"
    cta: "Xiaomi spec page"
    note: "90W HyperCharge on a 5,500 mAh pack, with no adapter in the box in most regions"
resources:
  - title: "USB-IF — USB Charger (USB Power Delivery)"
    url: "https://www.usb.org/usb-charger-pd"
    note: "The issuing body's own summary of what PD Revision 3.1 added, and what the old 100 W ceiling was built from"
  - title: "Xiaomi — 120W HyperCharge Combo (Type-A) specifications"
    url: "https://www.mi.com/global/product/xiaomi-120w-hypercharge-combo-type-a/"
    note: "Read the Output line. Five rails, one of which is 120 W, and a footnote saying the data is Xiaomi Laboratory's"
  - title: "Apple — Fast charge your iPhone"
    url: "https://support.apple.com/en-us/102574"
    note: "Apple's charge claims with the test conditions attached, model by model and year by year"
  - title: "GSMArena — Xiaomi 17 Pro Max battery life and charging test results"
    url: "https://www.gsmarena.com/xiaomi_17_pro_max_battery_life_and_charging_test_results-news-70064.php"
    note: "15-minute, 30-minute and time-to-full figures for seven current phones, measured in GSMArena's own lab"
  - title: "European Commission — Smartphones and Tablets: Ecodesign and Energy Label"
    url: "https://energy-efficient-products.ec.europa.eu/product-list/smartphones-and-tablets_en"
    note: "What the battery-endurance-in-cycles field on the EU energy label means and where to find a model's value"
  - title: "Regulation (EU) 2023/1670 — full text on EUR-Lex"
    url: "https://eur-lex.europa.eu/eli/reg/2023/1670/oj"
    note: "The ecodesign requirements themselves, Annex II onward"
sources:
  - title: "Xiaomi 120W HyperCharge Combo (Type-A) — specifications, model MDY-14-EE"
    url: "https://www.mi.com/global/product/xiaomi-120w-hypercharge-combo-type-a/"
    publisher: "Xiaomi"
    accessed: 2026-08-29
    primary: true
  - title: "USB Charger (USB Power Delivery)"
    url: "https://www.usb.org/usb-charger-pd"
    publisher: "USB Implementers Forum"
    accessed: 2026-08-29
    primary: true
  - title: "Xiaomi 17 Pro Max battery life and charging test results"
    url: "https://www.gsmarena.com/xiaomi_17_pro_max_battery_life_and_charging_test_results-news-70064.php"
    publisher: "GSMArena"
    accessed: 2026-08-29
    primary: true
  - title: "Fast charge your iPhone"
    url: "https://support.apple.com/en-us/102574"
    publisher: "Apple"
    accessed: 2026-08-29
    primary: true
  - title: "Smartphones and Tablets — Ecodesign requirements and Energy Label"
    url: "https://energy-efficient-products.ec.europa.eu/product-list/smartphones-and-tablets_en"
    publisher: "European Commission, Directorate-General for Energy"
    accessed: 2026-08-29
    primary: true
  - title: "REDMI Note 17 Pro Max 5G — full specifications"
    url: "https://www.mi.com/global/product/redmi-note-17-pro-max-5g/specs/"
    publisher: "Xiaomi"
    accessed: 2026-08-29
    primary: true
  - title: "Xiaomi 15T Pro — full specifications"
    url: "https://www.mi.com/global/product/xiaomi-15t-pro/specs/"
    publisher: "Xiaomi"
    accessed: 2026-08-29
    primary: true
---

A 120 W charger delivers 120 W for a few minutes near the start of a charge, and considerably less for the rest of it. Xiaomi's own specification for its 120W HyperCharge Combo, model MDY-14-EE, reads on the Output line: 5.0 V ⎓ 3.0 A at 15.0 W, 9.0 V ⎓ 3.0 A at 27.0 W, 11.0 V ⎓ 6.0 A at 66.0 W max, and 20.0 V ⎓ 6.0 A at 120.0 W max. Only the last of those is the number on the box.

What you get in practice is closer to this: in GSMArena's own charging test, a 100W phone went from flat to 44% in fifteen minutes and 82% in thirty. A 45W phone in the same test hit 41% and 72%. Less than half the rating, three points behind at the quarter hour.

## Why is a 120W rating not a 120W charge?

Because a lithium-ion cell will only take that current while it is nearly empty.

Charging runs in two phases. First constant current, where the charger pushes as much current as the pack is rated to accept and the cell voltage climbs. Then constant voltage, where the voltage is pinned at the limit and the current decays toward nothing. All the headline wattage lives in the first phase, and the first phase ends well before the battery is full. That is the whole reason manufacturers quote 0–50% times rather than 0–100% times. It is peak-versus-sustained, the same distinction that decides [why a 16-core laptop chip loses to an 8-core desktop](/computers/laptop-cores-vs-desktop-cores/) and [why one phone chip benchmarks 40% above another with the same name](/phones/same-chip-different-benchmark-scores/) — a burst rating that the physics only permits briefly.

Apple is unusually blunt about this. Its support page on fast charging, which we read on 29 August 2026, makes no 100% claim anywhere. It says an iPhone 17 Pro Max reaches 50% in around 20 minutes with a 40 W or higher adapter, and it attaches the conditions: Apple's own testing in July 2025, preproduction units, a drained battery, times measured from the appearance of the Apple logo as the unit started up. Every one of those conditions moves the number.

> [!KEY] The rail, not the badge
> Xiaomi's 120W adapter reaches its rating only on the **20.0 V ⎓ 6.0 A** rail. Its 11 V rail tops out at **66.0 W** and its 9 V rail at **27.0 W**. A charge that starts on 20 V does not stay there, and the brick's own spec sheet tells you what the alternatives are.

## What did an independent lab actually measure?

GSMArena published 15-minute, 30-minute and time-to-full figures for seven current phones alongside its Xiaomi 17 Pro Max battery results, using a flat battery and the bundled adapter. SpecWire has tested none of these phones; every figure below is GSMArena's own measurement, read on 29 August 2026.

| Phone (GSMArena's own measurements) | Battery | Rated charging | 15 min | 30 min | 0–100% |
| --- | --- | --- | --- | --- | --- |
| vivo X300 Pro | 5,440 mAh | 90W vivo FlashCharge | 55% | 100% | 0:29 |
| Xiaomi 17 Pro Max | 7,500 mAh | 100W Xiaomi HyperCharge | 44% | 82% | 0:39 |
| Xiaomi 17 Pro Max, over USB-PD | 7,500 mAh | 100W USB PD | 49% | 80% | 0:42 |
| Xiaomi 15 Ultra | 5,410 mAh | 90W Xiaomi HyperCharge | 42% | 72% | 0:51 |
| Galaxy S25 Ultra | 5,000 mAh | 45W USB PD + PPS | 41% | 72% | 0:59 |
| Oppo Find X9 Pro | 7,500 mAh | 80W SuperVOOC | 30% | 54% | 1:07 |
| iPhone 17 Pro Max | 4,832 mAh | 42W USB PD | 38% | 65% | 1:12 |

Read the two 7,500 mAh rows against each other. Same pack size, ratings 20% apart, and the finished charge takes 72% longer on the lower-rated phone. Now read the Galaxy S25 Ultra row against the Xiaomi 17 Pro Max: a rating gap of more than two to one produces a 15-minute gap of three percentage points.

Neither comparison is broken. They are measuring different things, and the spec sheet quietly encourages you to confuse them.

## Is a percentage the wrong unit?

Yes, and it is the biggest reason these numbers look strange.

A percent is a fraction of whatever pack the phone happens to have. Forty-four per cent of the Xiaomi 17 Pro Max's 7,500 mAh is roughly 3,300 mAh. Forty-one per cent of the Galaxy S25 Ultra's 5,000 mAh is roughly 2,050 mAh. Almost the same percentage, about 60% more charge actually moved. Milliamp-hours are not a great unit either, since charge without voltage is not energy, but at least they stop small batteries from looking fast for free.

> [!WARNING] "Full in 20 minutes" and "50% in 20 minutes" are not comparable claims
> Manufacturers publish whichever of the two flatters the product, and both are true statements about the same charging curve. Before comparing two phones, check that the endpoint is the same. It usually is not.

## Is a 120W phone charger even USB Power Delivery?

Generally not, and the current rating is the giveaway.

The USB Implementers Forum's own page on USB Power Delivery says that before Revision 3.1, PD was "limited to 100W using a solution based on 20V using USB Type-C cables rated at 5A". Revision 3.1 added fixed voltages of 28 V, 36 V and 48 V, taking the ceiling to 140 W, 180 W and 240 W respectively, with the USB Type-C specification updated to Release 2.1 to define the cables. So the sanctioned route to more than 100 W is more volts, not more amps.

Xiaomi's 120 W is 20 V at 6 A. That is above the 5 A cable rating USB-IF describes, at a voltage USB-IF caps at 100 W, which is why the speed depends on Xiaomi's own adapter, cable and handshake. The phone spec sheets say as much if you read the whole line: Xiaomi lists "100W HyperCharge" and "Supports PD3.0 / PD2.0" as two separate entries on the Redmi Note 17 Pro Max page. One is the proprietary path. The other is what a third-party charger gets.

This is the same shape of problem as [an HDMI port that carries a fraction of the bandwidth its version number implies](/explainers/4k-144hz-hdmi-cable/), as [two phones that are both IP68 while being rated for depths four times apart](/phones/ip68-rating-explained/), and as [a 990 kbps Bluetooth codec that usually negotiates down to 330](/audio/does-ldac-actually-sound-better-than-aac/). The figure is real. The condition that makes it real is what falls off the box.

> [!NOTE] GSMArena's PD row is worth a second look
> Their table includes the Xiaomi 17 Pro Max charged over generic USB-PD as a separate entry: **49%** at 15 minutes against **44%** on Xiaomi's own HyperCharge adapter, but **80%** against **82%** at 30 minutes and 42 minutes to full against 39. On that phone the proprietary path wins the back half of the charge, not the front.

## What does all this speed cost the battery?

Heat ages lithium-ion cells, and fast charging makes heat. The useful development is that the cost is now a published, regulated number rather than a matter of opinion.

Regulation (EU) 2023/1670, the European Commission's ecodesign regulation for smartphones, mobile phones, cordless phones and slate tablets, has applied to products placed on the EU market since 20 June 2025. Among its Annex II requirements: batteries must withstand at least 800 charge and discharge cycles while retaining at least 80% of their initial capacity. The companion energy labelling regulation, (EU) 2023/1669, puts the actual measured cycle count on the label as "battery endurance in cycles", alongside battery endurance per cycle in hours and minutes, a repeated free fall reliability class, a repairability class and the IP rating.

Eight hundred cycles is a floor, not a target. A phone that clears it by a wide margin has to say so, in a number, backed by an entry in the EPREL product database you reach through the QR code — which beats a marketing page promising the battery is "optimised".

> [!TIP] Look up the label before you believe the charging claim
> If a phone is sold in the EU, its energy label carries a cycle count and a QR code into EPREL. Two phones with the same charging wattage can carry very different cycle figures, and that is the number that describes how the phone will feel in year three.

## So what should you actually check?

The adapter's wattage is the least useful number in the transaction. Here is the order that works better.

> [!ACTION] Five minutes before you buy on a charging claim
> 1. **Find the endpoint of the claim.** "Full in 22 minutes" and "50% in 22 minutes" describe very different chargers, and both get printed the same size.
> 2. **Convert percentages to charge.** A percentage of a 10,000 mAh pack and a percentage of a 5,000 mAh pack are not the same amount of anything.
> 3. **Check whether the adapter is included.** Xiaomi's 15T Pro spec page states no power adapter is in the box and recommends its 90 W unit or above; the Redmi Note 17 Pro Max page lists a 100 W in-box charger.
> 4. **Read the second charging line.** "Supports PD3.0 / PD2.0" is what you get from a charger you already own, and it is usually well below the headline.
> 5. **Look at the cycle figure on the EU energy label**, not just the wattage. It is the only durability number on the box that anyone had to measure.

None of which makes fast charging a con. The vivo X300 Pro in GSMArena's table went from flat to 100% in 29 minutes, and the Redmi Note 17 Pro Max carries a 10,000 mAh silicon-carbon battery its own spec page pairs with a 100 W charger in the box. Charging genuinely got fast.

The wattage on the brick just is not the thing that got fast. It is the ceiling of a curve that spends most of its length somewhere else, and the only honest comparison is how much charge lands in the pack in the fifteen minutes you actually have — which nobody prints, and which somebody else has to measure for you.

*Specifications current as of 29 August 2026, verified against Xiaomi's product pages for the 120W HyperCharge Combo (MDY-14-EE), the REDMI Note 17 Pro Max 5G and the Xiaomi 15T Pro; the USB-IF's USB Power Delivery page; Apple's "Fast charge your iPhone" support document (published 24 March 2026); and the European Commission's ecodesign and energy label pages for smartphones and tablets covering Regulation (EU) 2023/1670. Charging measurements are GSMArena's own, read 29 August 2026. SpecWire operates no test lab and has charged nothing.*
