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

No external wallet is needed to deposit and play — you can fund your account in one tap with TON Connect or by sending USDT-on-TON to your deposit address. You'll want a TON wallet (Tonkeeper, MyTonWallet, Telegram Wallet, …) when you withdraw, since that's where your USDT is sent.

### How do I get into the closed beta?

Email [admin@fronex.xyz](mailto:admin@fronex.xyz) with your Telegram handle, time zone, and which pillar interests you most. Closed beta runs May 28 → June 6, 2026.

***

## Funding

### How can I fund my account?

Markets settle in **USDT on TON**, and that's how you fund your account — you deposit native USDT on the TON network. The Deposit screen gives you two ways to do it:

* **One-tap with TON Connect** — connect a TON wallet (Telegram Wallet, Tonkeeper, …) and approve a single USDT transfer. Fronex builds the transfer for you so it always goes to the right place; your wallet just signs it. No Fronex fees.
* **Manual transfer** — copy your deposit address (or scan the QR) and send USDT-on-TON to it from any wallet or exchange. No Fronex fees.

See [Your wallet](your-wallet.md) for the full walkthrough.

{% hint style="warning" %}
Send only **USDT on the TON network**. USDT sent to your address on Tron, Ethereum, BSC, or any other network is permanently lost. There is no card, on-ramp, or cross-chain bridge — funding is native USDT-on-TON only.
{% endhint %}

### Is there a minimum deposit?

Yes — **0.01 USDT**. Below that, TON's rounding can produce a zero-value transfer that still burns network gas. There's no upper limit. For a first deposit you'll also want a little TON in your wallet to cover network gas on the transfer.

### How long do deposits take?

A USDT-on-TON transfer typically confirms in 5–30 seconds. Your Fronex balance updates automatically once the deposit is detected on-chain — there's no fixed confirmation count or manual step.

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

Nothing from Fronex — there's no platform or percentage withdrawal fee. Withdrawals require network gas on TON, and **Fronex sponsors that gas for you**, so the full amount you request is what's sent. The minimum withdrawal is **1 USDT** (a floor to keep withdrawals from costing more in gas than they're worth).

### Is there a withdrawal limit?

You can make up to **5 withdrawals per rolling 24 hours**. There's no cap on the total amount you can withdraw — it's a count limit, not a value limit.

### Can I withdraw to my own wallet?

Yes. Withdraw any time to any TON wallet you control (Tonkeeper, MyTonWallet, Telegram Wallet, …). Fronex signs the USDT transfer to your address; you don't need a recovery phrase from us to receive it.

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

Market Owners earn **50% of the trade fees** generated on their markets. The baseline taker fee is 1.5%, and Community markets carry the highest fee multiplier (1.5×), so they generate the most fee revenue to share. Bigger markets, bigger share.

***

## Trust & safety

### Who custodies my funds?

Fronex does. Fronex is a **custodial** prediction platform: you deposit native USDT-on-TON, and once it's credited, Fronex holds your funds and tracks your balance in our off-chain ledger, which is the authoritative record. You can withdraw to your own TON wallet any time, and Fronex signs the USDT transfer back to you. There's no per-user wallet you control and no recovery phrase to export — custody and solvency are Fronex's responsibility.

### How do I know my balance is backed?

Fronex's balances are continuously reconciled against the USDT we hold on-chain, so the total of everyone's balances is always covered by real funds. We monitor this around the clock and surface any discrepancy loudly rather than letting it slide.

### What if the platform goes down?

Your USDT balance is recorded in Fronex's ledger and backed by funds held on TON. A temporary server outage doesn't put your balance at risk — pending market positions may be slower to settle, but your funds remain accounted for and reconciled.

### What if there's a smart-contract bug?

Our smart contracts are open-source, and we'll publish them on GitHub so anyone can read them. They've been reviewed but not formally audited at launch. Any bug we find is disclosed and either patched (for issues that don't affect funds) or covered from the insurance pool (for issues that do).

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
