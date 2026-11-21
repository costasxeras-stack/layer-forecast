# 0001: Advise on the coldest hour you are out, not the day's range

**Status:** accepted, 0.1.0

## Context

Daily high and low describe the weather, not the person. A 14°C afternoon says nothing about a 7:30 walk at 3°C.

## Decision

Advice uses the hours around leaving and coming back (and midday if set), and dresses for the coldest of them. The headline adds a "layers you can take off" line when windows differ by 8°C or more.

## Tradeoff

- Matches what people actually feel.
- Needs two times from the user. Sensible defaults (08:00 and 17:30) make it work on first open.
- Days with many trips are simplified to two or three windows.
