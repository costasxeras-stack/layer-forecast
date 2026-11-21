# 0002: Learn comfort from one tap, with a simple rule

**Status:** accepted, 0.1.0

## Context

People run cold or warm, and one setting is not enough. A model would be hard to explain and needs more data than one tap a day.

## Decision

Each "too cold" or "too warm" moves the advice by half a degree, capped at 5°. "Just right" adds nothing. The settings page says exactly how much it has moved and can reset it.

## Tradeoff

- Anyone can see why the advice changed.
- Learns slowly: about 6 taps to move one clothing band.
- Does not tell apart cold mornings from windy evenings. A later version could learn per window.
