---
title: "mAh vs Wh: which battery number should you actually compare?"
slug: mah-vs-wh-battery-capacity
seo_title: "mAh vs Wh: Which Battery Number Counts?"
meta: "mAh only means something at a stated voltage; Wh is the energy itself. What each battery number measures, who defines it, and why phones and laptops differ."
category: explainers
date: 2026-09-02
updated: 2026-09-02
description: "Milliamp-hours count charge; watt-hours count energy. Only one of them lets you compare a phone, a laptop and a power bank on the same scale, and the spec sheets that matter already know which."
image_alt: "Grouped bar chart comparing the typical and minimum battery capacity in milliamp-hours that Google and Molicel state for the Pixel 10 Pro, Pixel 10 Pro XL and the INR-21700-P45B cell"
tags: [mAh, Wh, battery capacity, watt-hours, milliamp-hours, IEC 61960, power bank, nominal voltage, FAA battery limit]
about: ["IEC", "Molicel", "Google Pixel", "Apple", "Federal Aviation Administration", "Anker"]
hero: chart
chart:
  type: grouped_bar
  title: "One battery, two numbers: typical vs minimum capacity, as the maker states it"
  y_label: "Capacity (mAh)"
  source: "Google Pixel 10 Pro tech specs; Molicel INR-21700-P45B data sheet v1.2, read 2 Sep 2026"
  series:
    - label: "Typical"
      points:
        - ["Pixel 10 Pro", 4870]
        - ["Pixel 10 Pro XL", 5200]
        - ["Molicel P45B cell", 4500]
    - label: "Minimum"
      points:
        - ["Pixel 10 Pro", 4707]
        - ["Pixel 10 Pro XL", 5079]
        - ["Molicel P45B cell", 4300]
key_takeaways:
  - text: "A watt-hour is energy; a milliamp-hour is charge, and voltage links them: Wh = V × Ah. That is the conversion the FAA prints on its PackSafe lithium battery page, updated 11 August 2026, alongside its **100 Wh** carry-on limit per battery."
    source: 7
  - text: "IEC 61960-3:2017 defines rated capacity as the charge, in ampere-hours, that a cell can deliver over a **5-hour** discharge at **20 °C** under the conditions in clause 7.3.1. It defines nominal voltage as a 'suitable approximate value' used to label a cell, not a measured one."
    source: 1
  - text: "Molicel's data sheet for the INR-21700-P45B cell, version 1.2, lists a typical capacity of **4,500 mAh (16.2 Wh)** and a minimum of **4,300 mAh (15.5 Wh)** at a nominal **3.6 V**. The same cell carries two capacity figures, 4.4% apart, and both are correct."
    source: 2
  - text: "Google's Pixel 10 Pro tech specs state the battery as 'Typical **4870 mAh** (minimum **4707 mAh**)'; the Pixel 10 Pro XL is 'Typical **5200 mAh** (minimum **5079 mAh**)'. Neither page states a voltage, so neither number converts to watt-hours without an assumption."
    source: 3
  - text: "Apple's 16-inch MacBook Pro spec page lists a '**100-watt-hour** lithium-polymer battery' with a footnote reading 'Actual rating of **99.6 watt-hours**'. The FAA's carry-on limit without airline approval is **100 Wh** per lithium-ion battery."
    source: [4, 7]
  - text: "Anker's own product page for its 25,000 mAh laptop power bank (model A1695) says charging losses cause 'a **30% to 45%** capacity reduction' and that a full charge 'typically delivers about **13,750 to 17,500mAh**'. The headline mAh is cell-side; the ports never see it."
    source: 8
