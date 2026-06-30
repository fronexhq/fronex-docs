---
description: What Fronex charges, where the money goes, and how payouts work.
---

# Fees & payouts

Fronex earns only on **trade fees** and **market creation fees**. There is no spread on the order book; the price you see is the price you pay. There is no deposit fee and no platform withdrawal fee — the only cost to move money is the TON network gas, and your withdrawal gas is paid by Fronex for you (it is never taken out of your USDT).

## Trade fees

When you take an order (predict in or out of a market), a small percentage fee is taken from your trade. The baseline taker fee is **1.5%**, and makers (resting limit orders) pay **no fee**. The effective rate is then scaled by a per-pillar multiplier, by how active the market is, and by your 30-day trading volume (higher-volume traders pay less):

| Pillar | Trade fee multiplier | Notes |
|---|---|---|
| Soccer | 0.8× | Auto-resolved via API-Football |
| Crypto | 1.0× (baseline) | BTC & TON "Up/Down" only; settled manually at expiry against Binance / CoinGecko / Pyth |
| Entertainment | 1.2× | Semi-manual resolution |
| Climate | 1.2× | Auto-resolved via Open-Meteo / NOAA |
| **Community / Custom** | **1.5×** | Manual MO resolution |

On top of this, **one pillar rotates to zero fee each week** (every Monday UTC), so a full category trades fee-free one week in five.

## Trade fee splits

The trade fee is split four ways:

1. **Market Owner share — 50%.** The Market Owner who created the market earns half of every trade fee on it.
2. **Rebate pool — 20%.** Paid out daily, pro-rata, to the real makers who provided the liquidity you traded against.
3. **Treasury — 25%.** The platform's operating account, which also funds the referral reward (see below).
4. **Insurance pool — 5%.** Held back to cover disputed resolutions and reversed-oracle refunds.

This split is the same for everyone — there's no hidden surcharge on referred users.

## Inviting friends

If a friend joins through your invite link, you earn **10% of the trading fees they generate** — paid in USDT straight to your Fronex balance. It comes out of **Fronex's own treasury share**, never out of your friend's money: they pay the exact same fees as everyone else, and you're never charged to invite. Full details in [Invite friends & earn](referrals.md).

## Market creation fees

Creating a market — whether as the platform or as a Market Owner — costs a flat USDT fee, paid at market creation time. The fee is **refunded in full** if your draft is rejected during admin review (for example, an AI clarity review rejection you can't or won't fix).

| Pillar | Creation fee | Why |
|---|---|---|
| Soccer | $5 | Oracle-fed, minimal manual work |
| Crypto | $5 | BTC & TON "Up/Down" markets, settled manually at expiry |
| Entertainment | $15 | Semi-manual, verified against public sources |
| Climate | $15 | Oracle-fed, but stricter parameters |
| Community / Custom (Pillar 5) | $25 | Manual MO resolution |

The exact fee is shown in the Mini App's Create flow before you commit.

## Where there are no fees

* **No deposit fee.** Only the TON network gas applies, paid by your own wallet when you send the deposit, not by Fronex. The minimum deposit is **0.01 USDT**.
* **No platform withdrawal fee, and no withdrawal gas charged to you.** Fronex sponsors the TON gas for your withdrawal — it is never deducted from your USDT balance. The minimum withdrawal is **1 USDT**.
* **No idle-balance fee.** Holding USDT in your Fronex wallet costs nothing.
* **No extra fee on a League beyond its stated entry.** Free leagues cost nothing to join. **Paid pools** charge only the entry fee shown on the join screen — and **100% of entry fees go into the prize pool** (Fronex takes no platform cut on Leagues).

## Payouts

Payouts are credited **automatically** to your Fronex balance **at settlement** — there is nothing to claim:

* **Auto-resolved markets**: shortly after the event ends, once the oracle result is in.
* **Semi-manual markets** (Entertainment): within 24 hours.
* **Community/Custom markets**: within 24 hours of the Market Owner setting the outcome.
* **Leagues**: prizes are credited automatically once the league's end time passes and settlement runs — winnings are pushed straight to your balance, with no claim window.

Payouts settle to your Fronex balance as USDT. From there, you can withdraw to any external TON wallet.

## What about the platform's wallet?

Fronex is **custodial**. When you deposit, your USDT is held in Fronex's treasury and credited to your account balance ([Your wallet](your-wallet.md)). The honest version: your money sits in a pooled Fronex treasury, not a personal on-chain vault you sign from — Fronex holds it and is responsible for staying solvent (we continuously reconcile so the total of everyone's balances never exceeds the USDT we actually hold). You can withdraw to any TON wallet you control at any time, and Fronex sponsors the network gas to send it.

## Refunds

A draft market that is **rejected during admin review** has its creation fee returned in full to the creator, in the same step as the cancellation.

Markets that **resolve to an outcome we then determine was wrong** trigger a refund of affected positions, paid from the insurance pool. We have not yet had to use this path; if we do, the post-mortem is published publicly.

Tournaments that don't reach the minimum number of players are **cancelled, and every entry fee is refunded** to your balance automatically.

## Tax

Fronex does not withhold tax on payouts. Tax treatment of prediction-market winnings varies by country, and it's your responsibility to report and pay as required where you live. We will not provide tax guidance.
