---
description: Five assets, daily and weekly markets, plus the Match-Window Crypto cross-pillar feature.
---

# Crypto markets

## The five assets

Fronex tracks five crypto assets at launch:

* **BTC** — Bitcoin
* **ETH** — Ethereum
* **SOL** — Solana
* **XRP** — Ripple
* **TON** — Toncoin (the asset our chain runs on)

About 15% of platform volume runs through crypto.

## Market types

### Daily close-strike

Will the asset close above or below a target price at end-of-day UTC?

> **BTC ≥ $70,000 by 23:59 UTC**
> Yes · No

### Weekly close-strike

Same format, weekly horizon. Closes Sunday 23:59 UTC.

### Top performer of the week

Multi-outcome (5-way): which of BTC, ETH, SOL, XRP, TON has the highest 7-day return?

### Pair outperform

Two-way: does asset A outperform asset B over a given window?

> **TON outperforms ETH over the next 7 days?**
> Yes · No

### FIFA World Cup 2026 final price marquees

Marquee markets for the duration of the FIFA World Cup 2026:

* **BTC price on the day of the World Cup Final** — multi-outcome bucketed
* **TON price on the day of the World Cup Final** — multi-outcome bucketed

## The Match-Window Crypto feature

This is Fronex's cross-pillar differentiator and a marquee feature for the FIFA World Cup 2026:

**Every soccer match auto-spawns 3 or more linked crypto markets** keyed to the match's kickoff and full-time. These markets:

* Open when the match opens
* Close when the match ends
* Resolve from a **Binance price snapshot at full-time**, cross-checked against CoinGecko, within 60 seconds of the final whistle

Example for **Brazil vs Argentina, kickoff 21:00 UTC**:

* "BTC ↑ during the match?" — yes/no
* "TON outperforms ETH for the next 2 hours?" — yes/no
* "BTC moves > 0.5% (either direction) during the match?" — yes/no

The result: a 90-minute soccer match generates ~3 short, sharp crypto markets you can predict alongside the match itself. You don't need to pick between watching the game and trading — you do both.

## Resolution

* **Primary oracle**: Binance (REST `/api/v3/ticker/price`)
* **Secondary oracle**: CoinGecko (sanity check)
* **Tertiary fallback**: Pyth (used if Binance returns an error and CoinGecko disagrees)

If the primary and secondary diverge by more than 0.5%, the market goes into pending and resolves manually within 24 hours.

Snapshot timing for match-window markets: the price is captured **within 60 seconds of full-time** as reported by API-Football. Both the Binance and CoinGecko readings, plus the divergence in basis points, are stored in `market_resolutions.oracle_proof` for audit.

## Pillar accent color

Crypto markets use **orange** (`#F97316`) for the Called-It state. The pillar's icon is a stylized coin glyph from the Fronex sticker set.

## What you'll never see in crypto markets

No leveraged products. No perpetuals. No "long" or "short" framing. Fronex crypto markets are **binary or N-way prediction markets** — you call the direction and the outcome resolves yes/no. There is no liquidation, no funding rate, no leverage multiplier.
