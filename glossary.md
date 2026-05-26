---
description: Definitions of the terms Fronex uses — and the terms we deliberately don't.
---

# Glossary

## A

**Admin SET** — the on-chain set of platform addresses authorized to sign settlement transactions. Stored as a `map<Address, Bool>` inside the FronexVault contract. New addresses added via `RegisterAdmin` opcode.

**API-Football** — our primary oracle for soccer (and tennis) match data and outcomes.

***

## B

**Best-3rd race** — at the FIFA World Cup 2026, 8 of the 12 third-placed group teams advance to the Round of 32. The "best-3rd race" is the set of markets predicting which 8.

**Bracket Challenge** — Fronex's flagship tournament. A 32-pick bracket covering the full FIFA World Cup 2026, run off-chain in PostgreSQL with on-chain prize payouts.

**brand-x glyph** — the Fronex logo. A 3D X letterform with a small gold crown in the upper-right notch and static sparkles. Three product variants: purple (fronex.fun), navy (fronex.xyz), rose (fronex.bio).

***

## C

**Call it** — what Fronex calls a correct prediction. Replaces "win" or "win the bet" everywhere in the app.

**ClaimBatch** — the on-chain operation that settles a batch of resolved positions in a single TON transaction. Reduces per-position gas cost.

**Climate (pillar)** — host-city weather and hurricane markets, ~5% of platform volume. Resolved from Open-Meteo and NOAA NHC.

**Closed beta** — the May 28 → June 6, 2026 window during which the Mini App is open only to hand-picked testers on mainnet via tokenized URLs.

**Community / Custom (pillar)** — Market Owner-created markets, ~3% of platform volume. 1.5× trade-fee multiplier compensates MOs for manual resolution.

**Coming-soon gate** — the public landing screen everyone sees until June 7, 2026. Closed-beta testers bypass via per-tester token; there is no Telegram-only bypass.

**Crypto (pillar)** — markets on BTC / ETH / SOL / XRP / TON. ~15% of platform volume. Includes the **Match-Window Crypto** cross-pillar feature.

***

## D

**Drop a prediction** — submit a prediction. Replaces "place a bet."

***

## E

**Entertainment (pillar)** — music charts, awards, summer cultural events. ~7% of platform volume. Semi-manual resolution.

***

## F

**FIFA World Cup 2026** — the tournament we launch around. 48 teams, 12 groups, 104 matches, June 11 – July 19, 2026. Hosted across the USA, Canada, and Mexico. **Always write the full name** in user-facing copy.

**Fronex.bio** — sister product. AI marketing tool for crypto projects. Private during the FIFA World Cup 2026 (founder uses it internally to market fronex.fun); public SaaS launches September 2026.

**Fronex.xyz** — sister product. The Fronex studio's public-facing website. Launches alongside fronex.fun on June 7, 2026.

**FronexVault** — the on-chain Tact contract that holds market collateral and settles outcomes. Five messages: LockForMarket, CreditFeePool, ResolveMarket, ClaimBatch, DistributeFees.

***

## G

**Gate** — short for coming-soon gate. See above.

***

## J

**Jetton** — a TON token standard. USDT on TON is a jetton.

***

## K

**KEK (Key Encryption Key)** — the master key Fronex uses to encrypt user vault mnemonics (`USER_VAULT_KEK_BASE64`) and platform shard mnemonics (`TREASURY_KEK_BASE64`). Two independent KEKs.

**Knockout** — the post-group stage of the FIFA World Cup 2026 (Round of 32 onward). Markets are **two-way** (Team A · Team B) — never three-way, because extra time and penalties always produce a winner.

***

## M

**Market Owner (MO)** — a user with platform permission to create Community markets. Earns a share of trade fees on their markets.

**Match-Window Crypto** — Fronex's cross-pillar feature. Every soccer match auto-spawns 3+ short crypto markets keyed to the match's kickoff and full-time, resolving from a Binance + CoinGecko price snapshot within 60 seconds of full-time.

**Mini App** — the Fronex product. Lives entirely inside Telegram via `@fronexfun_bot`. No separate native app to install.

***

## O

**Oracle** — a data source we use to resolve markets. We run: API-Football (soccer/tennis primary), TheSportsDB (sports backup), Binance (crypto primary), CoinGecko (crypto secondary), Pyth (crypto tertiary fallback), Spotify Charts (entertainment), Open-Meteo (weather), NOAA NHC (hurricanes).

**Order book** — the list of unmatched buy and sell orders on a market. Fronex uses a Redis-backed off-chain CLOB.

***

## P

**Pillar** — one of Fronex's five market categories: Soccer, Crypto, Entertainment, Climate, Community/Custom.

**Predict** — what you do on Fronex. We deliberately never say "bet."

**Per-user personal vault** — each Fronex user has their own `WalletContractV4` wallet on TON. User funds sit in the user's vault, not in a platform pool.

***

## R

**Round of 32 / R32** — the first knockout stage of the FIFA World Cup 2026, starting June 28, 2026. 16 matches.

***

## S

**Sanctions block** — the four-jurisdiction platform block: Iran, Syria, North Korea, Cuba. Implemented as `SANCTIONS_BLOCK_LIST = ['IR','SY','KP','CU']` and enforced before any account is created.

**Sharded admin treasury** — Fronex's platform-side wallet model. N independent admin signing wallets (~1 per 100 users), all encrypted with a single KEK. Sharding is for throughput, not blast-radius reduction. Users don't interact with these directly.

**Soccer (pillar)** — the largest pillar, ~70% of platform volume during the FIFA World Cup 2026.

***

## T

**Telegram Mini App** — Telegram's in-chat web app framework. Fronex is built as one.

**TON** — The Open Network. The blockchain Fronex runs on. Also the name of TON's native asset (one of our 5 tracked crypto assets).

**Tact** — the smart-contract language we use for our two contracts (FronexVault, FronexStaking).

**Token (closed beta)** — a per-tester URL-safe code that bypasses the coming-soon gate during closed beta. Issued individually; not transferable; revocable.

**Tournaments** — multi-market events with their own entry fee and prize pool. The Bracket Challenge is the first; more will follow post-World Cup.

***

## U

**USDT** — the stablecoin Fronex uses for all market collateral, fees, and payouts. Sent and received on the **TON network** only.

***

## V

**Vault** — see "personal vault" / "WalletContractV4". Or, for the on-chain contract sense, see "FronexVault."

***

## W

**WalletContractV4** — the standard TON wallet contract. Every Fronex user has one as their personal vault.

***

## Things Fronex deliberately does NOT use

These words are **forbidden** in Fronex user-facing copy:

* **bet** / **wager** / **gamble** — we use **predict** / **drop a prediction**.
* **win the bet** — we use **call it**.
* **long** / **short** / **leverage** — we don't list leveraged products. Markets are binary or N-way prediction markets.
* **Home / Away** — we use team names. The FIFA World Cup 2026 has neutral venues; there is no home advantage.
* **World Cup** (alone) — we use **FIFA World Cup 2026** (the full trademark-respecting name).
