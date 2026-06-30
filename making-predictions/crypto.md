---
description: BTC and TON, weekly Up/Down markets on tournament Fridays and the FIFA World Cup 2026 Final day.
---

# Crypto markets

## The two assets

Fronex keeps crypto simple. We track two assets:

* **BTC** — Bitcoin
* **TON** — the asset our chain runs on

That's it. No ETH, no SOL, no XRP. The honest version: crypto isn't the main event here — the FIFA World Cup 2026 is. Crypto is a small, focused side pillar, not a 24/7 trading desk.

## How crypto markets work: Up or Down

There's just one market type, and it's about as simple as it gets.

Each market asks one question: **will the price close above where it started?** When the market opens, we capture the live spot price — that's the **strike**. At expiry, we check the closing price against that strike.

* **Up** wins if it closes strictly *above* the strike.
* **Down** wins if it closes at or below the strike.

> **BTC — Up or Down this week?**
> Strike: $68,420 (captured at open)
> Up · Down

That's the whole format. No buckets, no multi-way "which asset wins," no pair comparisons — just a clean call on direction.

## When these markets run

Crypto markets aren't running all the time. The full set is about a dozen markets:

* **BTC and TON weekly Up/Down markets on the tournament's Fridays.**
* **BTC and TON Up/Down markets on FIFA World Cup 2026 Final day** (Sunday, July 19, 2026).

So crypto shows up on a handful of dates — it's a side prediction for the duration of the tournament, not an always-on feed.

{% hint style="info" %}
**Match-Window Crypto is currently paused.** We built a feature that auto-spawns short crypto markets keyed to a soccer match's kickoff and full-time. It isn't running right now — it spawns zero markets at the moment. If and when we switch it back on, we'll update this page. For now, crypto is just the weekly and Final-day Up/Down markets above.
{% endhint %}

## Resolution

* **Primary source**: Binance
* **Secondary check**: CoinGecko
* **Backup**: Pyth (tertiary fallback, used only if Binance is unavailable and CoinGecko disagrees)

Up/Down markets are **settled manually at expiry**. We capture the closing price, compare it to the strike, and pay out. We keep the Binance and CoinGecko readings on record so any settlement can be checked later. If the sources disagree by more than a small margin, we hold and reconcile before settling.

## Pricing

Crypto Up/Down markets show an **indicative price** computed from live spot + a log-normal volatility model — refreshed roughly every 30 seconds. It's a fair-value anchor; the order-book price is what you actually trade. See [How predictions work § The indicative price](overview.md#the-indicative-price).

## In the app

Crypto markets show up in **orange**.

## What you'll never see in crypto markets

No leveraged products. No perpetuals. No "long" or "short" framing. Fronex crypto markets are **simple binary prediction markets** — you call the direction (Up or Down) and the outcome resolves one way or the other. There is no liquidation, no funding rate, no leverage multiplier.
