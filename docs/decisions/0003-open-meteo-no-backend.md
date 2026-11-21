# 0003: Use Open-Meteo directly from the browser

**Status:** accepted, 0.1.0

## Context

A weather API with keys needs a server to hide them. That adds cost and a place where locations are logged.

## Decision

The browser calls Open-Meteo, which needs no key, for the forecast and the place search. There is no backend. Settings live in local storage.

## Tradeoff

- Free to run, nothing to maintain.
- The user's location goes to Open-Meteo to get the forecast, and the footer says so.
- Open-Meteo's free tier is for non-commercial use, which fits a portfolio app.
