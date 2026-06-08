---
description: Your personal TON vault, deposits, withdrawals, and what self-custody means in practice.
---

# Your wallet

## Your personal vault (self-custody)

The first time you open the app, Fronex generates a **personal vault** for you on TON — an on-chain wallet that only you control. You deposit native **USDT on TON** to your vault's address, and the USDT held there is your balance. You self-custody: Fronex never holds your funds for you.

Two things matter about that:

1. **You self-custody.** Your USDT lives in your own vault on TON — it is **not** pooled into a Fronex treasury wallet. You can export your vault's recovery phrase at any time and move your funds yourself, with or without the app.
2. **Trading is instant; your funds stay on-chain.** While a market is live, Fronex matches and settles your predictions off-chain so the app feels instant — but the USDT that backs your balance stays in your own on-chain vault until you choose to move it.

You can withdraw any time to any TON wallet you control, and the app sponsors the network gas. Because predictions settle off-chain, markets can resolve instantly while they're live — and your USDT stays in your own vault the whole time.

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

Your balance lives in your own personal vault, so you have **two ways** to take funds off the platform. The simplest is to **withdraw** in-app (Wallet → Withdraw) to any TON address you control, such as Tonkeeper or MyTonWallet — the app signs the USDT from your vault and sponsors the gas. You can also **export your vault's recovery phrase** from the app's wallet settings and move the USDT yourself from any TON wallet, with or without Fronex.

Because you self-custody, the security of your funds rests on two things: your Telegram account access **and** your recovery phrase. Anyone who has your recovery phrase can move your USDT — keep it offline and never share it with anyone, including people claiming to be Fronex.

## What we never ask for

* A recovery phrase or seed phrase of any kind — Fronex never asks for one, ever
* Your Telegram password or 2FA codes
* A withdrawal "fee" paid to an outside address, or any payment to "unlock," "verify," or "release" your balance

Anyone asking for those things is not Fronex. Forward the message to [admin@fronex.xyz](mailto:admin@fronex.xyz) and block them.
