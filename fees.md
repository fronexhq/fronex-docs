---
description: What Fronex charges, where the money goes, and how payouts work.
---

# Fees & payouts

Fronex earns only on **trade fees** and **market creation fees**. There is no spread on the order book; the price you see is the price you pay. There are no withdrawal fees beyond the small TON network fee.

## Trade fees

When you predict in or out of a market, a small percentage fee is taken from your trade. Where the fee goes depends on the pillar:

| Pillar | Trade fee multiplier | Notes |
|---|---|---|
| Soccer | 1× (baseline) | Auto-resolved via API-Football |
| Crypto | 1× (baseline) | Auto-resolved via Binance + CoinGecko |
| Entertainment | 1× (baseline) | Semi-manual resolution |
| Climate | 1× (baseline) | Auto-resolved via Open-Meteo / NOAA |
| **Community / Custom** | **1.5×** | Manual MO resolution — extra goes to the Market Owner |

The actual baseline percentage is shown on the trade panel before you confirm. You won't be surprised.

## Trade fee splits

The trade fee is split four ways:

1. **Market Owner share** — only on Community/Custom markets. The 0.5× multiplier above baseline goes here.
2. **Rebate pool** — funds a small rebate for early predictors who provide liquidity into a new market.
3. **Treasury** — the platform's operating account.
4. **Insurance pool** — a small slice held back to cover disputed resolutions.

The exact split percentages are configurable per market and shown on the market's detail page.

## Market creation fees

Creating a market — whether as the platform or as a Market Owner — costs a flat USDT fee, paid at market creation time. The fee is **refunded** if the market is cancelled before the event begins (e.g., low entries, oracle failure, or AI clarity review rejection that you can't or won't fix).

| Pillar tier | Creation fee | Why |
|---|---|---|
| Soccer / Crypto / Climate (auto-resolved) | Lower tier | Oracle-fed, minimal manual work |
| Entertainment (semi-manual) | Lower tier | Verified against public charts |
| Community / Custom (Pillar 5) | Higher tier | Manual MO resolution; matches the 1.5× trade fee multiplier |

The exact fee schedule is shown in the Mini App's Create flow before you commit.

## Where there are no fees

* **No deposit fee.** TON network fee (~0.05 TON) applies on the chain, not on Fronex.
* **No platform withdrawal fee.** Same — only the TON network fee applies.
* **No idle-balance fee.** Holding USDT in your Fronex wallet costs nothing.
* **No fee on the Bracket Challenge entry** beyond the stated entry fee, which is 100% pooled minus a small platform cut declared on the entry screen.

## Payouts

Payouts to your wallet happen **at settlement**:

* **Auto-resolved markets**: within seconds of the event ending.
* **Semi-manual markets** (Entertainment): within 24 hours.
* **Community/Custom markets**: within 24 hours of the Market Owner setting the outcome.
* **Bracket Challenge**: within 24 hours of the FIFA World Cup 2026 Final.

Payouts settle to your Fronex wallet as USDT (TON network). From there, you can withdraw to any external TON wallet.

## What about the platform's wallet?

Fronex uses **sharded admin signing wallets** for the platform's operational settlements — N independent wallets, one for every ~100 users, each encrypted with a single master key. This is an internal architecture detail; users don't interact with platform wallets directly. **You hold your funds in your own personal vault** ([Your wallet](your-wallet.md)).

## Refunds

Markets that **never reach the minimum liquidity** to be viable are cancelled, all positions refunded, and the creation fee refunded to the creator. The Mini App shows the minimum-liquidity threshold on each market's detail page.

Markets that **resolve to an outcome we then determine was wrong** trigger an automatic refund of all positions on the losing side, paid from the insurance pool. We have not yet had to use this path; if we do, the post-mortem is published publicly.

## Tax

Fronex does not withhold tax on payouts. Tax treatment of prediction-market winnings varies by country, and it's your responsibility to report and pay as required where you live. We will not provide tax guidance.
