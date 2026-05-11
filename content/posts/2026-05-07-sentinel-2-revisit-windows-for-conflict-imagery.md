+++
title = "Sentinel-2 Revisit Windows for Conflict Imagery: A Practical Guide"
date = "2026-05-07T09:00:00+00:00"
author = "M. Drahomanov"
tags = ["osint", "methodology", "imagery-analysis", "geolocation"]
draft = false
+++

For OSINT teams without a commercial tasking budget, the European Space Agency's Sentinel-2 constellation is the most important single source of overhead imagery on the planet. It is free, it is well-documented, it has predictable revisit cadence, and the latency from acquisition to public availability is usually under twelve hours. It is also limited in ways that matter, and confusion about those limits is one of the most common methodological errors in junior OSINT work. This note walks through how we plan around Sentinel-2 in practice.

## The constellation, in brief

Sentinel-2 is a two-satellite optical constellation (Sentinel-2A and Sentinel-2B, with Sentinel-2C launched and being commissioned at the time of writing). Each satellite carries a multi-spectral instrument with 13 bands; the highest-resolution bands are 10 metres ground sample distance. The orbit is sun-synchronous at roughly 786 km altitude, with a 290 km swath.

Two satellites means the effective revisit at the equator is about five days; at higher latitudes the overlap of adjacent swaths shortens the revisit further. Over most of the eastern Mediterranean — our area of interest for Iran/Israel/Levant work — the practical revisit is between two and three days, weather permitting. "Weather permitting" is doing real work in that sentence: cloud cover routinely makes a scheduled pass unusable.

## What 10 metres buys you and what it doesn't

A 10-metre ground sample distance is a hard ceiling. It is enough to:

- Confirm the footprint of a destroyed building (typical urban buildings are 15-50 metres across)
- See a crater on an airbase apron once the crater is more than a few metres across
- Track large-scale ground movements (vehicle convoys, construction)
- Detect smoke plumes and active fires

It is not enough to:

- Identify individual vehicles by model
- Count individual people
- Read aircraft tail numbers
- Detect sub-building damage like a single shattered window or a roof collapse over a single room

For sub-building detail you need commercial sub-metre imagery. Sentinel-2 is the workhorse; it is not the microscope.

## Planning the revisit

For a known location and a recent incident, the practical workflow is:

1. **Identify the relevant Sentinel-2 tile.** The MGRS-derived tile naming system (e.g., `36SXC` for parts of Syria) is documented and queryable through the Copernicus Open Hub.
2. **Look up the next scheduled acquisition.** Sentinel acquisition plans are published in advance. We typically check the plan immediately after an incident to know when the next pass is.
3. **Check weather.** ECMWF forecasts and Copernicus Atmosphere Monitoring Service products give a reasonable read on cloud cover for the predicted pass time.
4. **Wait.** This is the hard part. There is no shortcut. For a 2-3 day revisit cycle in the eastern Mediterranean, expect to wait 24-60 hours from incident to first usable imagery.
5. **Process the L2A product.** Use SentinelHub, Copernicus Browser, or the dataspace API. Atmospheric correction is already applied in L2A. Pan-sharpening is not — and is not really useful at 10 metres anyway.

## A worked timeline: Damascus annex strike

For the Damascus consulate annex incident on April 1 (demo anchor 29 April), the planned passes over tile `36SXC` were:

- T+1 day: partially clouded
- T+3 days: clean pass, used for the first impact-location confirmation
- T+5 days: clean pass, used to track debris-clearance progress
- T+8 days: clean pass, used to identify follow-on construction activity

This four-acquisition sequence is roughly typical for an urban incident in the Levant in spring weather. In winter or during dust season the usable-pass rate drops sharply.

## Common failure modes

A short list of things that have caught us out:

- **Tile boundary surprises.** Some sites of interest sit on the boundary between two tiles; the analyst has to remember to query both.
- **Cloud-edge artifacts.** A pass that looks clean in the thumbnail can have edge clouds that obscure the precise area of interest. Always check the actual pixels, not just the cloud-fraction metadata.
- **Shadow vs damage confusion.** At certain solar angles a deep shadow at a building edge can look identical to a damaged roof. Cross-checking the sun-azimuth metadata and looking at adjacent passes resolves this.
- **Mosaic confusion.** Some imagery providers mosaic across multiple acquisition dates, which can make a "current" image actually composite older pixels. We always use the single-pass product for incident work.

## What we use Sentinel-2 alongside

For higher resolution: Planet Labs (PlanetScope at 3 metres, SkySat at 50 cm, both paid). Maxar (sub-metre, paid). For SAR (cloud-penetrating): Sentinel-1, ICEYE (where free samples are released). For thermal: VIIRS via NASA FIRMS for active fire detection at moderate resolution.

For most incident work we lead with Sentinel-2 and pull in commercial sub-metre imagery only where there is a specific question that Sentinel-2 cannot answer — typically sub-building damage on an airbase or industrial site.

For the rolling Sentinel-2 work see [@cit_satellite_log](https://mastodon.social/@cit_satellite_log).

### Sources cross-referenced

- Related methodology: [Geolocating Strike Footage](../2026-05-01-geolocating-strike-footage-method-notes/)
- Applied case: [Damascus 72-Hour Recap](../2026-04-30-damascus-consulate-strike-72-hour-recap/)
- @cit_satellite_log: https://mastodon.social/@cit_satellite_log
- @cit_main_log: https://t.me/cit_main_log

### Public source citations

- European Space Agency, Sentinel-2 User Handbook
- Copernicus Open Hub / Copernicus Dataspace
- ECMWF, Copernicus Atmosphere Monitoring Service
- Planet Labs, Maxar, ICEYE provider documentation
- NASA FIRMS for VIIRS active-fire data