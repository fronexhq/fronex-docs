---
description: The Bracket Challenge — Fronex's marquee tournament for the FIFA World Cup 2026.
---

# The Bracket Challenge

The Bracket Challenge is Fronex's flagship tournament. One entry, 32 picks, real USDT prizes — and it lives entirely off-chain in our database so there are no per-entry gas fees.

## What it is

Before the FIFA World Cup 2026 begins on June 11, 2026, you submit **a full bracket**:

1. **Group-stage picks** — who finishes 1st, 2nd, and 3rd in each of the 12 groups.
2. **Best-3rd picks** — which 8 of the 12 third-placed teams advance to the Round of 32.
3. **Knockout picks** — predicting every match through the Round of 32 (16 matches), Round of 16 (8), Quarter-Finals (4), Semi-Finals (2), Third-Place (1), and the Final.

Total picks per entry: **104 matches** worth of outcomes, condensed into a single bracket form. The Mini App walks you through it screen by screen.

## Entry fee and prize pool

* **Entry fee**: small USDT amount (set per season, shown in the Mini App at signup).
* **Prize pool**: 100% of entry fees, minus a small platform fee, plus a seed contribution from Fronex.
* **Refund condition**: if fewer than 10 entries are received, the tournament is cancelled and entry fees are refunded to all participants.

## Scoring

Points are awarded per correct pick, with multipliers that increase as the tournament progresses:

| Stage | Points per correct pick |
|---|---|
| Group placement | 5 |
| Best-3rd advance | 10 |
| Round of 32 | 15 |
| Round of 16 | 25 |
| Quarter-Finals | 50 |
| Semi-Finals | 100 |
| Third-Place playoff | 75 |
| **Final winner** | **200** |

A perfect bracket would score thousands of points. Realistically nobody's ever picked one — but you don't need to be perfect to win the prize pool. The best bracket among the entries takes the top prize; runners-up share a graded payout.

## Settlement

Tournaments are **100% off-chain** — in PostgreSQL, not on TON contracts. This keeps entry costs low and lets us run leaderboards in real time. The prize-pool payout, however, *is* on-chain: when the tournament resolves (within 24 hours of the FIFA World Cup 2026 Final on July 19, 2026), payouts go out as a single batched **ClaimBatch** transaction from the platform's vault.

You can claim your prize from the Mini App at any time during the 90 days following resolution.

## Editing your bracket

Locked at the **kickoff of the first FIFA World Cup 2026 match** (June 11, 2026, 21:00 UTC).

Until then, you can revisit and edit any pick. After lock, the bracket is read-only — you can watch your score climb (or fall) match by match, but you cannot change picks.

## Tournament template, not one-off

The Bracket Challenge is the first tournament built on Fronex's reusable tournament infrastructure. After the FIFA World Cup 2026 we'll run:

* Premier League season-long brackets
* Champions League knockout brackets
* Other public knockout-format tournaments

The infrastructure is the same; only the source event changes.
