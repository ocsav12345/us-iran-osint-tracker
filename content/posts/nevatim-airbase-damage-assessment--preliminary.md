+++
title = "Nevatim Airbase Damage Assessment — Preliminary"
date = "2026-05-11T15:45:00+00:00"
author = "A. Kovacs"
tags = ["osint", "imagery-analysis", "nevatim", "israel", "iran", "geolocation"]
draft = false
+++

The first usable post-strike Sentinel-2 pass over Nevatim Airbase came down at roughly 09:30 UTC this morning. This is a preliminary damage assessment based on that pass plus three ground-level photographs published overnight via Israeli civilian accounts. Better imagery will follow; this post will be updated.

## Pre-strike baseline

We have been maintaining a working baseline of Nevatim over the past several weeks as part of [the retaliation watch](../2026-05-09-irans-retaliation-watch-what-the-osint-pipeline-is-doing/). The baseline is built from approximately ten Sentinel-2 passes since mid-April and three publicly-released commercial sub-metre images. It identifies:

- The main runway (08/26 orientation, approximately 3,600 metres long)
- The secondary runway (parallel, slightly shorter)
- Two main aircraft apron groupings
- A hardened aircraft shelter cluster on the northwest side of the field
- Fuel storage on the southwest corner
- Munition storage to the south of the main apron
- Administrative buildings and quarters to the east

This is the standard pre-strike workup for any defended airbase. Doing it before the event matters because in the post-strike work you want to be reading deltas against a known baseline, not building the baseline and the assessment simultaneously.

## What this morning's Sentinel-2 pass shows

At 10-metre resolution we can resolve:

- **Main runway**: visible scarring at two points, approximately 800 metres apart. The scarring is consistent with point-source impacts roughly 5-10 metres across; the runway is not severed. Pavement repair crater visible at one of the two scars in the imagery, suggesting active repair within hours of impact.
- **Apron area**: a single damage point visible on the southern apron, near but not on an aircraft parking position visible in the pre-strike baseline.
- **Hardened shelter cluster**: no visible damage at 10-metre resolution. Sub-shelter damage cannot be ruled out at this resolution.
- **Fuel storage**: no visible damage.
- **Munition storage**: no visible damage.

This is consistent with a "limited and precise" Iranian framing of the operation, with the caveat that "limited" and "precise" do not necessarily mean "ineffective." Hits on a runway disrupt operations; hits on apron disrupt operations; the operational disruption is real even if the absolute damage is modest.

## What the ground-level photographs show

Three photographs published overnight on Israeli civilian social-media accounts (since pulled in some cases, mirrored elsewhere) show:

1. A crater on what appears to be the main runway, with paving repair material visible. Geolocation of this image against the runway markings confirms the location matches one of the Sentinel-2 scars.
2. A view of the hardened shelter cluster from a distance, showing one shelter with what may be minor exterior damage. We are not confident in this read at the available image resolution.
3. A general view of the airbase taken from elevated ground to the southwest, showing visible smoke plumes from two locations consistent with the Sentinel-2 damage points.

We have geolocated photographs 1 and 3 with high confidence; we have geolocated photograph 2 with medium confidence.

## What we have not seen

We have not seen:

- Damage to aircraft. The Sentinel-2 resolution does not let us count F-35 or F-15 airframes on the apron; commercial sub-metre imagery will be needed for that.
- Damage to munition storage.
- Damage to fuel storage.
- Damage to administrative or quarters areas.

This is a strong preliminary statement against the broadest claims of either side. The Iranian operation hit the airbase; it did not destroy the airbase. The Israeli operation maintained the airbase as operational; it did not prevent every impact.

## What we are watching for next

- **First commercial sub-metre imagery.** Planet SkySat or Maxar tasking is the next step. We expect publicly-released imagery within the next 24-72 hours.
- **Israeli statements about specific damage.** The IDF spokesman has so far described damage as "minor." We will compare the language against what the imagery shows over the coming days.
- **Iranian statements about specific damage.** State media has so far described "significant damage to the airbase." We will compare those claims against what the imagery shows.
- **Fragment photographs.** Munition fragments recovered at impact points will tell us which Iranian ballistic systems performed and which did not.

For methodological context see [Identifying Munition Types](../2026-05-02-identifying-munition-types-from-damage-signatures/) and [Sentinel-2 Revisit Windows](../2026-05-07-sentinel-2-revisit-windows-for-conflict-imagery/). For the broader retaliation narrative see [The 99% Intercept Claim](../2026-05-10-the-99-percent-intercept-claim-what-the-numbers-mean/) and the [Aramco supply-chain retrospective](../2026-05-06-aramco-2019-supply-chain-lessons-for-air-defense/).

### Sources cross-referenced

- Companion case: [The 99% Intercept Claim](../2026-05-10-the-99-percent-intercept-claim-what-the-numbers-mean/)
- Methodology: [Identifying Munition Types](../2026-05-02-identifying-munition-types-from-damage-signatures/)
- Methodology: [Sentinel-2 Revisit Windows](../2026-05-07-sentinel-2-revisit-windows-for-conflict-imagery/)
- Historical: [Aramco 2019](../2026-05-06-aramco-2019-supply-chain-lessons-for-air-defense/)
- @cit_satellite_log: https://mastodon.social/@cit_satellite_log
- @cit_main_log: https://t.me/cit_main_log

### Public source citations

- Sentinel-2 tile covering Nevatim, Copernicus Open Hub
- IDF spokesman briefings, 14 April 2024 (anchor date)
- Tasnim, IRNA — Iranian state-affiliated
- Reuters, AP, BBC wires
- Times of Israel, Haaretz — Israeli press
- Civilian Israeli social-media posts (cited generically; not amplified by URL)