faq:
  - q: "Is Wh or mAh better for comparing batteries?"
    a: "Watt-hours, every time, because a watt-hour is a unit of energy and a milliamp-hour is not. A milliamp-hour counts charge, and the energy that charge represents depends on the voltage it was stored at. Two 5,000 mAh batteries at different cell voltages hold different amounts of energy; two 18 Wh batteries hold the same energy regardless of how they are built. If a spec sheet gives you Wh, use it. If it only gives mAh, you need the nominal voltage to say anything about energy."
  - q: "How do I convert mAh to Wh?"
    a: "Multiply by the nominal voltage and divide by 1,000: Wh = (mAh × V) ÷ 1,000. Molicel's P45B data sheet makes the arithmetic visible, listing 4,500 mAh at 3.6 V nominal as 16.2 Wh. The catch is the voltage. Phone spec pages almost never print it, and using 3.7 V where the cell is really 3.6 V, or 3.85 V, moves the answer by several percent. The FAA's PackSafe page gives the same formula the other way round, as volts times amp-hours."
  - q: "Why does my phone spec say 'typical' and 'minimum' or 'rated' capacity?"
    a: "Because cells vary from the production line, and standards require the manufacturer to commit to a floor. IEC 61960-3:2017 defines rated capacity as a value the manufacturer declares, measured as what the cell delivers over a 5-hour discharge at 20 °C. Google's Pixel 10 Pro page lists 4,870 mAh typical and 4,707 mAh minimum, a gap of about 3.3%. Molicel's P45B data sheet lists 4,500 mAh typical and 4,300 mAh minimum. The typical figure is the average of tested samples; the minimum is the one every unit is supposed to clear."
  - q: "Why does Apple list hours for iPhone but watt-hours for MacBook?"
    a: "Apple's iPhone 17 Pro tech specs, as read on 2 September 2026, list 'Built-in rechargeable lithium-ion battery' and video playback figures of up to 33 hours, with no mAh or Wh at all. Its MacBook Air page lists a 53.8-watt-hour battery and its MacBook Pro page lists 72.4 and 100 watt-hours. The laptop numbers matter to air-travel rules, where the limit is written in watt-hours, so they get printed. For phones Apple chooses to publish only the outcome, which is defensible but means you cannot compare an iPhone's capacity against an Android phone's mAh from the spec sheets alone."
  - q: "Can I take a 25,000 mAh power bank on a plane?"
    a: "The FAA's PackSafe rules, current as of 11 August 2026, limit spare lithium-ion batteries and power banks to 100 Wh each without airline approval, carried in the cabin only, and 101 to 160 Wh with airline approval, maximum two. A 25,000 mAh bank at 3.6 V nominal works out to 90 Wh, which clears the limit; at 3.7 V it is 92.5 Wh. The FAA notes newer batteries have the Wh rating printed on them, so read the label rather than doing the sum, and check the airline, because the FAA page says many carriers set stricter limits on how many power banks you may bring."
  - q: "Why does a 25,000 mAh power bank charge my 5,000 mAh phone only three or four times?"
    a: "Because the 25,000 mAh is counted at the cells' own voltage and your phone is charged through a USB port at 5 V or more. Converting 25,000 mAh from 3.6 V to 5 V leaves 18,000 mAh of charge before any losses, and the boost converter, cable and the phone's own charging circuit each take a cut. Anker's product page for its A1695 25K bank says the reduction is 30 to 45%, and that a full bank typically delivers 13,750 to 17,500 mAh. Divide that by a 5,000 mAh phone battery and you get the three-and-a-bit charges people actually see."
products:
  - name: "Google Pixel 10 Pro"
    url: "https://store.google.com/product/pixel_10_pro_specs"
    cta: "Google tech specs"
    note: "The 'Typical 4870 mAh (minimum 4707 mAh)' line, and no voltage anywhere on the page"
  - name: "Apple MacBook Pro"
    url: "https://www.apple.com/macbook-pro/specs/"
    cta: "Apple tech specs"
    note: "72.4 Wh and 100 Wh batteries, with the 99.6 Wh 'actual rating' footnote on the 16-inch"
  - name: "Anker Laptop Power Bank (25K, 165W)"
    url: "https://www.anker.com/products/a1695-anker-power-bank-25000mah-165w"
    price: "$119.99"
    cta: "Anker product page"
    note: "25,000 mAh headline; the FAQ section admits 13,750 to 17,500 mAh delivered"
