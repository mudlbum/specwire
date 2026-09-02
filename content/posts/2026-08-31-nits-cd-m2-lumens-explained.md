---
title: "Nits, cd/m² and lumens: which one describes a screen?"
slug: nits-cd-m2-lumens-explained
seo_title: "Nits vs cd/m² vs Lumens"
meta: "Nits and cd/m² are the same unit. Lumens are not. Here is what each one measures, who defines it, and why 1,000 nits is really three numbers."
category: explainers
date: 2026-08-31
updated: 2026-08-31
description: "Nits and candela per square metre are two names for one unit. Lumens measure something else entirely. This is what each quantity means, which document defines it, and why a brightness figure without its test patch is not a measurement."
image_alt: "Grouped bar chart comparing VESA DisplayHDR tier requirements for an 8 percent centre patch against sustained full-screen luminance, in candela per square metre"
tags: [nits, candela per square metre, lumens, luminance, DisplayHDR, photometry, screen brightness, SI units]
about: ["VESA", "BIPM", "NIST", "Apple", "ISO", "IEC", "International System of Units"]
hero: chart
chart:
  type: grouped_bar
  title: "DisplayHDR CTS 1.2: one tier name, two luminance floors"
  y_label: "Minimum luminance (cd/m2)"
  source: "VESA DisplayHDR performance criteria, CTS 1.2, table updated July 2026"
  series:
    - label: "8% centre patch, 2% APL background"
      points:
        - ["HDR 400", 400]
        - ["HDR 600", 600]
        - ["HDR 1000", 1000]
        - ["HDR 1400", 1400]
        - ["True Black 1000", 1000]
    - label: "Full-screen, long duration"
      points:
        - ["HDR 400", 320]
        - ["HDR 600", 350]
        - ["HDR 1000", 600]
        - ["HDR 1400", 900]
        - ["True Black 1000", 500]
key_takeaways:
  - text: "A nit and a candela per square metre are the same unit of luminance: **1 nit = 1 cd/m²**. The candela is one of the seven SI base units, defined by the BIPM by fixing the luminous efficacy of 540 × 10¹² Hz radiation, K_cd, at **683 lm/W**."
    source: [1, 2]
  - text: "One candela is the luminous intensity of a source radiating **1/683 W per steradian** at 540 × 10¹² Hz — a yellow-green frequency chosen because that is where human vision peaks. The unit is calibrated to the eye, not to raw power."
    source: 1
  - text: "\"DisplayHDR 1000\" is three numbers, not one. VESA's CTS 1.2 criteria require **1,000 cd/m²** on an 8% centre patch, **1,000 cd/m²** on a full-screen flash, and only **600 cd/m²** full-screen over a long duration."
    source: 3
  - text: "DisplayHDR True Black 1000 asks for **1,000 cd/m²** on the 8% patch but just **500 cd/m²** full-screen sustained, alongside a black level of **0.0005 cd/m²** in the dual corner box test."
    source: 3
  - text: "Apple's Studio Display XDR specification lists **1000 nits** SDR brightness and **2000 nits** peak HDR, with the peak figure footnoted as applying at temperatures below **25 °C**."
    source: 4
  - text: "NIST realises the luminance unit by measuring illuminance **2.45 m** from an integrating-sphere source running at **2856 K** through a **6 mm** aperture, then computing L = E·d²/A. Every nit you read on a spec sheet traces back through a chain like that one."
    source: 5
faq:
  - q: "Is a nit the same as a candela per square metre?"
    a: "Yes, exactly. One nit is one candela per square metre, and the two are interchangeable in every context. Manufacturers tend to write nits because it is shorter and reads as a proper noun; standards bodies and measurement labs write cd/m² because that is the coherent SI expression. VESA's DisplayHDR criteria use cd/m² throughout, Apple's spec sheets use nits, and they are talking about the same quantity."
  - q: "Why do projectors use lumens instead of nits?"
    a: "Because a projector does not have a screen. Lumens measure luminous flux — the total light a source emits in every direction — which is the right quantity for something that throws light at a surface it does not control. A monitor emits light from a fixed area you can measure, so luminance in cd/m² is the natural unit. The luminance you actually see from a projector depends on the lumens, the screen area, and the screen's gain, and the projector maker only controls the first one."
  - q: "Are lumens and lux the same thing?"
    a: "No. A lumen is a unit of luminous flux, total light output. A lux is one lumen falling on one square metre — light arriving at a surface, which is illuminance. Luminance in cd/m² is light leaving a surface toward you. Flux, illuminance and luminance are three different questions: how much light is there, how much lands here, and how bright does that patch look."
  - q: "Why is my 1,000-nit monitor not 1,000 nits on a white page?"
    a: "Because that figure was almost certainly measured on a small bright patch, not a full screen. Under VESA's DisplayHDR CTS 1.2 criteria, a DisplayHDR 1000 monitor must hit 1,000 cd/m² on an 8% centre patch, but only 600 cd/m² across the whole screen for a sustained period. The gap is thermal and electrical: driving every subpixel hard at once draws far more power than lighting a small square, so the panel dims itself. That is normal, specified behaviour, not a fault."
  - q: "How many nits do I actually need?"
    a: "It depends on the ambient light you are working against, not on an absolute threshold, and the honest answer is that no standard prescribes a number for you. What the specification can tell you is which figure to read. For SDR desk work you are living in the full-screen sustained number, so that is the one to compare — a DisplayHDR 1000 panel only guarantees 600 cd/m² there. For HDR content the peak matters, because it applies to small specular highlights, which is what the 8% patch test is modelling."
  - q: "What are 'LED lumens' on a cheap projector?"
    a: "Not a standardised measurement. ISO/IEC 21118:2020 is the international standard covering what belongs on a data projector specification sheet, and it is the reference a projector maker cites when it wants its number to be comparable to anyone else's. Terms like 'LED lumens', 'light source lumens' or a bare 'lumens' with no standard named are outside that framework, and figures quoted that way routinely sit several times above what the same unit would measure under a named method. If the specification sheet does not name the standard, treat the number as marketing."
