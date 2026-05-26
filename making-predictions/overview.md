---
description: How a market works on Fronex — order book, prices, positions, and settlement.
---

# How predictions work

## The basic shape of a market

Every Fronex market has **two or three possible outcomes**:

| Market type | Outcomes |
|---|---|
| **Two-way** (knockouts, crypto strikes, yes/no questions) | Team A · Team B |
| **Three-way** (group-stage soccer, draw possible) | Team A · Draw · Team B |
| **N-way** (top scorer, group winner, top performer of week) | One outcome per option |

You **pick an outcome** and the market gives you a **price** — between 0.01 and 0.99 USDT. The price represents the market's current view of how likely that outcome is.

Example:

> **Brazil vs Argentina — group stage**
> Brazil **0.42** · Draw **0.28** · Argentina **0.30**

Buying Brazil at 0.42 USDT means: if Brazil wins, you receive 1.00 USDT per share. Your profit is 0.58 USDT per share. If Brazil doesn't win, your shares settle to zero.

## Buying and selling

Markets are an **order book**, not a fixed-price product. Prices move as people buy and sell.

* **Buy** an outcome you think is more likely than its price suggests.
* **Sell** a position you already hold to lock in a profit (or cut a loss) before the market resolves.

You don't have to wait until settlement. If you bought Brazil at 0.42 and the price rises to 0.55 before the match starts, you can sell and pocket the difference.

## How settlement works

When the event ends, the market **resolves** based on data from one of our oracle providers:

* **Soccer & tennis**: API-Football (primary), TheSportsDB (backup)
* **Crypto**: Binance (primary), CoinGecko (secondary), Pyth (tertiary fallback)
* **Entertainment**: Spotify Charts and other public feeds
* **Climate**: Open-Meteo (weather), NOAA NHC (hurricanes)
* **Community/Custom**: Market Owner sets the resolution rule when creating the market; resolution is verified manually

Payouts hit your wallet within seconds of settlement. The Mini App will push a notification.

## Disputed or delayed resolutions

If an oracle disagrees with another source (e.g., API-Football says one thing, TheSportsDB another) or the source data is delayed, the market enters **pending resolution** and we resolve manually within 24 hours. You can still trade in and out of pending markets, but settlement happens once we confirm the outcome.

## What you'll never see on Fronex

We use the language of **prediction**, not the language of gambling. You won't see "bet," "wager," "long," "short," or "leverage" anywhere in the app. You'll see:

* **Predict** — pick an outcome
* **Call it** — your prediction was right
* **Drop a prediction** — submit your pick

This isn't aesthetic — it's policy. Fronex is a prediction app for skill-based forecasting, not a betting product.

## The five pillars

* **[Soccer](soccer.md)** — the FIFA World Cup 2026 plus year-round leagues
* **[Crypto](crypto.md)** — five assets, daily/weekly markets, plus the match-window feature
* **[Entertainment](entertainment.md)** — music charts, awards, summer culture
* **[Climate](climate.md)** — host-city weather, hurricanes
* **[Community & custom](community.md)** — Market Owner-created markets