resources:
  - title: "IEC 61960-3:2017 — catalogue entry and free preview"
    url: "https://webstore.iec.ch/en/publication/29603"
    note: "The standard that defines rated capacity and nominal voltage for portable lithium cells. Clauses 3.4 and 3.5 are in the free preview pages"
  - title: "Molicel INR-21700-P45B product data sheet, v1.2"
    url: "https://www.molicel.com/wp-content/uploads/INR21700P45B_1.2_Product-Data-Sheet-of-INR-21700-P45B-80109.pdf"
    note: "A cell data sheet that prints mAh and Wh side by side for both typical and minimum capacity — the cleanest worked example there is"
  - title: "FAA PackSafe — Lithium Batteries"
    url: "https://www.faa.gov/hazmat/packsafe/lithium-batteries"
    note: "The 100 Wh and 160 Wh limits, the two-battery cap, and the regulator's own Wh conversion tip"
  - title: "49 CFR 175.10(a)(18)"
    url: "https://www.ecfr.gov/current/title-49/subtitle-B/chapter-I/subchapter-C/part-175/subpart-A/section-175.10#p-175.10(a)(18)"
    note: "The regulation behind the PackSafe summary, if you want the legal text"
  - title: "Apple MacBook Air — Tech Specs"
    url: "https://www.apple.com/macbook-air/specs/"
    note: "53.8 Wh stated plainly, alongside the test conditions for the hours figures"
sources:
  - title: "IEC 61960-3:2017 — Secondary lithium cells and batteries for portable applications — Part 3: Prismatic and cylindrical lithium secondary cells, and batteries made from them"
    url: "https://webstore.iec.ch/en/publication/29603"
    publisher: "IEC"
    accessed: 2026-09-02
    primary: true
  - title: "Product Data Sheet INR-21700-P45B, Version 1.2"
    url: "https://www.molicel.com/wp-content/uploads/INR21700P45B_1.2_Product-Data-Sheet-of-INR-21700-P45B-80109.pdf"
    publisher: "Molicel (E-One Moli Energy)"
    accessed: 2026-09-02
    primary: true
  - title: "Pixel 10 Pro & Pixel 10 Pro XL — Tech Specs"
    url: "https://store.google.com/product/pixel_10_pro_specs"
    publisher: "Google"
    accessed: 2026-09-02
    primary: true
  - title: "MacBook Pro — Tech Specs"
    url: "https://www.apple.com/macbook-pro/specs/"
    publisher: "Apple"
    accessed: 2026-09-02
    primary: true
  - title: "MacBook Air — Tech Specs"
    url: "https://www.apple.com/macbook-air/specs/"
    publisher: "Apple"
    accessed: 2026-09-02
    primary: true
  - title: "iPhone 17 Pro — Tech Specs"
    url: "https://www.apple.com/iphone-17-pro/specs/"
    publisher: "Apple"
    accessed: 2026-09-02
    primary: true
  - title: "PackSafe — Lithium Batteries"
    url: "https://www.faa.gov/hazmat/packsafe/lithium-batteries"
    publisher: "Federal Aviation Administration"
    accessed: 2026-09-02
    primary: true
  - title: "Anker Laptop Power Bank (25K, 165W, Built-In and Retractable Cables) — product page, model A1695"
    url: "https://www.anker.com/products/a1695-anker-power-bank-25000mah-165w"
    publisher: "Anker"
    accessed: 2026-09-02
    primary: true
  - title: "INR-21700-P45B — product page"
    url: "https://www.molicel.com/inr-21700-p45b/"
    publisher: "Molicel"
    accessed: 2026-09-02
    primary: true
---

Compare watt-hours. A watt-hour is a unit of energy, which is the thing a battery actually stores and the thing that runs your screen. A milliamp-hour is a unit of charge, and charge only becomes energy once you multiply it by a voltage. So **Wh = V × Ah**, exactly as the FAA prints it on its PackSafe page, and a mAh figure with no voltage attached is a number with a variable missing. Phone makers quote mAh because the voltage is roughly the same across phones and the bigger number looks better. Laptop makers quote Wh because air-travel rules are written in Wh. Neither is lying. But only one of them is handing you a number you can compare across categories without doing homework first.

## What does a milliamp-hour actually count?

Charge. One milliamp-hour is the charge that flows when one milliamp runs for one hour, so a 4,500 mAh battery can, under the conditions its maker chose, push out 900 mA for five hours. Notice what is missing: how hard that charge is being pushed. That is the voltage, and without it you cannot say how much work the battery can do.

The document that governs this for the cells in your phone is IEC 61960-3:2017, the International Electrotechnical Commission's performance standard for prismatic and cylindrical lithium cells in portable equipment. Clause 3.5 defines rated capacity as a value "determined under specified conditions and declared by the manufacturer", and the note beneath it pins down the conditions: it is the quantity of electricity, in ampere-hours, that a single cell can deliver over a **5-hour period** when charged, stored and discharged as clause 7.3.1 specifies, which is a discharge at 20 °C. Push the same cell harder, or colder, and it delivers less. The rated figure is not the cell's capacity in the abstract. It is the cell's capacity under one gentle, warm test.

