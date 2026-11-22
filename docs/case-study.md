# Case study: Layer Forecast

## The problem

Weather apps show the day's high and low. Nobody is outside at the high. People are outside on the way to work and on the way back, and they feel the cold differently. This app looks only at the hours you are out, adjusts for how you travel, and learns your comfort from one tap a day.

## From a small tool to an app

Version 0 was a one-screen tool on my portfolio site, picked because it was quick to build. It worked, but it only stored data. For 0.1.0 I asked what a user would need to come back every week, and what the app should show them that they could not see before. The answer shaped three decisions.

## Decisions

### 1. Advise on the coldest hour you are out, not the day's range

Daily high and low describe the weather, not the person. A 14°C afternoon says nothing about a 7:30 walk at 3°C.

**Decision:** Advice uses the hours around leaving and coming back (and midday if set), and dresses for the coldest of them. The headline adds a "layers you can take off" line when windows differ by 8°C or more.

Full record: [docs/decisions/0001-coldest-hour-you-are-out.md](decisions/0001-coldest-hour-you-are-out.md)

### 2. Learn comfort from one tap, with a simple rule

People run cold or warm, and one setting is not enough. A model would be hard to explain and needs more data than one tap a day.

**Decision:** Each "too cold" or "too warm" moves the advice by half a degree, capped at 5°. "Just right" adds nothing. The settings page says exactly how much it has moved and can reset it.

Full record: [docs/decisions/0002-simple-learning-from-one-tap.md](decisions/0002-simple-learning-from-one-tap.md)

### 3. Use Open-Meteo directly from the browser

A weather API with keys needs a server to hide them. That adds cost and a place where locations are logged.

**Decision:** The browser calls Open-Meteo, which needs no key, for the forecast and the place search. There is no backend. Settings live in local storage.

Full record: [docs/decisions/0003-open-meteo-no-backend.md](decisions/0003-open-meteo-no-backend.md)

## What it does now

- **Your hours:** set when you leave and come back, and whether you go out at midday. Advice uses the coldest hour of each window.
- **How you travel:** walking or public transport, bike or scooter (feels about 2°C colder, stricter rain line, gloves below 8°C), or car (2°C kinder).
- **Comfort learning:** "I usually run cold or warm", plus a daily "too cold, just right, too warm" tap. Each answer moves the advice by half a degree, up to 5°.
- **Today and tomorrow:** a one-line headline, then a card per window with temperature, feels like, rain, wind, layers, rain and wind extras, UV tips and snow boots.
- **Hour by hour:** a chart of how warm it feels to you, the chance of rain, and your hours out shaded.
- **7 days:** the coldest daytime feel, the warmest, rain, and what to wear each day.
- **Places and units:** up to 6 saved places, search or use your location, °C and km/h or °F and mph. All rules are listed in the app.

## What I would measure

There is no usage data yet, so there are no findings. These are hypotheses to test with real users.

| Measure | Definition | Target |
|---|---|---|
| Comfort | Share of daily answers that are "just right" after 2 weeks of use | [x]% |
| Return use | Share of users who open it on at least 4 mornings a week | [x]% |
| Learning | Days until answers settle on "just right" | [x] days |

## What I would do next

1. Learn comfort separately for mornings and evenings
2. A morning notification with the headline
3. Children's profiles with their own comfort setting

## My role

I defined the problem, the users, the features and the decisions, and tested every flow on desktop and phone widths.
