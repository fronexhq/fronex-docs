---
description: Frequently asked questions about Fronex.
---

# FAQ

## Account & access

### Is Fronex a betting app?

No. Fronex is a **prediction market** — you call what happens next based on public, oracle-resolvable events. We use the language of prediction throughout, and we don't list traditional betting products like parlays, accumulators, or sports books.

### Where can I use Fronex?

Anywhere except **Iran, Syria, North Korea, and Cuba**. That includes the United States, Canada, and Mexico — the FIFA World Cup 2026 host countries. See [Safety & policy](safety.md).

### What languages does the app support?

Eight at launch: English, Chinese (Simplified), Russian, Japanese, Korean, German, Portuguese (Brazil), Spanish (LATAM). More are on the post-launch roadmap.

### Do I need a separate wallet?

No. Fronex generates a personal vault wallet for you at signup. You don't need Tonkeeper, MyTonWallet, or any external wallet to use the app. (Though you'll want one when you withdraw.)

### How do I get into the closed beta?

Email [admin@fronex.xyz](mailto:admin@fronex.xyz) with your Telegram handle, time zone, and which pillar interests you most. Closed beta runs May 28 → June 6, 2026.

***

## Funding

### What asset do I deposit?

**USDT on the TON network only.** Sending USDT on any other network (Tron, Ethereum, BSC, etc.) results in permanent loss. Always confirm "TON" before you send.

### Is there a minimum deposit?

No enforced minimum, but TON network fees are small, so we recommend at least 5 USDT for your first deposit.

### How long do deposits take?

5–30 seconds for the on-chain confirmation. Your Fronex balance updates immediately after that.

### Can I deposit TON instead of USDT?

Not at launch. USDT is the only quote asset for markets. TON is the asset Fronex's chain runs on, but it's not what you predict in.

***

## Trading

### Can I cash out before a market resolves?

Yes. Until the market locks (at the event's start time), you can predict in and out. Your position has a current market price; the price moves as other predictors trade.

### What happens to my position after the market locks?

Once locked (e.g., at kickoff for a soccer match), no more trading. The market resolves automatically (or manually for community markets) when the event ends, and the payout hits your wallet within seconds or hours depending on the pillar.

### What if the oracle disagrees with itself?

If our primary and secondary oracles diverge, the market goes into **pending status**. We resolve manually within 24 hours. You can keep trading in/out while pending (with the caveat that the eventual settlement is what determines your payout).

### What's the smallest position I can take?

The Mini App shows the minimum-tick increment on each market. It varies by market type but is typically 0.01 USDT per share.

***

## Money out

### How long do withdrawals take?

Usually under 60 seconds after you confirm. The TON network is fast.

### What does a withdrawal cost?

The TON network fee (a few cents). Fronex does not add a withdrawal fee.

### What's the daily withdrawal limit?

During closed beta: 1,000 USDT per 24 hours. At public launch on June 7, 2026, this relaxes.

### Can I export my wallet to Tonkeeper?

Yes, at public launch. Profile → Security → Export Wallet will give you the recovery phrase. During closed beta, exports are disabled to keep the population stable.

***

## Community markets

### Can I create a market?

Yes — once you have **Market Owner status**. See [Become a Market Owner](market-owners.md) for the three paths. Anyone can apply.

### Why does my proposed market get rejected by AI review?

The most common reasons:

* Ambiguous outcome (more than one interpretation possible)
* Resolution source is private, paywalled, or undisclosed
* The market touches a person's death, illness, or other distasteful subject
* The market uses forbidden vocabulary (bet/wager/gamble/long/short/leverage)
* The market is about a non-public individual

The AI review shows you the specific issue. Edit and resubmit.

### How much do Market Owners earn?

A share of the 0.5× trade-fee multiplier above baseline on Community markets. If your market sees 10,000 USDT in trade volume and the baseline fee is 1%, the MO share is approximately 50 USDT for that market. Bigger markets, bigger share.

***

## Trust & safety

### Who custodies my funds?

You do, in spirit. Your funds sit in a personal vault wallet (a `WalletContractV4` on TON) tied to your account. The wallet's mnemonic is encrypted by Fronex during closed beta so the app can sign settlement transactions for you. At public launch, **Export Wallet** becomes available — paste the mnemonic into any TON wallet and your balance moves with you.

### Can Fronex see my deposits?

Anyone can. Your vault wallet's TON address is public on the chain. Anyone with a TON block explorer can see your balance and transactions. That's a feature, not a bug — it's how we promise you that your money isn't pooled with everyone else's.

### What if the platform goes down?

Your funds are in your personal vault on TON. Even if Fronex's servers were entirely offline, your USDT is still on TON. Pending market positions might be slower to settle, but the underlying assets are not at risk from a platform outage.

### What if there's a smart-contract bug?

Our two Tact contracts (FronexVault and FronexStaking) are public on GitHub at [github.com/fronexhq/fronex-contracts](https://github.com/fronexhq/fronex-contracts). They've been reviewed but not formally audited at launch. Any bug we find is disclosed and either patched (for non-fund-affecting issues) or addressed via insurance pool payouts (for fund-affecting issues).

### What if I disagree with a resolution?

Email [admin@fronex.xyz](mailto:admin@fronex.xyz) with the market ID and your concern. Auto-resolved markets are very rarely wrong (oracles disagreeing triggers pending status). Community-market disputes are escalated to the platform; if the MO resolved against their stated source, the resolution is reversed and the MO loses fee share on that market.

***

## Anything else

### How do I contact the team?

* Email: [admin@fronex.xyz](mailto:admin@fronex.xyz)
* Telegram channel: [t.me/fronex\_official](https://t.me/fronex_official)
* X / Twitter: [@fronexhq](https://x.com/fronexhq)
* Discord: [discord.gg/sA4HFvjjv](https://discord.gg/sA4HFvjjv)

### Is there a referral program?

Not at launch. We may add one post-WC; if we do, it'll be opt-in and clearly disclosed. We're not running any third-party referral links during closed beta.

### When does public launch happen?

**June 7, 2026** — four days before the FIFA World Cup 2026 kickoff.
