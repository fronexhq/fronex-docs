---
description: Host-city weather, hurricane season, and live climate markets tied to the FIFA World Cup 2026.
---

# Climate markets

Climate is the smallest of the data-driven pillars, but it's tightly themed to the FIFA World Cup 2026 — every market is tied to either a host city or the 2026 Atlantic hurricane season.

## Market types

### Host-city weather

The FIFA World Cup 2026 is played across **16 host cities** in the USA, Canada, and Mexico. Every match-day spawns weather markets keyed to that city's kickoff time:

* **High temperature in Mexico City on match day?** — bucketed
* **Rain at kickoff in Toronto?** — yes/no
* **Wind speed exceeds 25 km/h at full-time in Vancouver?** — yes/no

These markets resolve from **Open-Meteo** (free, oracle-friendly weather feed) for the official station nearest the venue.

### Heatwave markets

Specific marquee markets for high-stakes weather days:

* **Mexico City exceeds 35°C on the day of its match?**
* **Vancouver or Toronto records 30°C+ during the tournament?**

These matter — heat is a real factor in match outcomes, and these markets often correlate with adjacent soccer match-window markets.

### Hurricane markets

The Atlantic hurricane season runs **June 1 – November 30**, overlapping the entire FIFA World Cup 2026. Live markets:

* **Does an Atlantic system reach Category 3 by [date]?**
* **Total named storms by July 19?** — bucketed
* **Does a tropical system affect a coastal host city's match?**

Resolution comes from **NOAA NHC** (the National Hurricane Center's public advisory feed).

## Resolution

* **Primary oracle for weather**: Open-Meteo (free, station-accurate, daily refresh)
* **Hurricane data**: NOAA NHC public feed
* **No backup oracle for climate** — each climate market type has a single data source. If that source is delayed or looks wrong, the market enters **pending resolution** and we resolve it manually within 24 hours (see [Making predictions › overview](overview.md))

For markets that depend on a specific station (e.g., "Mexico City Benito Juárez Airport"), the station name is noted on the market detail page.

## Why climate?

Two reasons climate earns its own pillar instead of folding into "other":

1. **Tournament-relevant**: Heat in Mexico City, rain in Toronto, hurricane risk in the Gulf — these all materially affect matches. Predicting climate alongside the match is a natural cross-pillar move.
2. **Public, free oracle data**: Open-Meteo and NOAA give us the same data professional meteorologists use, with no API costs. That keeps climate markets cheap to run and easy to verify.

## In the app

Climate markets show up in **teal-green**.
