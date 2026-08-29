---
title: "Does LDAC actually sound better than AAC?"
slug: does-ldac-actually-sound-better-than-aac
seo_title: "LDAC vs AAC: What's Verified"
meta: "Sony rates LDAC at 990kbps but phones pick 330 or 660. Here is what the AOSP code, Sony's own spec and SoundGuys' measurements actually say."
category: audio
date: 2026-08-28
updated: 2026-08-28
description: "LDAC's headline number is roughly three times AAC's. Whether you ever receive that number depends on a bitrate your phone chooses silently, and never tells you about."
image_alt: "Bar chart comparing measured high-frequency roll-off in kilohertz for AAC on four phones against LDAC's three bitrate settings"
tags: [LDAC, AAC, Bluetooth codecs, A2DP, Sony, AOSP, bitrate, wireless audio]
about: ["Sony", "LDAC", "AAC", "Bluetooth SIG", "Android Open Source Project", "Advanced Audio Distribution Profile"]
hero: chart
chart:
  type: bar
  title: "Measured high-frequency roll-off — the point where the codec stops sending"
  y_label: "Roll-off frequency (kHz)"
  source: "Measurements by Robert Triggs for SoundGuys; LDAC figures in Hi-Res mode. Read 28 August 2026"
  series:
    - label: "Roll-off (kHz)"
      points:
        - ["AAC, Huawei P20 Pro", 14.2]
        - ["AAC, LG V30", 16]
        - ["AAC, Galaxy Note 8", 17]
        - ["AAC, iPhone 7", 18.9]
        - ["LDAC 330kbps", 18]
        - ["LDAC 660kbps", 30]
        - ["LDAC 990kbps", 47]
key_takeaways:
  - text: "Sony's LDAC developer documentation states a maximum bitrate of **990 kbps**, and that best-effort mode switches automatically among **330, 660 and 990 kbps** depending on link conditions. The Hi-Res Audio Wireless logo is satisfied only at 990 kbps."
    source: 1
  - text: "SoundGuys measured which rate six phones actually chose at arm's length: only **1 of 6** picked 990 kbps. Three picked 660 kbps and two were stuck at **330 kbps** — the setting SoundGuys found worse than SBC."
    source: 3
  - text: "In Android's own source tree, AAC and SBC are first-class A2DP codecs while LDAC sits in the vendor-specific path as `a2dp_vendor_ldac.cc`. AOSP's default codec priority ranks LDAC at **5001** against AAC's **2001**, so LDAC wins negotiation whenever both ends support it."
    source: 2
  - text: "SoundGuys measured AAC's high-frequency roll-off across four phones and got **14.2 kHz** on the Huawei P20 Pro against **18.9 kHz** on the iPhone 7 — a **4.7 kHz** spread from one codec, because the encoder runs on the phone's CPU under its power-management policy."
    source: 3
  - text: "A CD-rate stereo stream is **1,411 kbps** of PCM, so even LDAC's top **990 kbps** discards roughly a third of the data. SoundGuys states plainly that LDAC cannot be considered lossless."
    source: [1, 3]
  - text: "All of these measurements were taken on **2018** hardware, and SoundGuys flags both pages as dated — its AAC piece, last updated **17 June 2025**, says it is improbable that modern phones still show these problems. No newer measurement set of comparable depth has been published."
    source: [3, 4]
