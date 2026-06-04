---
description: How Fronex holds your USDT, deposits, withdrawals, and what custody means in practice.
---

# Your wallet

## How Fronex holds your balance

Fronex is a **custodial** prediction platform. You deposit native **USDT on TON** to a deposit address, and once the deposit is credited, your balance is tracked in Fronex's ledger — that ledger is the authoritative record of what you own.

Two things matter about that:

1. **Your balance is held by Fronex on your behalf.** After a deposit is credited, the USDT is pooled in Fronex's treasury-controlled wallets and your balance lives in Fronex's off-chain ledger. There is no per-user wallet you control and no recovery phrase to export — custody and solvency are Fronex's responsibility.
2. **Solvency is continuously reconciled.** A reconciliation worker checks every few minutes that the sum of all user balances is fully backed by the USDT Fronex holds. If anything ever drifted, it would be flagged loudly.

You withdraw any time and Fronex signs the USDT back to your own TON wallet from the pool. Because the ledger — not an on-chain wallet you hold — is the source of truth, the convenience is that the app can settle markets for you instantly while a market is live.

## Funding your wallet

Open the Mini App, tap the wallet icon (top-right), then **Deposit**. Funding is **native USDT on TON only** — there is no card, on-ramp, bridge, or cross-chain swap. There are exactly two ways to fund your account, and both deliver **USDT on TON** to your deposit address.

### Option 1 — Connect your TON wallet (one tap)

The simplest path. Connect a TON wallet — **Telegram Wallet, Tonkeeper**, or any TON Connect wallet — and approve a single USDT transfer that Fronex prepares for you.

1. Tap **Connect wallet** and pick your TON wallet.
2. Fronex builds the USDT transfer for you (the destination is set on our side — never trusted from your device) and your wallet shows it for approval.
3. Approve the transfer. You pay only the TON network gas for the transfer; if your wallet is short on TON, the app warns you before you sign so the transfer doesn't fail.

### Option 2 — Send to your deposit address (manual)

Use this if you already hold USDT on TON in an exchange or another wallet.

1. The screen shows your deposit address (a `UQ…` or `EQ…` string, ~48 characters) and a QR code of it.
2. From any exchange or wallet that supports **USDT on TON**, set the network to **TON**, paste the address, and send.
3. Most TON deposits confirm in **a few seconds to a couple of minutes**.

{% hint style="warning" %}
**Send USDT on the TON network only.** Sending USDT on Tron, Ethereum, BSC, or any other network to this address will result in **permanent loss** — those funds cannot be recovered. Always confirm the network reads "TON" before you send.
{% endhint %}

Your balance updates automatically once the deposit lands and is detected on-chain — there's no fixed confirmation count to wait for. If it hasn't appeared after a few minutes, contact [admin@fronex.xyz](mailto:admin@fronex.xyz) with your transaction hash.

### Minimum deposit

The enforced minimum deposit is **0.01 USDT**. (Below that, USDT's six-decimal rounding can produce a zero-value transfer that still burns gas.) That said, TON network gas applies to every transfer, so for a first deposit we recommend sending at least **5 USDT** so the gas is small relative to the amount.

## Withdrawing

To withdraw USDT to an external wallet:

1. Wallet → **Withdraw**.
2. Paste your destination TON address.
3. Enter the amount (USDT, TON network).
4. Confirm.

Withdrawals usually settle within about a minute. **Fronex charges no withdrawal fee** — the exact amount you request is sent. The only cost is the TON network gas for the on-chain transfer, and **Fronex sponsors that gas** — it is not deducted from your balance.

### Minimum and limits

* **Minimum withdrawal: 1 USDT** (a floor that keeps tiny transfers from costing more in gas than they're worth).
* **Up to 5 withdrawals per rolling 24 hours** per account. There is no per-day USD cap and no cooldown on amounts — just this count limit, which applies at all times (it is not beta-only).

## Withdrawing to your own wallet

Fronex holds your balance custodially, so there is **no recovery phrase to export** — there is no per-user wallet you control. To take funds off the platform, simply **withdraw** (Wallet → Withdraw) to any TON address you control, such as Tonkeeper or MyTonWallet. Fronex signs the USDT to that address from the treasury pool, and your balance moves with you.

Because custody is Fronex's responsibility, the security of your funds depends on your Fronex account access and on Fronex's reconciled solvency — not on you safeguarding a seed phrase.

## What we never ask for

* A recovery phrase or seed phrase of any kind — Fronex never asks for one, ever
* Your Telegram password or 2FA codes
* A withdrawal "fee" paid to an outside address, or any payment to "unlock," "verify," or "release" your balance

Anyone asking for those things is not Fronex. Forward the message to [admin@fronex.xyz](mailto:admin@fronex.xyz) and block them.