> [!KEY]
> A mAh figure is a charge count at an unstated voltage, taken at an unstated discharge rate. IEC 61960-3 fixes the rate at a 5-hour discharge and the temperature at 20 °C. The voltage, you still have to find yourself.

## What does a watt-hour count, and why is it the honest unit?

Energy. One watt-hour is one watt sustained for one hour, and it already has the voltage folded in, because a watt is volts times amps.

Molicel's product data sheet for its INR-21700-P45B cell, version 1.2, reads like a worked example. Typical capacity: **4,500 mAh, 16.2 Wh**. Minimum capacity: **4,300 mAh, 15.5 Wh**. Nominal voltage: **3.6 V**. Check the arithmetic and it closes: 4.5 Ah × 3.6 V = 16.2 Wh. The data sheet also lists a charge voltage of 4.2 V and a discharge cut-off of 2.5 V, which is the part most spec sheets skip. A lithium cell does not sit at one voltage. It starts full near 4.2 V and slides down toward 2.5 V as it empties, and the 3.6 V "nominal" figure is an average that stands in for the whole slide. IEC 61960-3 is candid about this in clause 3.4, defining nominal voltage as a "suitable approximate value of the voltage used to designate or identify a cell". Approximate, and used to designate. It is a label, not a measurement.

That is the whole reason mAh comparisons wobble. Two cells with different chemistries can have different nominal voltages, and a 5,000 mAh cell at 3.85 V holds about 7% more energy than a 5,000 mAh cell at 3.6 V. The mAh number is identical. The energy is not.

| Quantity | Unit | What it measures | Needs a voltage to compare? |
| --- | --- | --- | --- |
| Charge | mAh (or Ah) | How many electrons the battery can deliver | Yes |
| Energy | Wh | How much work those electrons can do | No |
| Nominal voltage | V | The label value linking the two | It *is* the voltage |

> [!TIP]
> When a spec sheet gives mAh only, look for the nominal voltage on the battery's regulatory label, a teardown, or the maker's safety data sheet. Then compute Wh yourself. If you can't find the voltage, treat the mAh figure as comparable only with other phones, where cell voltages cluster closely, and not with anything else.

## Why does the same battery carry two capacity numbers?

Because cells vary, and the standard makes the manufacturer commit to a floor.

Google's tech specs page for the Pixel 10 Pro, read on 2 September 2026, gives the battery as "Typical **4870 mAh** (minimum **4707 mAh**)". The Pixel 10 Pro XL is "Typical **5200 mAh** (minimum **5079 mAh**)". The typical number is the average across tested samples; the minimum is what every shipped unit is supposed to meet. The gap is about 3.3% on the smaller phone and 2.3% on the larger, the same structure Molicel uses on a bare cell: 4,500 mAh typical against 4,300 mAh minimum, a 4.4% spread.

Marketing uses the typical figure, which is fair enough. But when two phones are 100 mAh apart on the headline, read them as equal, because the spread inside one model is bigger than the difference between them.

And note what Google's page does not say. There is no voltage anywhere on it. So 4,870 mAh cannot be turned into watt-hours from Google's own document, which means it cannot be placed on the same scale as a laptop, a tablet or a power bank without an assumption about the cell. Charging figures have the same shape of problem, which is why we walked through [what a 120 W charging claim actually delivers, minute by minute](/phones/120w-fast-charging-minute-by-minute/) rather than trusting the wattage on the box.

> [!NOTE]
> Apple goes one step further and publishes neither. Its iPhone 17 Pro tech specs, as of 2 September 2026, list a "Built-in rechargeable lithium-ion battery" and up to 33 hours of video playback, with no mAh and no Wh. You get the outcome and not the capacity, which is defensible for a buyer and useless for a comparison.

## Why do laptops quote Wh when phones quote mAh?

Because the rules that laptops bump into are written in watt-hours.

The FAA's PackSafe guidance for lithium batteries, last updated 11 August 2026, limits spare lithium-ion batteries and power banks to a rating of **100 Wh** per battery in carry-on baggage, with **101 to 160 Wh** allowed only with airline approval and capped at two per passenger. The regulator does not care about mAh, because mAh does not tell it how much energy could go into a fire. So laptop makers, whose batteries sit right up against that line, print the unit the rule is written in.