faq:
  - q: "Is LDAC better than AAC?"
    a: "On paper, comfortably. Sony's own documentation puts LDAC's ceiling at 990 kbps against AAC's roughly 250-264 kbps over Bluetooth. In practice the answer depends entirely on which LDAC bitrate your phone negotiates. SoundGuys' measurements found LDAC at 990 and 660 kbps clearly ahead of every AAC implementation they tested, but LDAC at 330 kbps worse than both AAC on an iPhone and plain SBC. Since 330 kbps is what a weak link falls back to, LDAC is better than AAC only when the connection is good."
  - q: "Which LDAC bitrate does my phone use?"
    a: "You cannot tell from the Bluetooth settings screen. Android exposes the choice under Developer options, in a setting called LDAC playback quality, where best effort is the default. Enable Developer options, connect the headphones, then look for the LDAC codec entry. If you never enable Developer options, the phone silently picks 330, 660 or 990 kbps and never tells you which."
  - q: "Does the iPhone support LDAC?"
    a: "No. SoundGuys states that Apple devices do not support LDAC and use SBC and AAC instead. That is not a small omission, because AAC is the codec Apple has optimised hardest — SoundGuys measured the iPhone 7 as the best AAC implementation in its test group by a clear margin. On an iPhone, the LDAC question does not arise; the codec is simply unavailable."
  - q: "Why does AAC sound different on different Android phones?"
    a: "Because AAC's encoder runs on the phone's application processor, and how much CPU it gets is a scheduling decision. SoundGuys attributes the variation to Android's Energy Aware Scheduling, which weighs clock speed against battery life and can assign Bluetooth encoding a low priority. The same headphones fed by two different phones over the same codec produced measurably different frequency response in their tests — a 4.7 kHz spread in roll-off across four devices."
  - q: "Is LDAC at 990 kbps lossless?"
    a: "No. A 16-bit, 44.1 kHz stereo stream is 2 x 16 x 44,100 = 1,411 kbps, so LDAC's 990 kbps ceiling has to throw away about a third of it before transmission. Sony markets LDAC as Hi-Res Audio Wireless, which is a logo requirement about frequency capability at 990 kbps, not a claim of bit-perfect transmission. Bit-perfect over classic Bluetooth A2DP is not currently on offer at CD rate."
  - q: "Should I force 990 kbps in Developer options?"
    a: "Only if your listening position keeps the radio link strong. SoundGuys measured that most codecs — SBC, AAC and LDAC 330 — only start dropping packets around -80 dBm RSSI, while LDAC at 990 kbps risks stuttering just below -60 dBm. They measured the Sony WH-1000XM3 averaging about -49 dBm worn normally, with dips towards -60 dBm when a hand or arm blocked the path. That is enough headroom to try 990, and not enough to guarantee it."
  - q: "Does any of this matter if I mostly listen on the train?"
    a: "Probably not much. On a commute your link is crowded, your ears are working against 70-plus dB of ambient noise, and the codec will spend its time at the bottom of its range regardless of what you selected. The measured differences between codecs are largest above 15 kHz and in the noise floor — exactly the regions ambient noise buries first. Codec choice matters most sitting still in a quiet room."
products:
  - name: "LDAC — Sony's developer documentation"
    url: "https://www.sony.co.jp/en/Products/LDAC/"
    cta: "Sony's own page"
    note: "The 990/660/330 kbps figures and the best-effort description, straight from the licensor"
  - name: "Advanced Audio Distribution Profile 1.4 — Bluetooth SIG"
    url: "https://www.bluetooth.com/specifications/specs/advanced-audio-distribution-profile-1-4/"
    cta: "Specification page"
    note: "The adopted profile every one of these codecs rides on, with its SBC and AAC conformance files"
