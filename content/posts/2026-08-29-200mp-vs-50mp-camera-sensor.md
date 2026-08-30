---
title: "Does a 200MP camera take better photos than a 50MP one?"
slug: 200mp-vs-50mp-camera-sensor
seo_title: "200MP vs 50MP: Better Photos?"
meta: "A 200MP phone writes a 12.5MP file by default, and DXOMARK's top-scoring main camera is 50MP. What the megapixel number does and doesn't measure."
category: phones
date: 2026-08-29
updated: 2026-08-29
description: "Megapixels are the one camera number with no measurement standard behind it. Here is what Samsung's own datasheets say a 200MP sensor does with those pixels, and what the labs measured when they pointed it at a chart."
image_alt: "Bar chart comparing the effective pixel pitch of Samsung ISOCELL 200MP and 50MP image sensors in each of their output modes"
tags: [megapixels, pixel binning, ISOCELL HP2, image sensor, pixel pitch, DXOMARK, ISO 12233, smartphone camera]
about: ["Samsung Electronics", "ISOCELL HP2", "ISOCELL GNJ", "DXOMARK", "ISO", "Apple", "Huawei"]
hero: chart
chart:
  type: bar
  title: "Effective pixel pitch by output mode, from Samsung's own press releases"
  y_label: "Pixel pitch (µm)"
  source: "Samsung Electronics, 17 January 2023 and 27 June 2024"
  series:
    - label: "Effective pixel pitch"
      points:
        - ["HP9 · 200MP", 0.56]
        - ["HP2 · 200MP", 0.6]
        - ["JN5 · 50MP", 0.64]
        - ["GNJ · 50MP", 1.0]
        - ["HP2 · 50MP", 1.2]
        - ["HP9 · 12MP", 2.24]
        - ["HP2 · 12.5MP", 2.4]
key_takeaways:
  - text: "Samsung's own press release for the 200MP ISOCELL HP2 states the sensor packs **200 million 0.6 µm** pixels in a **1/1.3-inch** optical format, and that its Tetra²pixel binning turns it into a **1.2 µm 50MP** or **2.4 µm 12.5MP** sensor by binding four to 16 neighbouring pixels."
    source: 1
  - text: "In DXOMARK's own lab testing, the 50MP Huawei Pura 80 Ultra scored **184** on the Photo Main sub-score against **167** for the 200MP Samsung Galaxy S26 Ultra — the highest Photo Main result DXOMARK lists, from a camera with a quarter of the pixel count."
    source: [3, 4]
  - text: "\"50MP\" describes sensors of wildly different size. Samsung's ISOCELL GNJ is **50 million 1.0 µm** pixels in a **1/1.57-inch** format; its ISOCELL JN5 is **50 million 0.64 µm** pixels in a **1/2.76-inch** format, both announced on the same day in June 2024."
    source: 2
  - text: "Apple's iPhone 17 Pro technical specifications list the Fusion Main camera as **48MP** at **ƒ/1.78**, with 48MP capture offered as an opt-in \"super-high-resolution\" mode alongside **24MP** rather than as the default output."
    source: 5
  - text: "Resolution has a published measurement standard and megapixel count is not it. **ISO 12233:2024**, edition **5**, published September 2024 by ISO/TC 42, specifies how to measure the resolution and spatial frequency response of a digital camera."
    source: 6
  - text: "DXOMARK's published protocol puts each phone through roughly **1,500** images and more than **two hours** of video across light levels from **10,000 lux** down to **1 lux**, with about **ten days** of engineering time per device."
    source: 7