products:
  - name: "Apple Studio Display XDR"
    url: "https://www.apple.com/studio-display-xdr/specs/"
    cta: "Apple tech specs"
    note: "1000 nits SDR, 2000 nits peak HDR, 2304 dimming zones — and the temperature footnote on the peak figure"
resources:
  - title: "BIPM — SI base unit: candela"
    url: "https://www.bipm.org/en/si-base-units/candela"
    note: "The definition itself, including the exact 683 lm/W value that fixes the scale"
  - title: "VESA DisplayHDR performance criteria (CTS 1.2)"
    url: "https://displayhdr.org/performance-criteria/"
    note: "The full tier table. Read the row labels — patch size and duration are where the tiers actually differ"
  - title: "NIST — realization of related photometric units"
    url: "https://www.nist.gov/pml/sensor-science/optical-radiation/realization-related-photometric-units"
    note: "How a national metrology institute turns a lamp and an aperture into a traceable cd/m²"
  - title: "NIST — SI Units: luminous intensity"
    url: "https://www.nist.gov/pml/owm/si-units-luminous-intensity"
    note: "Short explanation of the candela and the V(λ) luminous efficiency weighting"
  - title: "ISO/IEC 21118:2020 — specification sheets for data projectors"
    url: "https://www.iso.org/standard/74674.html"
    note: "The catalogue entry for the standard that governs what a projector spec sheet should contain"
  - title: "BIPM — SI Brochure, 9th edition"
    url: "https://www.bipm.org/en/publications/si-brochure"
    note: "The whole system in one document, including every derived photometric unit"
sources:
  - title: "SI base unit: candela (cd)"
    url: "https://www.bipm.org/en/si-base-units/candela"
    publisher: "BIPM"
    accessed: 2026-08-31
    primary: true
  - title: "SI Units – Luminous Intensity"
    url: "https://www.nist.gov/pml/owm/si-units-luminous-intensity"
    publisher: "NIST"
    accessed: 2026-08-31
    primary: true
  - title: "DisplayHDR Performance Criteria, CTS 1.2"
    url: "https://displayhdr.org/performance-criteria/"
    publisher: "VESA"
    accessed: 2026-08-31
    primary: true
  - title: "Studio Display XDR — Technical Specifications"
    url: "https://www.apple.com/studio-display-xdr/specs/"
    publisher: "Apple"
    accessed: 2026-08-31
    primary: true
  - title: "Realization of related photometric units"
    url: "https://www.nist.gov/pml/sensor-science/optical-radiation/realization-related-photometric-units"
    publisher: "NIST"
    accessed: 2026-08-31
    primary: true
  - title: "ISO/IEC 21118:2020 — Information to be included in specification sheets for data projectors"
    url: "https://www.iso.org/standard/74674.html"
    publisher: "ISO"
    accessed: 2026-08-31
    primary: true
  - title: "SI Brochure: The International System of Units, 9th edition"
    url: "https://www.bipm.org/en/publications/si-brochure"
    publisher: "BIPM"
    accessed: 2026-08-31
    primary: true
---

Nits describe a screen. Lumens describe a light source. And a nit is not a rival to candela per square metre — it is the same unit under a shorter name, so **1 nit = 1 cd/m²** exactly. That single equivalence resolves most of the confusion on a display product page, because manufacturers write nits and standards bodies write cd/m², and readers reasonably assume two words mean two things.

