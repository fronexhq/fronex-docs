---
description: Geo policy, age policy, responsible prediction, and what to do if something feels off.
---

# Safety & policy

## Geo policy

Fronex blocks four jurisdictions at the platform level:

* **Iran** 🇮🇷
* **Syria** 🇸🇾
* **North Korea** 🇰🇵
* **Cuba** 🇨🇺

If you're in one of these countries (detected via IP and platform-level checks at login), the app returns HTTP 451 — you cannot create an account, deposit, trade, or withdraw. This is non-negotiable and required by the asset issuers we work with (USDT enforces the same restriction).

**Every other country is open**, including the United States, Canada, and Mexico — the FIFA World Cup 2026 host countries.

Fronex operates under a **three-mode operational model** that you, the user, don't really need to think about — it only affects how we market in your region:

| Mode | What it means for marketing |
|---|---|
| `BLOCKED_SANCTIONS` | Platform blocked. (IR/SY/KP/CU) |
| `OPEN_ACCESS_NO_PAID_ACQUISITION` | Open to use. No paid ads run in your region. (US/CA/UK/FR/SG/AU/NZ/etc.) |
| `PRIMARY_GROWTH` | Open to use. Active marketing and localization. (LATAM/East Asia/CIS/DACH/etc.) |

If you can open the app and deposit, you can use it. The mode only affects what you might see on Twitter, not what you can do inside Fronex.

## Age policy

Fronex is for users **18 and older**. Some jurisdictions require a higher age (19 in some Canadian provinces, 21 in some US states). Use your local age threshold; we don't override it.

We do not have hard ID verification at signup. We rely on the Telegram account's stated age and our terms-of-service acceptance. If we have reason to believe you are underage, your account is closed and balances are refunded to the source.

## Responsible prediction

Fronex is a prediction product, not a betting product, but the practical risk to your wallet is similar: **you can lose money you put in**.

A few rules of thumb:

* **Deposit only what you can comfortably lose.** Treat any USDT in your Fronex wallet as already gone — that way every win is a bonus.
* **Cap your daily volume.** Use Profile → Limits to set a daily spend cap. The cap is enforced before any trade.
* **Take breaks.** If you're predicting on autopilot or chasing losses, close the app. The market will be there tomorrow.
* **Don't predict when emotional or impaired.** It's the same advice your gambling-aware friends would give you.

## What we will help with

* **Account self-exclusion.** Profile → Self-Exclude pauses your account for 30 days, 6 months, or permanently. Once set, it cannot be reversed before the timeline ends.
* **Daily limits.** Profile → Limits sets per-day deposit and trade caps.
* **Withdrawal first.** If you set a self-exclusion, your balance is automatically queued for withdrawal to your last-used destination address.

## Forbidden in user-facing copy

By policy, you'll never see Fronex use the words:

* **bet** / **wager** / **gamble**
* **long** / **short** / **leverage**

We use **predict**, **call it**, and **drop a prediction**. This isn't aesthetic — it's part of how we frame the product to ourselves and to regulators. If you see those words in our copy, that's a bug; please tell us.

## Reporting a problem

* **Bug or unexpected behavior**: [admin@fronex.xyz](mailto:admin@fronex.xyz)
* **Security report** (vulnerability disclosure): [admin@fronex.xyz](mailto:admin@fronex.xyz) with subject `SECURITY:` — we'll respond within 24 hours.
* **Suspicious DM claiming to be Fronex**: forward to [admin@fronex.xyz](mailto:admin@fronex.xyz) with the source handle. We will not DM you first; we use the channel and the email only.
* **Account in distress** (you suspect you have a prediction problem, or you're being pressured by another user): email and we will lock the account temporarily while we look into it.

## What we will never do

* Ask for your mnemonic or any other wallet's recovery phrase.
* Promise guaranteed returns or "AI prediction signals."
* DM you first to offer beta access (during closed beta you'll receive a personal invitation from the founder; we never use third-party DMs).
* Run paid promotional campaigns through random influencers without disclosure.