resources:
  - title: "Sony — LDAC developer site"
    url: "https://www.sony.co.jp/en/Products/LDAC/"
    note: "Sony's stated bitrates, the best-effort behaviour, and the Hi-Res Audio Wireless condition"
  - title: "AOSP — Bluetooth services, advanced audio codecs"
    url: "https://source.android.com/docs/core/connect/bluetooth/services"
    note: "The default a2dp_source_codec_priority values that decide which codec wins negotiation"
  - title: "AOSP — A2DP codec source tree"
    url: "https://android.googlesource.com/platform/packages/modules/Bluetooth/+/refs/heads/main/system/stack/a2dp/"
    note: "See for yourself which codecs are first-class and which are a2dp_vendor_*"
  - title: "SoundGuys — LDAC measured"
    url: "https://www.soundguys.com/ldac-ultimate-bluetooth-guide-20026/"
    note: "Frequency response, noise floor and per-phone best-effort defaults, with the outlet's own age warning"
  - title: "SoundGuys — AAC measured"
    url: "https://www.soundguys.com/the-ultimate-guide-to-bluetooth-headphones-aac-20296/"
    note: "The per-device AAC roll-off and noise floor numbers, including why Android varied"
  - title: "Bluetooth SIG — Advanced Audio Distribution Profile 1.4"
    url: "https://www.bluetooth.com/specifications/specs/advanced-audio-distribution-profile-1-4/"
    note: "The adopted profile, its errata requirement, and the SBC and AAC conformance test files"
sources:
  - title: "LDAC developer site — features, bitrates and best-effort mode"
    url: "https://www.sony.co.jp/en/Products/LDAC/"
    publisher: "Sony Corporation"
    accessed: 2026-08-28
    primary: true
  - title: "Bluetooth services — advanced audio codecs and codec priority"
    url: "https://source.android.com/docs/core/connect/bluetooth/services"
    publisher: "Android Open Source Project"
    accessed: 2026-08-28
    primary: true
  - title: "The ultimate guide to Bluetooth headphones: LDAC isn't Hi-res"
    url: "https://www.soundguys.com/ldac-ultimate-bluetooth-guide-20026/"
    publisher: "SoundGuys"
    accessed: 2026-08-28
    primary: true
  - title: "The ultimate guide to Bluetooth headphones: AAC only acceptable on Apple phones"
    url: "https://www.soundguys.com/the-ultimate-guide-to-bluetooth-headphones-aac-20296/"
    publisher: "SoundGuys"
    accessed: 2026-08-28
    primary: true
  - title: "Advanced Audio Distribution Profile 1.4"
    url: "https://www.bluetooth.com/specifications/specs/advanced-audio-distribution-profile-1-4/"
    publisher: "Bluetooth SIG"
    accessed: 2026-08-28
    primary: true
  - title: "A2DP codec implementations in the Android Bluetooth stack"
    url: "https://android.googlesource.com/platform/packages/modules/Bluetooth/+/refs/heads/main/system/stack/a2dp/"
    publisher: "Android Open Source Project"
    accessed: 2026-08-28
    primary: true
---

Usually, yes — but only when your phone is running LDAC at 660 or 990 kbps, and it often isn't. Sony's own documentation rates LDAC at a maximum of 990 kbps and says a best-effort mode picks silently among 330, 660 and 990 kbps based on link conditions. When SoundGuys checked which rate six phones actually chose sitting an arm's length from the headphones, only one picked 990 kbps and two were stuck at 330 kbps — a setting the same lab measured as worse than ordinary SBC. AAC's ceiling over Bluetooth sits around 250 kbps. So LDAC's advantage is real, large, and entirely conditional on a number nothing in your phone's interface displays.

## What is LDAC actually specified to do?

Sony's LDAC developer site is the primary document, and it is refreshingly specific. It states LDAC transmits "at the maximum bitrate of 990kbps", that best-effort mode "controls bitrate automatically depending on the network condition", and that the rate "automatically changes among 330kbps/660kbps/990kbps". Sony's own comparison baseline is Bluetooth A2DP SBC at 328 kbps, 44.1 kHz — which is where the marketing line about three times the data comes from.

One footnote on that page does most of the work: LDAC "satisfies the requirement of Hi-Res Audio Wireless logo at the transfer rate of 990 kbps". Not at 660. Not at 330. The badge on the box describes a mode your phone may never select.

> [!KEY]
> Sony specifies exactly three LDAC bitrates — 330, 660 and 990 kbps — and grants the Hi-Res Audio Wireless logo only at the top one. Everything below is unbadged.

