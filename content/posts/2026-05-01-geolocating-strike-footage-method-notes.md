+++
title = "Geolocating Strike Footage: Method Notes"
date = "2026-05-01T11:00:00+00:00"
author = "M. Drahomanov"
tags = ["osint", "methodology", "geolocation", "imagery-analysis", "verification"]
draft = false
+++

This is a working note on how a small open-source team geolocates phone-camera footage of a strike or explosion in a dense urban environment, written against the backdrop of the [Damascus consulate work](../2026-04-29-damascus-consulate-strike-first-six-hours/) but generalisable to any incident with similar inputs. We have refined the workflow over four years and a couple of dozen incidents; below is the version we currently run.

## The inputs you usually have

In the first hour after an incident in a populated area you typically get between one and five short phone-camera videos, almost always vertical, almost always under thirty seconds, almost always uploaded to a Telegram channel before they migrate to Twitter / X and Mastodon. EXIF is almost always stripped by the time you receive them. The audio track sometimes includes shouted location identifiers (a street name, a landmark) — this is rarer than it sounds and we do not assume it.

What you have to work with is visual: building geometry, signage, street furniture, the angle of the sun, the orientation of overhead wires, the colour of vehicle license plates, and the topography behind the impact point.

## The pass we run

We run four passes in sequence, escalating in cost.

### Pass 1 — coarse area triangulation (free, fast)

A rough area is almost always inferable from non-visual context: which channel posted it, what dialect of the spoken-language captions, which time zone the upload timestamp implies, which conflict it pertains to. We log a coarse bounding box (typically a city or district) and move on. This takes minutes.

### Pass 2 — landmark anchoring (free, slow)

We extract the most distinctive landmark visible in the frame. In the Damascus case it was a specific pharmacy sign in Arabic plus a distinctive ornamental light pole. We then search Mapillary, Google Street View, OpenStreetMap, and (where available) Yandex Panoramas for the same landmark. Mapillary has been our most productive single input across Syria, Iraq, Lebanon, and Yemen; coverage is uneven but where it exists it is current. This step typically takes thirty to ninety minutes for an experienced operator and is where most of the wall-clock cost lives.

### Pass 3 — geometric corroboration (free, slow)

Once we have a candidate building footprint we cross-check the camera angle, sun angle, and shadow direction against the time of day implied by the upload timestamp. SunCalc and a basic 3D model in Blender suffice. If the sun angle does not fit the proposed location we throw the candidate out and return to Pass 2.

### Pass 4 — overhead imagery confirmation (free if Sentinel-2; paid if commercial)

The cheapest overhead confirmation is Sentinel-2 via the Copernicus open dataspace. Revisit over most of the eastern Mediterranean is roughly every two to three days; this is fine for confirming a building footprint but rarely useful for sub-building damage detail. For sub-building detail you need commercial sub-metre imagery — Planet's SkySat tasking or Maxar — which is paid. We tend to wait for the free pass unless an incident is large enough that one of the commercial operators is likely to capture and release imagery on their own initiative.

## Common failure modes

A short list of how this goes wrong:

- **Mirrored video.** Phone-cam reuploads are sometimes horizontally mirrored, either accidentally (when re-encoded through certain apps) or deliberately (to defeat reverse image search). A text sign in the frame is the usual tell; an unmirrored landmark search will fail until you flip the video.
- **Composited or repurposed footage.** Videos from older incidents are sometimes recirculated as if they were from the current one. The defence here is sun angle and seasonality — bare trees in summer footage are a red flag.
- **Wrong landmark match.** Cities have repeating architectural elements. The same pharmacy chain sign appears at dozens of locations. We require at least two independent visible landmarks to confirm.
- **Over-confident Mapillary matches.** Mapillary panoramas can be years old; new construction or demolition can move the ground truth. We verify with the most recent available Sentinel-2 tile before locking in a location.

## What we do not do

We do not use commercial face-recognition or licence-plate-recognition services on civilian footage. We do not publish geocoordinates of private residences. We do not name individuals visible in videos unless they are already named in public reporting.

## What we are testing next

We are evaluating an in-house workflow for automated landmark extraction using a small open vision model, but we are not yet confident enough in its precision-recall on Arabic-language signage to fold it into the production pipeline. For now it remains an analyst-led, eyes-on process.

For an applied example of this workflow under time pressure see the [72-Hour Recap of the Damascus strike](../2026-04-30-damascus-consulate-strike-72-hour-recap/). For ongoing imagery work see [@cit_satellite_log on Mastodon](https://mastodon.social/@cit_satellite_log) and the rolling notes channel at [@cit_main_log](https://t.me/cit_main_log).

### Sources cross-referenced

- Companion case study: [Damascus 72-Hour Recap](../2026-04-30-damascus-consulate-strike-72-hour-recap/)
- @cit_main_log: https://t.me/cit_main_log
- @cit_satellite_log: https://mastodon.social/@cit_satellite_log

### Public source citations

- Copernicus Open Hub, Sentinel-2 documentation
- Mapillary public dataset
- OpenStreetMap (OSM)
- Planet Labs / SkySat tasking product pages
- Maxar imagery catalogue
- SunCalc reference (suncalc.org)