faq:
  - q: "Why does my 200MP phone save a 12MP photo?"
    a: "Because that is the mode the sensor ships in. Samsung's ISOCELL HP2 press release describes Tetra²pixel binning that merges four or sixteen neighbouring pixels into one, so the sensor behaves as a 1.2 µm 50MP part or a 2.4 µm 12.5MP part depending on light. Combining sixteen small pixels into one large one collects the same light over a bigger area with one readout instead of sixteen, which is why the binned file usually looks cleaner than the full-resolution one. The 200MP mode is still there, in the menu, for when you want it."
  - q: "Is a 50MP camera worse than a 200MP camera?"
    a: "Not by any measurement anyone publishes. In DXOMARK's testing the highest Photo Main sub-score belongs to the Huawei Pura 80 Ultra at 184, and DXOMARK lists its main camera as a 50MP 1-inch sensor with 1.6 µm pixels. The 200MP Galaxy S26 Ultra scored 167 in the same category. Pixel count is one input to image quality and not the dominant one."
  - q: "What actually decides how detailed a phone photo is?"
    a: "Sensor area, lens quality and aperture, stabilisation, and the processing pipeline, roughly in that order of how often they are the limiting factor. Total sensor area sets how many photons the camera can collect in a given exposure; the lens sets how finely those photons can be placed. Megapixels only tell you how the collected light is subdivided, which matters mainly when you crop."
  - q: "Does the 200MP mode ever help?"
    a: "Yes, in two specific places. Cropping is the obvious one, since a 200MP frame survives a hard crop that would fall apart at 12MP. The other is in-sensor zoom: Samsung says the ISOCELL HP9 offers 2x and 4x in-sensor zoom modes via a remosaic algorithm, reaching up to 12x when paired with a 3x telephoto module. Samsung also uses the 50MP intermediate mode to shoot 8K video, which is about 33MP per frame, so the extra photosites are doing real work even when you never select 200MP yourself."
  - q: "Are small pixels limited by physics?"
    a: "By diffraction, eventually. The Airy disk produced by a circular aperture has a diameter of roughly 2.44 × λ × N, so at ƒ/1.4 in 550 nm green light a point source lands as a spot about 1.9 µm across. On the 0.6 µm pixels of an ISOCELL HP2 that spot covers about three pixels in each direction before the lens has made a single error. On a 1.6 µm pixel it covers barely more than one. This is why extra photosites stop buying extra detail well before the sensor runs out of them."
  - q: "Should I turn 200MP mode on permanently?"
    a: "Probably not. Full-resolution files are many times larger, they are slower to capture, and they are taken without the binning that helps in anything short of bright daylight. Switch to it deliberately when you are shooting a static, well-lit subject that you intend to crop into, and leave the phone in its default mode the rest of the time."
products:
  - name: "Samsung ISOCELL HP2"
    url: "https://semiconductor.samsung.com/image-sensor/mobile-image-sensor/isocell-hp2/"
    cta: "Samsung product page"
    note: "The 200MP part described here, with Samsung's own Tetra²pixel and Super QPD descriptions"
  - name: "Apple iPhone 17 Pro"
    url: "https://www.apple.com/iphone-17-pro/specs/"
    cta: "Apple tech specs"
    note: "48MP Fusion Main at ƒ/1.78, with 24MP and 48MP listed as super-high-resolution options"
resources:
  - title: "ISO 12233:2024 — Digital cameras: resolution and spatial frequency responses"
    url: "https://www.iso.org/standard/88626.html"
    note: "Edition 5, ISO/TC 42. The standard that does define how to measure resolving power, unlike the megapixel number"
  - title: "Samsung — ISOCELL HP2 announcement"
    url: "https://news.samsung.com/global/samsung-introduces-the-200-megapixel-image-sensor-for-the-ultimate-high-resolution-experience-in-flagship-smartphones"
    note: "Pixel pitch, optical format and every binning mode, in the manufacturer's own words"
  - title: "Samsung — ISOCELL HP9, GNJ and JN5 announcement"
    url: "https://news.samsung.com/global/samsung-unveils-versatile-image-sensors-for-superior-smartphone-photography"
    note: "Two very different 50MP sensors announced on the same day. Compare the optical formats"
  - title: "DXOMARK — how the Camera score is built"
    url: "https://www.dxomark.com/dxomark-mobile-scores-smartphone-cameras"
    note: "The lab's own description of the test suite, the lux range and what the Texture sub-score covers"
  - title: "DXOMARK — Samsung Galaxy S26 Ultra camera test"
    url: "https://www.dxomark.com/samsung-galaxy-s26-ultra-camera-test/"
    note: "Sub-scores and sample crops for the 200MP camera discussed here"
  - title: "Samsung — mobile image sensor lineup"
    url: "https://semiconductor.samsung.com/image-sensor/mobile-image-sensor/"
    note: "Every current ISOCELL part in one place, so you can check a phone's sensor against its datasheet"
