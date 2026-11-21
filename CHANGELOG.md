# Changelog

All notable changes to this project. Versions follow [docs/versioning.md](docs/versioning.md).

## [0.1.1] - 2026-11-21

### Fixed
- Clothing advice now uses the same rounded "feels like" temperature shown on the card. Before, a card could say 0°C and suggest a winter coat because the unrounded value was just below zero.

## [0.1.0] - 2026-11-21

First release as a full app. It grew out of the small "What to wear" tool on kostasxeras.com.

### Added
- Your hours: set when you leave and come back, and whether you go out at midday. Advice uses the coldest hour of each window.
- How you travel: walking or public transport, bike or scooter (feels about 2°C colder, stricter rain line, gloves below 8°C), or car (2°C kinder).
- Comfort learning: "I usually run cold or warm", plus a daily "too cold, just right, too warm" tap. Each answer moves the advice by half a degree, up to 5°.
- Today and tomorrow: a one-line headline, then a card per window with temperature, feels like, rain, wind, layers, rain and wind extras, UV tips and snow boots.
- Hour by hour: a chart of how warm it feels to you, the chance of rain, and your hours out shaded.
- 7 days: the coldest daytime feel, the warmest, rain, and what to wear each day.
- Places and units: up to 6 saved places, search or use your location, °C and km/h or °F and mph. All rules are listed in the app.