The harder problem comes next. A luminance figure only means something once you know the size of the patch it was measured on and how long the panel held it. "1,000 nits" can be three different measurements on the same monitor, and under VESA's own certification rules it usually is.

## What are the four units, and which one is on your monitor's box?

Photometry has four quantities that get muddled, and they answer four different questions.

| Quantity | Unit | What it answers |
| --- | --- | --- |
| Luminous flux | lumen (lm) | How much visible light does this source emit in total? |
| Luminous intensity | candela (cd) | How much light goes in this particular direction? |
| Illuminance | lux (lx) | How much light is landing on this surface? |
| Luminance | cd/m², a.k.a. nit | How bright does this surface look from where I'm standing? |

A monitor, a phone and a TV all emit light from a fixed, measurable area, so luminance is the natural unit and the box says nits. A projector bulb throws light in a cone at a surface it does not own, so flux is the natural unit and the box says lumens. A room's lighting design is specified in lux, because what matters is how much light reaches the desk.

> [!KEY]
> Nit and cd/m² are the same unit. If a spec sheet uses both words for two different figures, it is being sloppy, not precise.

## What is a candela, and why 683?

The candela is one of the seven SI base units, and the BIPM defines it by fixing a constant: the luminous efficacy of monochromatic radiation at a frequency of 540 × 10¹² Hz, written K_cd, is exactly **683 lm/W**. Invert that and you get the plain-language version the BIPM also publishes — one candela is the luminous intensity of a source emitting monochromatic radiation at 540 × 10¹² Hz with a radiant intensity of 1/683 watt per steradian in that direction.

Two things in there are worth slowing down for.

The first is the frequency. 540 THz is a yellow-green, and it was picked because that is roughly where human photopic vision peaks. Radiation at any other frequency still gets measured in candelas, but it is weighted by the standard luminous efficiency curve, V(λ), which NIST describes as peaking at that same yellow-green. So the candela is not a physics unit that happens to involve light. It is a physics unit deliberately bent around one species' retina. A watt of deep red and a watt of yellow-green are the same energy and wildly different candelas.

The second is the steradian. Intensity is per unit solid angle, which is why a torch and a bare bulb can emit identical lumens and give completely different candela readings — the torch concentrates its flux into a narrow cone. Luminance is then intensity per unit area of the emitting surface: cd/m². Flux, then direction, then area.

> [!NOTE]
> The candela is the only SI base unit whose definition is tied to human perception. The 2018 revision of the SI changed the definitions of the kilogram, ampere, kelvin and mole; the candela kept its 683 lm/W constant and was simply restated in the same explicit-constant form as the other six.

## Why "DisplayHDR 1000" is really three numbers

This is where the unit stops being the interesting part and the test condition takes over.

VESA's DisplayHDR compliance test specification — CTS 1.2, released 7 May 2024, with the summary tier table updated in July 2026 — measures peak white three separate ways, and a monitor has to clear all three to wear the badge. For DisplayHDR 1000, the requirements are:

| Test | DisplayHDR 1000 minimum |
| --- | --- |
| 8% centre patch, 2% APL background | 1,000 cd/m² |
| Full-screen flash | 1,000 cd/m² |
| Full-screen, long duration | 600 cd/m² |

So a certified DisplayHDR 1000 monitor is guaranteed to be a 600-nit display when you fill the screen with white and leave it there. The 1,000 figure applies to a small square, or to a brief flash. VESA is explicit about the intent — the flash test represents "very brief usage such as an explosion in a movie or game", and the long-duration test represents stable full-screen use.

The gap widens as the tiers climb. DisplayHDR 400 asks for 400 cd/m² on the patch and 320 sustained, a 20% drop. DisplayHDR 1400 asks for 1,400 on the patch and 900 sustained, a 36% drop. And the True Black tiers, aimed at emissive panels, relax the full-screen numbers much further: True Black 1000 requires 1,000 cd/m² on the 8% patch but only 500 cd/m² on both the flash and the long-duration test, while demanding a black level of 0.0005 cd/m² in the dual corner box test. That trade is the whole design philosophy of the tier, and it is legible in the table if you read the row labels instead of the column headers.

If you want the tier-by-tier walkthrough, we've covered [what each DisplayHDR tier actually certifies](/displays/displayhdr-tiers-explained/) separately. The point here is narrower: the unit was never the ambiguous part.

> [!WARNING]
> A brightness number quoted without its patch size and duration is not a measurement. It is a maximum, taken under whichever of the three conditions flattered the panel most.

## What does Apple's "2000 nits" promise?

Apple's own technical specifications for the Studio Display XDR list a 27-inch 5K panel with a Mini-LED backlight and 2,304 dimming zones, rated at **up to 1000 nits brightness (SDR)** and **2000 nits peak brightness (HDR)**. The word "peak" is doing the same work VESA's 8% patch does, and Apple attaches a footnote to it: the figure applies at temperatures less than 25 °C.

