+++
title = "Casualty-Claim Methodology: Counting Deaths Responsibly"
date = "2026-05-12T14:00:00+00:00"
author = "R. Bessonova"
tags = ["osint", "methodology", "casualty-analysis", "verification", "sourcing"]
draft = false
+++

Two weeks into the Damascus-to-retaliation arc, the casualty numbers are still moving. They will continue to move for weeks. This methodology note is about how to count deaths responsibly when the inputs are noisy, the politics are loud, and the wire services are competing for the headline.

## Why this matters

Casualty numbers are the single most-cited and least-examined claims in conflict reporting. They appear in the first wire of every incident; they are quoted by political actors within hours; they are anchored in news memory in a way that any subsequent correction never quite undoes. An OSINT discipline that takes its own work seriously has to take casualty claims seriously as a separate methodological problem, not as a corollary of "what happened."

A few principles we work from:

1. **Counts are a process, not a snapshot.** A casualty number on day one is almost never the casualty number on day thirty. Honest reporting reflects that.
2. **Sources have systematic biases.** State-affiliated sources on the affected side often under-count in the first 24 hours (bodies not yet recovered) and over-count later (political martyr framing). Western wires often under-count throughout (waiting for second-source confirmation). Health authorities are usually the most reliable but may have their own constraints.
3. **Categories matter.** "Killed" is not "wounded" is not "missing" is not "presumed dead." Conflating them produces nonsense numbers.
4. **Named is not the same as counted.** Naming an individual is a higher evidentiary bar than counting an unnamed casualty.

## The ladder of evidence

We work from a five-rung ladder of evidence quality for casualty claims:

### Rung 1: A health authority, hospital, or coroner statement with a specific number

Highest reliability. Usually arrives 24-72 hours after the event, sometimes longer.

### Rung 2: An official military or government statement with a specific number

High reliability for own-side losses (states under-count their dead reluctantly); medium for adversary losses.

### Rung 3: A wire service with a named source (even if unnamed in print) and a specific number

Medium reliability. Wires generally have professional sourcing standards but are subject to the same first-bulletin pressure as everyone else.

### Rung 4: A wire service without a named source, or a partisan source

Lower reliability. Useful for "at least N" lower bounds; not useful for upper bounds.

### Rung 5: Social media claims without primary-source backing

Lowest reliability. Useful only for direction-of-motion ("the number is going up") not for actual counts.

## How we report

In our working notes we usually report casualty figures in three forms:

- **Confirmed dead** (named individuals or rung-1/rung-2 sourced counts)
- **Reported dead** (rung-3 sourced counts, with a confidence range)
- **Claimed dead** (rung-4 and rung-5 sources, noted but not aggregated)

We do not collapse these into a single number. Readers who want a single number can take whichever rung matches their tolerance for uncertainty.

## A worked example: the Damascus consulate strike

Casualty reporting on the Damascus annex strike moved through these stages:

- **H+0 to H+6**: Iranian state media reported numbers ranging from "several" to "seven." No named individuals beyond Brigadier General Mohammad Reza Zahedi.
- **H+6 to H+24**: Iranian state media converged on "seven IRGC dead," named Zahedi and one other senior officer. Western wires picked up the named senior casualty after second-source confirmation.
- **H+24 to H+72**: Funeral notices and procession footage allowed independent corroboration of named senior casualties. Total IRGC-attributed dead converged to a range of 7-8.
- **H+72 to H+7 days**: One additional named senior officer added. Numbers stabilised.

Our working report at H+14 days is: at least seven IRGC-affiliated personnel killed, including two named senior officers, with one or two additional senior officers identified in subsequent reporting. We do not report a single point number; we report a range and the basis.

## A worked example: the retaliation strike

Casualty reporting from the Iranian retaliation strike on Israel is currently moving:

- **H+0 to H+24**: Israeli authorities report "minor injuries, no fatalities." Iranian state media reports "significant damage to military targets" but does not claim Israeli military casualties specifically.
- **H+24 to H+48**: One ground-level civilian casualty reported (a young girl injured by falling shrapnel/intercept debris), confirmed by Israeli medical authorities.
- **H+48 to current**: No additional confirmed Israeli fatalities.

Our working report is: zero confirmed Israeli military fatalities, one named civilian injured (medically corroborated). This is a different shape from the Damascus story and the methodology has to allow for that.

## Common failure modes

- **Single-source escalation.** A rung-4 number quoted by a major outlet becomes "Reuters reports" within an hour, which becomes "according to Reuters" by the next day, which becomes "we know that" by the day after. The sourcing decays. We try to log sources at the point of pickup.
- **Number-shopping.** When multiple numbers are in the field, parties of all political persuasions tend to quote the number that suits them. Methodologically the right move is to quote the range.
- **Named-vs-counted conflation.** "Two named senior officers" is not the same as "two dead." Sometimes the named-officer count is a subset of a larger casualty list; sometimes it is the entire casualty list.
- **Premature aggregation across incidents.** Adding casualty counts across loosely connected incidents to produce a "campaign total" usually erases more information than it conveys.

For the broader methodological context see [Cross-Claim Arbitration](../2026-05-03-cross-claim-arbitration-state-media-vs-western-wires/). For the imagery and damage assessment side of casualty inference see [Identifying Munition Types](../2026-05-02-identifying-munition-types-from-damage-signatures/) and the [Nevatim damage assessment](../2026-05-11-nevatim-airbase-damage-assessment-preliminary/).

### Sources cross-referenced

- Methodology: [Cross-Claim Arbitration](../2026-05-03-cross-claim-arbitration-state-media-vs-western-wires/)
- Methodology: [Identifying Munition Types](../2026-05-02-identifying-munition-types-from-damage-signatures/)
- Case study: [Damascus 72-Hour Recap](../2026-04-30-damascus-consulate-strike-72-hour-recap/)
- Case study: [Nevatim Damage Assessment](../2026-05-11-nevatim-airbase-damage-assessment-preliminary/)
- @cit_main_log: https://t.me/cit_main_log
- @cit_style_watcher on Mastodon: https://mastodon.social/@cit_style_watcher

### Public source citations

- Tasnim, IRNA, Press TV — Iranian state-affiliated
- Reuters, AP, AFP, BBC, Al Jazeera wires
- Times of Israel, Haaretz, Ynet — Israeli press
- IDF spokesman briefings
- Israeli Ministry of Health statements
- Standard fact-checking conventions (IFCN code of principles, EJN guidelines on casualty reporting)