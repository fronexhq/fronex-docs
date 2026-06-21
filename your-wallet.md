---
description: Your deposit address, your balance, deposits, withdrawals, and the honest version of how Fronex holds your funds.
---

# Your wallet

## How Fronex holds your funds (the honest version)

Let's be straight about this, because it matters. **Fronex is custodial.** When you deposit, your USDT is held in Fronex's treasury and credited to your **account balance** — the number you see in the app. That balance is what you predict with, and it's yours to withdraw any time.

The first time you open the app, Fronex generates a **personal deposit address** for you on TON. That address is just a doorway for receiving funds: you send native **USDT on TON** to it, and once the deposit lands it's credited to your balance. Behind the scenes Fronex sweeps deposits into a treasury pool that it controls — so the deposit address is a *receive-only address*, not a wallet you sign from and not one you hold a recovery phrase for.

Two things matter about that:

1. **Fronex holds custody, and is responsible for it.** Your USDT sits in Fronex's treasury, and your account balance is the authoritative record of what you're owed. Fronex continuously reconciles to make sure the pooled USDT always covers everyone's balances.
2. **Trading is instant.** Predictions are matched and settled against your balance off-chain, so the app feels instant and markets can resolve the moment they're called — no on-chain transaction every time you make a move.

You can withdraw any time to any TON wallet you control, and Fronex sponsors the network gas. Withdrawals are signed and sent by Fronex from its pool straight to the address you give us.

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

## Taking funds off the platform

To move your balance to a wallet you control, **withdraw** in-app (Wallet → Withdraw) to any TON address you own, such as Tonkeeper or MyTonWallet. Fronex signs and sends the USDT from its pool and sponsors the gas, so the full amount you request lands in your wallet. There is no recovery phrase for you to export and no separate "move it yourself" path — withdrawing in-app is how you take funds out.

Because Fronex is custodial, the security of your funds rests on **your Telegram account access** — that's how you get into the app and authorise withdrawals. Keep your Telegram account secure (a strong password and two-factor authentication), and never hand control of it to anyone, including people claiming to be Fronex.

## What we never ask for

* A recovery phrase or seed phrase for **any** wallet — Fronex never asks for one, ever (and there is no Fronex recovery phrase to give out)
* Your Telegram password or 2FA codes
* A withdrawal "fee" paid to an outside address, or any payment to "unlock," "verify," or "release" your balance

Anyone asking for those things is not Fronex. Forward the message to [admin@fronex.xyz](mailto:admin@fronex.xyz) and block them.
