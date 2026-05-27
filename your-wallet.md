---
description: Your personal on-chain vault, deposits, withdrawals, and what self-custody means in practice.
---

# Your wallet

## Your own on-chain vault

When you sign up, Fronex generates a **personal vault wallet** for you on the TON blockchain. It's a standard TON wallet, and it's yours.

Two things matter about that:

1. **Your balance is on-chain, not on our books.** When you deposit USDT, it sits in your vault's address — we don't pool user funds into a house wallet. You can verify your balance independently on any TON block explorer (tonviewer.com, tonscan.org).
2. **Your recovery phrase is encrypted.** We hold it in encrypted form so we can settle markets for you — but on launch day, we'll let you export it so you can move funds out using any standard TON wallet.

This is **non-custodial in spirit** — your balance is yours, observable on-chain — with the convenience that the app can sign settlement transactions for you while a market is live.

## Funding your wallet

Open the Mini App, tap the wallet icon (top-right), then **Deposit**. You'll see a list of **funding paths** — pick whichever matches what you're funding from. Whatever you choose, the money arrives as **USDT on TON** in your personal vault.

{% hint style="info" %}
The deposit screen only lists the paths that are live for your account and region. During closed beta, some may show a **Coming soon** badge — use any of the available ones meanwhile.
{% endhint %}

### Option 1 — Telegram Wallet (USDT direct on TON)

The cheapest path, with **no Fronex fees**. Use this if you already hold USDT on the TON network.

1. The screen shows your TON address (a `UQ…` or `EQ…` string, ~48 characters) and a QR code of it.
2. From any exchange or wallet that supports **USDT on TON**, set the network to **TON**, paste your Fronex address, and send.
3. Most TON deposits confirm in **5–30 seconds**.

{% hint style="warning" %}
**This path requires USDT on the TON network only.** Sending USDT on Tron, Ethereum, BSC, or any other network to this address will result in **permanent loss** — those funds cannot be recovered. Always confirm the network reads "TON" before you send. (The other paths below handle network routing for you, so this warning is specific to a direct send.)
{% endhint %}

### Option 2 — Card / Apple Pay

The fastest way to fund with regular money. Pay with **card, Apple Pay, or bank transfer** and receive USDT in your vault — card processing and delivery are handled by MoonPay. Funds usually land within a few minutes. KYC may apply depending on your jurisdiction.

### Option 3 — Crypto & Bridge

For funding from another coin or another chain. This path has two modes you toggle between:

* **Swap a coin** — send BTC, ETH, SOL, XRP, POL, or USDT (on TRON, Ethereum, Solana, or Polygon). You'll get a temporary deposit address; send the exact amount and it's auto-swapped to USDT-on-TON and forwarded to your vault. Swaps typically settle in **10–30 minutes**. Each source asset has a minimum, shown on screen before you send.
* **Bridge from Ethereum** — move **USDT-ERC20** (Ethereum) to TON via the official `bridge.ton.org`. Your destination vault is pre-filled. This typically settles in **5–15 minutes**, depending on Ethereum confirmations. Fronex never custodies funds during transit.

Your balance updates as soon as a deposit confirms. If it hasn't appeared after the expected window, contact [admin@fronex.xyz](mailto:admin@fronex.xyz) with your transaction hash.

### Minimum deposit

There's no enforced minimum for a direct TON send, but TON network fees on USDT transfers are ~0.05–0.10 TON per transaction. We recommend depositing at least **5 USDT** for your first deposit so the network fee is small relative to the amount. For swaps, the per-asset minimum shown in the app applies instead (it varies by source coin and network).

## Withdrawing

To withdraw USDT to an external wallet:

1. Wallet → **Withdraw**.
2. Paste your destination TON address.
3. Enter the amount (USDT, TON network).
4. Confirm.

Withdrawals usually settle within 60 seconds. There's a small network fee (a few cents) for the on-chain transfer.

### Withdrawal limits during closed beta

During closed beta, withdrawals are subject to a 24-hour cooldown after your first deposit, and a per-day cap of 1,000 USDT. These limits relax on public launch (June 7, 2026).

## Self-custody at launch

On launch day, **Profile → Security → Export Wallet** becomes available. That gives you the recovery phrase for your personal vault wallet — paste it into any standard TON wallet (Tonkeeper, MyTonWallet, etc.) and your balance moves with you.

We don't have access to your funds without your signature once you've exported. The trade-off is that you take over key management — if you lose the phrase, we can't recover your funds.

Until launch day, exports are disabled to keep the closed-beta wallet population stable.

## What we never ask for

* The recovery phrase to any other wallet
* A signature from any wallet other than your Fronex vault
* Your Telegram password or 2FA codes

Anyone asking for those things is not Fronex. Forward the message to [admin@fronex.xyz](mailto:admin@fronex.xyz) and block them.