sources:
  - title: "Samsung Introduces the 200-Megapixel Image Sensor for the Ultimate High Resolution Experience in Flagship Smartphones (ISOCELL HP2)"
    url: "https://news.samsung.com/global/samsung-introduces-the-200-megapixel-image-sensor-for-the-ultimate-high-resolution-experience-in-flagship-smartphones"
    publisher: "Samsung Electronics"
    accessed: 2026-08-29
    primary: true
  - title: "Samsung Unveils Versatile Image Sensors for Superior Smartphone Photography (ISOCELL HP9, GNJ, JN5)"
    url: "https://news.samsung.com/global/samsung-unveils-versatile-image-sensors-for-superior-smartphone-photography"
    publisher: "Samsung Electronics"
    accessed: 2026-08-29
    primary: true
  - title: "Samsung Galaxy S26 Ultra Camera test"
    url: "https://www.dxomark.com/samsung-galaxy-s26-ultra-camera-test/"
    publisher: "DXOMARK"
    accessed: 2026-08-29
    primary: true
  - title: "Huawei Pura 80 Ultra Camera test"
    url: "https://www.dxomark.com/huawei-pura-80-ultra-camera-test/"
    publisher: "DXOMARK"
    accessed: 2026-08-29
    primary: true
  - title: "iPhone 17 Pro and 17 Pro Max — Technical Specifications"
    url: "https://www.apple.com/iphone-17-pro/specs/"
    publisher: "Apple"
    accessed: 2026-08-29
    primary: true
  - title: "ISO 12233:2024 — Digital cameras — Resolution and spatial frequency responses"
    url: "https://www.iso.org/standard/88626.html"
    publisher: "International Organization for Standardization"
    accessed: 2026-08-29
    primary: true
  - title: "How DXOMARK scores smartphone rear cameras"
    url: "https://www.dxomark.com/dxomark-mobile-scores-smartphone-cameras"
    publisher: "DXOMARK"
    accessed: 2026-08-29
    primary: true
---

No, not on its own. A 200MP phone hands you a 12.5MP photo by default, because the sensor merges sixteen neighbouring pixels into one before the file is written. Samsung says so in its own announcement of the ISOCELL HP2: the sensor "transforms either into a 1.2μm 50MP or 2.4μm 12.5MP image sensor by binding four to 16 neighboring pixels."

And the highest Photo Main sub-score DXOMARK publishes belongs to a 50MP camera. In DXOMARK's own testing the Huawei Pura 80 Ultra scored 184 there, against 167 for the 200MP Galaxy S26 Ultra. DXOMARK lists the Huawei's main camera as a 50MP 1-inch sensor with 1.6 µm pixels.

> [!KEY]
> Megapixels count photosites. They say nothing about how much light reaches those photosites, which is the quantity that actually decides how a photo looks.

## What does a megapixel number actually measure?

The number of photosites on the sensor. That's the whole definition, and no standards body governs how it's stated.

Compare that with the numbers that do have a document behind them. Resolution — the ability to render fine detail — is covered by ISO 12233, whose current edition 5 was published in September 2024 by ISO/TC 42, the photography committee. It specifies how to measure a digital camera's resolution and its spatial frequency response, which is the contrast the camera retains as detail gets finer. Nothing in it involves counting pixels. A phone maker could double its megapixel figure tomorrow and its ISO 12233 result would barely move, because the lens and the processing would still be doing what they were doing.

This is the same gap SpecWire keeps running into: a number with a certifying body behind it, like the [DisplayHDR tiers a monitor has to be measured against](/displays/displayhdr-tiers-explained/), behaves very differently from a number the marketing department picks.

## Why does a 200MP sensor give you a 12.5MP photo?

Pixel binning. When the sensor is read out, groups of adjacent photosites are summed into one output pixel, so the camera collects light over the combined area but reports it once. Samsung brands its version Tetra²pixel, and the HP2 press release from 17 January 2023 spells out every mode.

| ISOCELL HP2 mode | Output resolution | Effective pixel pitch | What Samsung says it's for |
| --- | --- | --- | --- |
| Native | 200MP | 0.6 µm | Maximum detail, bright light |
| 4-to-1 binned | 50MP | 1.2 µm | 8K video at 30 fps, roughly 33MP per frame |
| 16-to-1 binned | 12.5MP | 2.4 µm | Low light, and 4K 60 fps HDR via Smart-ISO Pro |

Read that middle column backwards and the trick becomes obvious. A 2.4 µm pixel collects sixteen times the light of a 0.6 µm one, because area scales with the square of the pitch. Samsung is selling you a sensor that can be a 12.5MP camera with big pixels or a 200MP camera with tiny ones, and it chooses for you based on the scene.

> [!NOTE]
> Samsung also reports that the HP2's Dual Vertical Transfer Gate raises the pixel's full-well capacity by more than 33 per cent. Full-well capacity is how many electrons a pixel can hold before it clips to white, and it's a far better predictor of highlight behaviour than resolution is.

## Is "50MP" even one thing?

It isn't, and this is where the spec sheet gets genuinely misleading. On 27 June 2024 Samsung announced two 50MP sensors in the same press release.

| Sensor | Resolution | Pixel pitch | Optical format |
| --- | --- | --- | --- |
| ISOCELL HP2 | 200MP | 0.6 µm | 1/1.3 in |
| ISOCELL HP9 | 200MP | 0.56 µm | 1/1.4 in |
| ISOCELL GNJ | 50MP | 1.0 µm | 1/1.57 in |
| ISOCELL JN5 | 50MP | 0.64 µm | 1/2.76 in |