AAC has no equivalent single number, and that is the honest answer rather than an evasion. Over Bluetooth, AAC's rate is negotiated against the link's MTU and then encoded on the phone's CPU. You can watch this happen in the Android source: the AAC encoder sets its bitrate to the smaller of the configured value and a peak computed from the MTU, then hands the job to a software encoder. The number is an outcome, not a specification.

## Why does the same codec sound different on two phones?

Because the encoder is software running on a processor that has other priorities. SoundGuys measured AAC's high-frequency roll-off across four phones and found the Huawei P20 Pro cutting off at 14.2 kHz, the LG V30 at 16 kHz, the Samsung Galaxy Note 8 at 17 kHz, and the iPhone 7 reaching 18.9 kHz. Same codec, same test rig, 4.7 kHz of spread.

SoundGuys attributes the gap to Android's Energy Aware Scheduling, which decides how much CPU a task gets, and notes that AAC "requires much more processing power than SBC or aptX". A phone tuned aggressively for battery life gives the encoder less headroom, and the encoder responds by throwing away more.

| Codec and device | Measured roll-off | Noise floor at 1 kHz | Who measured it |
| --- | --- | --- | --- |
| AAC, Huawei P20 Pro | 14.2 kHz | peaks near -42 dB | SoundGuys |
| AAC, LG V30 | 16 kHz | not published | SoundGuys |
| AAC, Galaxy Note 8 | 17 kHz | about -73 dB | SoundGuys |
| AAC, iPhone 7 | 18.9 kHz | -91 dBFS | SoundGuys |
| LDAC 330 kbps | just under 18 kHz | -80 dB in the 1-5 kHz band | SoundGuys |
| LDAC 660 kbps | 30 kHz (Hi-Res mode) | about -110 dB at 2 kHz | SoundGuys |
| LDAC 990 kbps | 47 kHz (Hi-Res mode) | about -116 dB to 15 kHz | SoundGuys |

SpecWire has not tested any of this. Every number above was measured by Robert Triggs for SoundGuys, and every one of them comes with a caveat we will get to.

LDAC does not have this problem to nearly the same degree, and the reason is structural rather than clever: its three rates are discrete and declared, so a weak phone drops a step rather than quietly degrading inside one. You lose quality either way. With LDAC you can at least name which step you are on.

## Which codec does your phone actually pick?

Android decides by priority, and the defaults are in the open. AOSP's `config.xml` ships `a2dp_source_codec_priority_ldac` at 5001, aptX HD at 4001, aptX at 3001, AAC at 2001 and SBC at 1001, with the note that a larger value means higher priority. Both ends must support a codec for it to be selected, but where a phone and a headset both speak LDAC and AAC, stock Android takes LDAC without asking.

There is a second structural detail worth seeing. In Android's Bluetooth stack, SBC and AAC live in `a2dp_sbc.cc` and `a2dp_aac.cc`, while LDAC, aptX and Opus sit in files prefixed `a2dp_vendor_`. That prefix is the whole story: the Bluetooth SIG's Advanced Audio Distribution Profile 1.4 — the adopted revision, whose published document set includes SBC bitstreams and AAC conformance test files — defines SBC and AAC directly. LDAC rides A2DP's vendor-specific codec slot. It is a guest on the standard, not part of it.

> [!WARNING]
> "Supports LDAC" on a spec sheet tells you the codec can be negotiated. It says nothing about which of the three bitrates you will get, and that is the variable that decides whether LDAC beats AAC or loses to SBC.

## When is LDAC worse than AAC?

At 330 kbps, on SoundGuys' measurements, and it is not close. They recorded LDAC 330's noise floor at around -80 dB between 1 and 5 kHz, rising to a peak of -35 dB at 15 kHz, and described it as "by far the worst high-frequency performance I have seen from any Bluetooth codec". Its roll-off lands just before 18 kHz, below plain SBC.

