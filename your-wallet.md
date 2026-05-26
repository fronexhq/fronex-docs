---
description: Your personal on-chain vault, deposits, withdrawals, and what self-custody means in practice.
---

# Your wallet

## Your own on-chain vault

When you sign up, Fronex generates a **personal vault wallet** for you on the TON blockchain. It's a `WalletContractV4` — the standard TON wallet contract — and it's yours.

Two things matter about that:

1. **Your balance is on-chain, not on our books.** When you deposit USDT, it sits in your vault's address — we don't pool user funds into a house wallet. You can verify your balance independently on any TON block explorer (tonviewer.com, tonscan.org).
2. **Your mnemonic is encrypted.** We hold it in encrypted form so we can settle markets for you — but on launch day, we'll make export available so you can move funds out using any standard TON wallet.

This is **non-custodial in spirit** — your balance is yours, observable on-chain — with the convenience that the app can sign settlement transactions for you while a market is live.

## Funding your wallet

### Step 1 — See your address

Open the Mini App, tap the wallet icon (top-right), then **Deposit**.

You'll see:

* Your TON address (a `UQ…` or `EQ…` string, ~48 characters)
* A QR code of the same address
* The asset to send: **USDT (Jetton, TON network)**

{% hint style="warning" %}
**Send USDT on the TON network only.** Sending USDT on Tron, Ethereum, BSC, or any other network will result in **permanent loss** — those funds cannot be recovered. Always confirm the network reads "TON" before you send.
{% endhint %}

### Step 2 — Send USDT

From any exchange or wallet that supports **USDT on TON**:

* Set the network to **TON**.
* Paste your Fronex deposit address.
* Send. Most TON deposits confirm in 5–30 seconds.

Your balance updates as soon as the deposit confirms. If it hasn't appeared after 5 minutes, contact [admin@fronex.xyz](mailto:admin@fronex.xyz) with your TX hash.

### Minimum deposit

There's no enforced minimum, but TON network fees on USDT transfers are ~0.05–0.10 TON per transaction. We recommend depositing at least **5 USDT** for your first deposit so the network fee is small relative to the amount.

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

* Your TON mnemonic from another wallet
* A signature from any wallet other than your Fronex vault
* Your Telegram password or 2FA codes

Anyone asking for those things is not Fronex. Forward the message to [admin@fronex.xyz](mailto:admin@fronex.xyz) and block them.