Apple's MacBook Pro tech specs make the pressure visible. The 14-inch models list a **72.4-watt-hour** battery. The 16-inch models list a **100-watt-hour** battery, and a footnote on that figure reads: "Actual rating of 99.6 watt-hours." That is a manufacturer designing to a regulatory ceiling and then telling you, in small type, that it landed 0.4 Wh underneath. Apple's MacBook Air page lists **53.8 watt-hours** with no such drama, because it is nowhere near the limit.

| Device | Capacity as the maker states it | Unit | Can you compare it directly? |
| --- | --- | --- | --- |
| Google Pixel 10 Pro | Typical 4870 mAh (minimum 4707 mAh) | mAh | Only against other phones |
| Google Pixel 10 Pro XL | Typical 5200 mAh (minimum 5079 mAh) | mAh | Only against other phones |
| Apple iPhone 17 Pro | Not stated; up to 33 h video playback | hours | No |
| Apple MacBook Air | 53.8 Wh | Wh | Yes |
| Apple MacBook Pro 16-inch | 100 Wh (actual rating 99.6 Wh) | Wh | Yes |
| Anker A1695 power bank | 25,000 mAh | mAh | Only with an assumed voltage |
| Molicel INR-21700-P45B cell | 4,500 mAh / 16.2 Wh typical | both | Yes |

> [!WARNING]
> "100 Wh" on a laptop is not a round marketing number. It is the FAA's carry-on ceiling, and makers design to sit just under it. If you see a laptop or power bank advertised above 100 Wh, check whether your airline will let it aboard before you check whether you want it.

## Why does a 25,000 mAh power bank not deliver 25,000 mAh?

Because the headline mAh is counted at the cells' own voltage, and your phone is charged at 5 V or higher through a USB port.

Anker's product page for its Laptop Power Bank (25K, 165W), model A1695, states a total capacity of **25,000 mAh** and prints no watt-hour figure at all. But its own FAQ on the same page answers the question in the section title: energy loss during charging, it says, "results in a 30% to 45% capacity reduction", and "a fully charged Anker 25,000mAh power bank typically delivers about 13,750 to 17,500mAh". Anker even offers a formula: multiply the total capacity by 0.65, then divide by your phone's battery capacity.

Two things eat the difference. The first is arithmetic. If the cells are 3.6 V nominal, the pack stores 25,000 mAh × 3.6 V = 90 Wh. Push that out at 5 V and the same 90 Wh is only 18,000 mAh, before anything has been lost. The mAh number shrank by 28% without a single joule going missing, because mAh was never the energy. The second is real loss: the boost converter, the cable and the phone's own charging circuit each waste some as heat. Anker's 30 to 45% bracket is the sum of both, and it is the only figure on the page that describes what the ports deliver.

> [!ACTION]
> Reading any battery spec:
> - Find the unit. Wh compares across everything; mAh compares only within one device class.
> - If it is mAh, find the nominal voltage before believing any cross-category comparison.
> - Check whether the figure is typical or minimum. Marketing uses typical; IEC 61960-3 rated capacity is the floor.
> - For a power bank, look for the maker's delivered-capacity note. Anker's is 55 to 70% of the headline.
> - For anything you will fly with, read the Wh on the label, not the box. The FAA's line is 100 Wh.

## So which number should you use?

Watt-hours whenever the document offers them, and computed watt-hours, with your voltage assumption stated, whenever it does not. Within one category, mAh is a serviceable shorthand: phone cells sit close enough in nominal voltage that a 10% mAh gap is a real gap. Across categories it fails, and in a power bank listing it fails even at the same voltage, because the number you're given and the number you get are separated by a converter.

Spec sheets are full of units that look interchangeable and aren't. Luminance has the same trap in reverse, where [nits and cd/m² really are one unit](/explainers/nits-cd-m2-lumens-explained/) and lumens only look like a third name for it. The fix is the same: find the document that defines the unit, read the test condition next to the figure, and compare like with like.

*Specifications current as of 2 September 2026, read from the IEC catalogue preview of 61960-3:2017, Molicel's P45B data sheet v1.2, Google's and Apple's tech specs pages, Anker's A1695 product page and the FAA's PackSafe lithium battery guidance as listed below.*