The GNJ and the JN5 carry the same headline figure and are not remotely the same component. One has pixels nearly two and a half times wider than the other, on a much larger die. Samsung positions the JN5 for ultra-wide, front and telephoto duty precisely because its slim optical format fits where a main sensor won't.

So when a phone lists "50MP ultra-wide", that tells you almost nothing until you find the optical format. The megapixel figure survived into 2026 as a marketing number for the same reason "1 ms response time" did on monitors: it's a single digit that goes up, and [the measurement conditions behind it are never printed next to it](/displays/monitor-response-time-1ms-explained/).

## Where does the physics stop cooperating?

At diffraction, and sooner than most spec sheets imply.

Light passing through a circular aperture doesn't converge to a point. It lands as an Airy disk whose diameter, to the first dark ring, is about 2.44 × λ × N, where λ is the wavelength and N the f-number. DXOMARK lists the Galaxy S26 Ultra's main lens at ƒ/1.4. Put 550 nm green light through that and you get 2.44 × 0.55 × 1.4 ≈ 1.9 µm. On the HP2's 0.6 µm pixels, a perfect point in the scene arrives smeared across roughly three pixels in each direction, before the lens has introduced a single aberration of its own.

On the Pura 80 Ultra's 1.6 µm pixels at ƒ/1.6, the same calculation gives about 2.1 µm — a spot barely wider than one pixel. The larger sensor isn't wasting resolution. The smaller one is buying photosites the optics can't feed.

> [!WARNING]
> None of this makes the 200MP sensor bad. The HP2 is physically larger than the GNJ and collects more light overall. It just means the pixel count is the wrong thing to compare, and comparing it will lead you to the wrong phone.

## What did the labs actually measure?

DXOMARK is the one publishing repeatable numbers here, so it's worth knowing what its numbers cover. Its published protocol describes roughly 1,500 images and more than two hours of video per device, shot from 10,000 lux down to 1 lux, with about ten days of engineering time per phone. The Texture sub-score specifically measures preservation of fine surface detail, using charts that DXOMARK says conform to industry standards including CPIQ.

| Phone (DXOMARK's own figures) | Main sensor | Overall Camera | Photo Main |
| --- | --- | --- | --- |
| Huawei Pura 80 Ultra | 50MP, 1 in, 1.6 µm | 175 | 184 |
| Samsung Galaxy S26 Ultra | 200MP, 1/1.3 in, 0.6 µm | 157 | 167 |

DXOMARK scored the Galaxy S26 Ultra's Texture sub-score at 124 and noted that its detail improved over the S25 Ultra, which it attributes to the wider ƒ/1.4 lens rather than to the sensor. That's the pattern across the whole category: the year-on-year gains are coming from optics, stabilisation and processing, while the megapixel figure sits unchanged at 200.

> [!TIP]
> If you want a like-for-like comparison between two phones, find the optical format of each main sensor first. It's the closest single proxy for light-gathering ability, and it's the number manufacturers are least keen to put on the box.

## When is 200MP genuinely worth having?

Two cases, both real.

Cropping is the first. A 200MP frame tolerates a hard crop that would collapse at 12.5MP, which is useful if you shoot wide and reframe later. The second is in-sensor zoom, where the phone reads a central region at full resolution and remosaics it. Samsung says the ISOCELL HP9 offers 2x and 4x in-sensor zoom this way, reaching up to 12x when paired with a 3x telephoto module. And the intermediate 50MP mode exists mostly to feed 8K video, which needs about 33MP per frame.

Those extra photosites are earning their keep. They're just doing it through zoom and video, not through the detail in your ordinary daylight snapshot — a distinction that echoes [how a codec's headline bitrate differs from what the link actually sustains](/audio/does-ldac-actually-sound-better-than-aac/).

> [!ACTION]
> Before you compare two phone cameras on megapixels, check these instead: the main sensor's optical format; its native pixel pitch and the pitch after binning; the maximum aperture; whether stabilisation is optical or sensor-shift; and what a named lab measured, with its light level attached.

Even Apple, which markets aggressively on camera quality, doesn't lead with the count. Its iPhone 17 Pro technical specifications describe the Fusion Main camera as 48MP at ƒ/1.78, and list 48MP capture as a "super-high-resolution" option alongside 24MP rather than as the standard output. The company shipping a 48MP sensor is telling you, in its own spec sheet, that it would rather write you a smaller file.

*Specifications current as of 29 August 2026. Sensor figures from Samsung Electronics press releases dated 17 January 2023 and 27 June 2024; camera scores from DXOMARK's published test results, read 29 August 2026; standard details from the ISO catalogue entry for ISO 12233:2024, edition 5. SpecWire operates no test lab and has not tested any device named here.*