Read that footnote as a general rule rather than an Apple quirk. Luminance costs power, power becomes heat, and heat forces the panel to back off. Every peak brightness figure on every display is bounded by a thermal condition somewhere, whether or not the manufacturer prints it. Apple printed it.

Notice also that Apple separates the SDR and HDR numbers, which is more useful than one headline figure. The 1000-nit SDR rating governs your spreadsheet at midday. The 2000-nit peak governs a specular highlight in an HDR grade, for a fraction of a second.

> [!TIP]
> When you compare two displays, compare like conditions: patch-to-patch, or sustained-to-sustained. Comparing one maker's peak against another's full-screen number tells you nothing except which marketing department was braver.

The habit generalises well beyond screens. Processor benchmarks carry a hidden test condition in exactly the same way, which is [why the same Snapdragon 8 Elite posts scores 40% apart in different phones](/phones/same-chip-different-benchmark-scores/): the benchmark is built to pause between workloads so heat cannot accumulate, so the score describes a chip that was kept cool rather than one under sustained load.

## When are lumens the right unit?

When the light source and the surface are different objects. Projectors are the everyday case.

A projector's flux, in lumens, is fixed by the projector. The luminance you actually perceive is not, because it depends on how far that flux gets spread and on how much of it the screen sends back toward your seat rather than scattering elsewhere. Move the same projector from a 60-inch screen to a 100-inch one and its output covers about 2.8 times the area, so every square metre of image gets roughly a third as much light. Two identical projectors in two rooms produce two different cd/m² readings. That is not a defect in the lumen; it is the lumen answering the question it was designed for.

The standards position here is worth knowing. ISO/IEC 21118:2020, Edition 3, published February 2020 by ISO/IEC JTC 1/SC 28, specifies the information to be included in specification sheets for front-projection data projectors. It was confirmed in 2025 and is now flagged for revision, with a committee draft in progress. When a projector maker states a luminance figure "per ISO 21118", it is committing to a defined disclosure framework. When a listing says "12,000 LED lumens" and names no standard at all, there is nothing to check it against.

> [!ACTION]
> Reading a projector listing:
> 1. Find the standard named next to the lumen figure. No standard, no comparison.
> 2. Check whether the figure describes white light output or colour light output. They are separate measurements and a spec sheet that quotes only one of them has chosen which.
> 3. Work out the throw distance and screen size you'll actually use, then stop comparing lumens across different screen sizes.
> 4. Treat any four-figure lumen claim on a sub-$200 unit as unverified until a named source measures it.

## Who actually checks a nit?

Somebody has to, or the unit is a rumour. In the United States that somebody is NIST, and the procedure it publishes is refreshingly concrete.

NIST realises the luminance unit using a reference integrating-sphere source operated at 2856 K, 15 cm across, with a 6 mm precision aperture at its exit port. Standard photometers measure the illuminance 2.45 m away, and the average luminance over the aperture plane falls out of L = E·d²/A — illuminance times distance squared, divided by aperture area. The whole arrangement sits in a light-tight box on the photometry bench to keep stray light out, and the calibration is repeated every time a luminance measurement is performed. NIST last updated that page on 19 December 2025.

Every colorimeter a review outlet points at a monitor traces back, through some number of calibration steps, to a realisation like that one. It is also why measurements from different labs on the same panel rarely agree to the last digit, and why a figure with a named lab and a stated method attached is worth more than a bigger number with neither.

## How do you read a brightness spec in thirty seconds?

Four questions, in order. What patch size? What duration? What content mode — SDR or HDR? And who measured it?

If a spec sheet answers all four, you can compare it to another that does. If it answers none, you have a number, not a measurement, and the only thing you can safely conclude is that the panel reached that luminance at least once under conditions nobody has told you. The units themselves — nits, cd/m², lumens — were never the obstacle. They are well defined, internationally agreed, and traceable to a lamp in a light-tight box in Maryland. What varies is everything around them.

Worth noting too that luminance is only half of what your eye is judging. How bright a screen looks also depends on how dark it can go and how much room light it reflects back at you, which is why [the QD-OLED versus WOLED question turns on your room more than on the panel](/displays/qd-oled-vs-woled/). A cd/m² figure describes light leaving the panel. It says nothing about the light arriving from the window behind you.

*Specifications current as of 31 August 2026: VESA DisplayHDR CTS 1.2 tier table as updated July 2026; BIPM SI Brochure, 9th edition; Apple Studio Display XDR technical specifications; ISO/IEC 21118:2020, Edition 3; NIST photometric realisation page as updated 19 December 2025. SpecWire does not operate a test lab and takes no measurements of its own.*