Now look at what pushes a link down to 330 kbps. SoundGuys plotted dropped audio against signal strength and found most codecs — SBC, AAC, LDAC 330 — holding until roughly -80 dBm RSSI, while LDAC at 990 kbps risks stuttering just below -60 dBm. They measured Sony's own WH-1000XM3 averaging about -49 dBm worn normally, dipping towards -60 dBm when an arm or a hand got in the way. Sony's flagship headphones on Sony's own codec sit close enough to the cliff that a hand in a pocket can push them over.

> [!TIP]
> If you want 990 or 660 kbps, you have to ask for it. Turn on Developer options, connect the headphones, and set LDAC playback quality explicitly rather than leaving it on best effort. Then keep the phone on the same side of your body as the headset.

## How much of this is still true in 2026?

Less than the numbers suggest, and SoundGuys says so themselves — which is the main reason to trust them. Their LDAC page carries a banner reading "Hold up! This article is quite old" and describes itself as "more of a snapshot into history than always-current information". The AAC page goes further: it calls the poor Android results "improbable" on modern silicon, and points out that several of the worst-performing brands have since left the market entirely.

So treat the per-phone AAC numbers as evidence that phone-side encoding *can* vary badly, not as a current ranking of phones you can buy. The LG V30 and Huawei P20 Pro are museum pieces.

What has not aged is the structure. Sony still specifies three bitrates and still grants the logo at one of them. Android still defaults LDAC to best effort. The link budget that makes 990 kbps fragile is a property of classic Bluetooth's radio, not of 2018 silicon. And nobody has published a measurement set of comparable depth on current hardware — which is itself the finding. If you want a 2026 answer to "does LDAC beat AAC on a Pixel 10", the honest response is that no lab has published one.

> [!NOTE]
> This is the same shape of problem as [a monitor quoting 1 ms without naming the transition it was measured on](/displays/monitor-response-time-1ms-explained/), [two phones both wearing an IP68 badge at depths four times apart](/phones/ip68-rating-explained/), or [a 120W charging figure that only applies while the battery is nearly empty](/phones/120w-fast-charging-minute-by-minute/). The headline figure is genuine. The condition attached to it is what decides whether you ever see it.

## So what should you actually do?

Three things, in descending order of how much difference they make.

Fix the link before you fix the codec. Everything above says the bitrate follows the radio, so pocket position, body blocking and Wi-Fi congestion move the needle further than any menu setting. If you are on iOS the decision is made for you anyway: SoundGuys reports that Apple devices do not support LDAC, and Apple's AAC implementation was the strongest in their test group.

Then, if you are on Android with LDAC headphones and you listen somewhere quiet, go into Developer options and pin the rate rather than accepting best effort. Choosing 660 kbps is the defensible middle — SoundGuys measured its CD-mode noise floor at around -112 dB, roughly what a properly dithered CD gives you, with meaningfully more stability headroom than 990.

And be clear about the ceiling. A CD-rate stereo stream is 1,411 kbps of PCM. LDAC's best is 990. Roughly a third of the data is gone before it leaves your phone, which is why SoundGuys concludes LDAC "cannot be considered lossless, although it is the closest you can currently get over a Bluetooth connection". Sony has never claimed otherwise in the specification — only in the logo.

> [!ACTION]
> Before you buy on the strength of a codec badge: confirm both the phone and the headphones list the codec; enable Developer options and check which bitrate is actually negotiated where you listen; and if you are on iOS, ignore LDAC entirely and buy for the AAC implementation instead.

*Specifications current as of 28 August 2026. Sony's LDAC developer documentation, the AOSP Bluetooth services documentation and A2DP source tree (tree 3f96ee4), and the Bluetooth SIG's Advanced Audio Distribution Profile 1.4 page were read on that date. All measured values are attributed to SoundGuys, whose LDAC page was last updated 1 October 2025 and whose AAC page was last updated 17 June 2025; both carry the outlet's own warning that the underlying tests were run on 2018 hardware.*
