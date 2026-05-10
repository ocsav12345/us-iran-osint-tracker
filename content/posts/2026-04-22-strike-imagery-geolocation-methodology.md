+++
title = "Geolocating Strike Footage: A Five-Step Methodology"
date = 2026-04-22T09:00:00Z
tags = ["osint", "geolocation", "imagery-analysis"]
+++

When strike footage circulates across Telegram and X without an attributed source, the first step is not to verify the claim—it is to verify the location. This note outlines a reproducible methodology for geolocating video and image stills using freely available tools.

## Step 1: Extract still frames

Download the video clip using `youtube-dl` or a similar tool. Frame-by-frame analysis using `ffmpeg` or VLC's screenshot feature generates high-resolution stills. Look for landmarks: road markers, building geometry, utility poles, shadows cast by structures.

## Step 2: Shadow angle analysis

The sun's position depends on date, time, and latitude. Cross-check claimed timestamps against observed shadow angles using [suncalc.org](https://suncalc.org). If a clip claims to be from 14:00 UTC but shadows point east (morning angle), the timestamp is wrong or the location claim is wrong.

## Step 3: Sentinel-2 multispectral matching

The Copernicus Open Access Hub ([https://scihub.copernicus.eu](https://scihub.copernicus.eu)) hosts free Sentinel-2 satellite imagery with 10-meter resolution. Download a multispectral scene from within ±2 weeks of the claimed incident date. Overlay the video landmark against the satellite orthophoto. Building footprints, road networks, and field patterns are often distinctive enough to confirm or exclude a location.

## Step 4: Cross-reference wire service reports

Reuters, AP, and AFP publish geographical metadata in their incident reporting. Search their archives for overlapping date ranges and location clusters. If independent wire reporting contradicts the claimed location, note this as a data point—not a proof of falsehood, but a signal requiring further corroboration.

## Step 5: Document assumption gaps

At each step, state what you cannot verify. Did you have a clear view of the target structure? Was the satellite image from the exact date, or within a week? Did the wire service confirm the location, or only the general region? Transparency about assumption boundaries is the credibility layer that separates analysis from speculation.

---

This methodology is incremental: each step narrows uncertainty rather than settling it. The goal is to move from "we do not know where this is" to "we are confident this is location X, with these remaining caveats." No single tool proves a location; confidence builds through converging evidence.

Further articles in this project will apply this framework to specific incidents circulating across __TG_PRIMARY_URL__ and __MASTO_PRIMARY_URL__, with live worked examples.

