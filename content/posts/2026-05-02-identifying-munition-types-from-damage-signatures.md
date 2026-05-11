+++
title = "Identifying Munition Types from Damage Signatures"
date = "2026-05-02T10:15:00+00:00"
author = "M. Drahomanov"
tags = ["osint", "methodology", "imagery-analysis", "verification"]
draft = false
+++

When a strike happens and there is no public claim of responsibility, or when the claim is contested, the damage signature itself becomes evidence. This note walks through how we read damage at three scales — the building, the room, and the fragment — to put bounds on what kind of munition was probably involved. As with the [geolocation method note](../2026-05-01-geolocating-strike-footage-method-notes/), the goal is to publish a process that another team could re-run.

## A taxonomy worth memorising

For the kinds of incidents we cover, four broad munition families dominate:

1. **Air-dropped general-purpose bombs** (Mark-80 series and analogues, with or without precision kits like JDAM)
2. **Standoff air-to-surface missiles** (small to medium warhead, precision-guided)
3. **Cruise missiles** (large warhead, very long range, distinctive penetration pattern)
4. **Loitering munitions and small drones** (small warhead, low-fragment, often visible airframe debris)

Each of these leaves a different damage signature. The first job is to narrow to a family.

## The building scale

The building tells you about warhead size and delivery angle.

A **Mark-84-class general-purpose bomb** (about 900 kg) will, on a typical urban building, produce total structural collapse of the targeted floor, severe damage to floors above and below, and a crater that is often visible at street level even after debris clearance. The shockwave will routinely break windows on adjacent buildings hundreds of metres away.

A **small standoff air-to-surface missile** (warhead in the 20-50 kg range) tends to produce surgical damage: a single room or two destroyed, the floor above largely intact, adjacent windows broken but adjacent walls structurally sound. The Damascus consulate annex damage we have been working on falls squarely in this range.

A **cruise missile** like a Tomahawk or a Kh-101 produces a distinctive combination: a penetrating warhead pattern (the munition arrives almost horizontally and burrows before detonating), and a long debris trail along the entry vector that is often visible in overhead imagery.

A **Shahed-136-class loitering munition** has a 30-50 kg warhead but a distinctive low-velocity terminal phase that leaves a more localised damage pattern, often with visible airframe debris (the twin-tail "delta" geometry is unmistakable when it survives).

## The room scale

Inside the affected space, the dispersion of damage tells you about fuze type and detonation height.

Air-burst fuzing produces an overhead-skewed damage pattern: ceilings down, furniture flung outward and downward, characteristic walls peppered with downward-angled fragmentation. Point-detonating fuzing produces a more spherical pattern centred on the impact point. Delayed-fuze (penetrator) detonations strip the lower walls and shred floors but often leave the ceiling above relatively intact.

## The fragment scale

Where fragments are recoverable and photographed, you can sometimes get a positive identification of the munition. The most diagnostic items are:

- **Tail-section serial numbers and markings** — Western-origin precision munitions usually carry stencilled markings that are partially recoverable even from blown fragments. The Yemen and Syria reporting catalogues built by other teams over the past decade are an indispensable cross-reference here.
- **Distinctive fin or canard geometries** — small standoff missiles in different families have characteristic cropped-delta or cruciform fins. Even a partial fin section is often diagnostic.
- **Seeker-head domes** — surviving seeker glass and the diameter of the dome aperture narrow the family of munitions sharply.

We have a working internal corpus of about three hundred annotated fragment photos covering munitions used in Syria, Yemen, Iraq, and Ukraine. It is not yet public; we are working through the disclosure risk.

## Failure modes

A short list of how this analysis goes wrong:

- **Mixed-munition strikes.** When two munitions hit the same target within seconds, the damage signatures add and become hard to separate. The defence here is timing: the seismic record (where local stations exist) and overlapping video audio tracks sometimes resolve a two-bang signature.
- **Munition staging.** Some munitions, particularly loitering munitions, have airframe fragments that are deliberately structurally similar to other systems. Positive identification requires the warhead pattern plus the airframe debris, not just the airframe.
- **Cover stories.** Where a state has reason to misattribute a strike to a different munition family, debris can be planted or removed before independent inspection. This is rare but not unheard of.

## Applied to Damascus

Our working assessment of the Damascus annex strike is that the damage pattern — single-room destruction, adjacent walls intact, floor above largely preserved, no visible airframe debris consistent with a loitering munition, no visible cruise-missile entry vector — fits the standoff air-to-surface missile family. We are not naming a specific munition publicly; we do not have a high-confidence fragment match. Other groups have proposed candidates; we are not yet ready to converge with them in public.

### Sources cross-referenced

- Related methodology: [Geolocating Strike Footage](../2026-05-01-geolocating-strike-footage-method-notes/)
- Companion case study: [Damascus 72-Hour Recap](../2026-04-30-damascus-consulate-strike-72-hour-recap/)
- @cit_main_log working notes: https://t.me/cit_main_log
- Style watcher feed: https://mastodon.social/@true_me_news

### Public source citations

- ARES (Armament Research Services) public catalogue
- Bellingcat munition identification posts (general reference)
- UN Group of Experts on Yemen reports (munition fragment annexes)
- Open-source seismic networks (IRIS, ORFEUS) where local stations resolve