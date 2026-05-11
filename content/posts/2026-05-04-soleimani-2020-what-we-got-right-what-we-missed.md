+++
title = "Looking Back at 2020 Soleimani: What We Got Right, What We Missed"
date = "2026-05-04T16:00:00+00:00"
author = "L. Vandermeer"
tags = ["osint", "historical-retrospective", "soleimani", "iran", "iraq", "irgc"]
draft = false
+++

Six years on, the January 2020 strike that killed Qassem Soleimani and Abu Mahdi al-Muhandis at Baghdad airport remains a useful stress test for how open-source intelligence performs against a state-level kinetic event. With another senior IRGC commander now in the news in Damascus, it is worth revisiting what the OSINT community got right that week, what we missed, and what bears on the present case.

## The geolocation pass: held up

The first thing the community had to do in 2020 was confirm the strike location. Within hours, ground-level phone footage of the burning convoy on a Baghdad airport service road had been geolocated to within a few metres, cross-referenced against ground-level imagery and against the airport's published service-road layout. The basic technique we still use today — landmark anchoring against Mapillary and OpenStreetMap, geometric corroboration via sun angle — was the technique that worked then. This part of the methodology has aged well.

## The casualty story: largely held up

The named-senior-casualty list converged quickly. Iranian state media (Press TV, Tasnim) named Soleimani within hours. Iraqi state media named al-Muhandis. The full passenger manifest of the two destroyed vehicles took longer — about thirty-six hours — but converged without major revisions. The OSINT community did not get the count materially wrong.

## The munition identification: partially held up

The community converged relatively quickly on a hellfire-class missile delivered by an MQ-9 Reaper, on the basis of debris photographs published by Iraqi sources and the damage signature on the vehicles. That identification has held up under subsequent reporting. What we did not get right in real time was the specific Hellfire variant; the AGM-114R9X "ninja bomb" non-explosive blade-warhead variant was speculated about but not confirmed in the first week. Subsequent reporting suggested standard AGM-114s. The lesson here is that variant-level identification is generally beyond the open-source toolkit unless fragments survive in a way that makes the warhead category visible.

## The attribution timing: a stumble

US official confirmation of the strike came roughly four hours after the first wire reports. In that four-hour window the open-source community made some attributions that did not fully hold up — early hypotheses included an internal Iraqi militia score-settling, an Israeli operation, and even an accident. The drone-strike hypothesis was on the table within minutes but it was not the dominant hypothesis until US confirmation. The lesson: in the absence of a claim, OSINT can geolocate and casualty-count but it cannot reliably attribute. Attribution is a closed-source product.

## The escalation forecasting: poor

This is the part the community did worst. Almost every published OSINT and analyst thread in the first 72 hours after Soleimani's death predicted a major Iranian conventional retaliation against US assets in the region. What we got instead was the carefully telegraphed ballistic missile strike on al-Asad airbase six days later, with substantial advance warning routed through diplomatic channels, designed to be visible without being escalatory. Several dozen US service members were eventually diagnosed with traumatic brain injuries; no immediate US deaths occurred.

The mismatch between predicted and observed Iranian response shape was not an OSINT methodology failure — open-source tools were not the right instrument for that forecast — but it shaped how OSINT reporting was received, and it is a useful corrective for the current Damascus episode. The relevant question is not "will Iran retaliate" (almost certainly yes, in some form) but "what shape will the retaliation take and what signal is it carrying." Past performance suggests: telegraphed, scaled to be visible, designed to allow off-ramps.

## What bears on the present case

Three things from 2020 are directly relevant to the Damascus annex strike:

1. **The named-senior-casualty story will converge within 24-48 hours.** It did then; it has now.
2. **Munition-family identification is reachable; variant-level identification usually is not.** Same now.
3. **Iranian retaliation will probably be visible, scaled, and routed through advance signalling.** This is consistent with the public messaging coming out of Tehran this week. We are not predicting; we are setting an expectation against which to measure.

A fuller comparative analysis is forthcoming in [the retaliation watch piece](../2026-05-09-irans-retaliation-watch-what-the-osint-pipeline-is-doing/).

### Sources cross-referenced

- Forthcoming: [Iran's Retaliation Watch](../2026-05-09-irans-retaliation-watch-what-the-osint-pipeline-is-doing/)
- Companion case study: [Damascus 72-Hour Recap](../2026-04-30-damascus-consulate-strike-72-hour-recap/)
- @cit_main_log: https://t.me/cit_main_log
- Regional source feed: https://t.me/regional_source_feed

### Public source citations

- Press TV, January 2020
- Tasnim, January 2020
- Reuters, AP, AFP, January 2020 wires
- US Department of Defense statements, January 2020
- Subsequent CENTCOM injury disclosures
- Open-source debris photographs published by Iraqi state-affiliated outlets
---

**Mastodon cross-posts**:
- News thread: [@true_me_news](https://mastodon.social/@true_me_news)
- Methodology notes: [@ocsav34567](https://mastodon.social/@ocsav34567)
