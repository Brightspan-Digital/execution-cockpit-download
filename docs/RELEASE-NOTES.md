# Execution Cockpit 0.5.0 — Public Preview

Released 2026-10-31 · Windows 10 and 11 (64-bit)

| | |
|---|---|
| Installer | `ExecutionCockpit-0.5.0-staging-Setup.exe` |
| Size | 39,176,762 bytes (39.2 MB) |
| SHA-256 | `ec3a309a1402e86312ace37a938551f63b5e16a4ca65511363cb6cbada95b60a` |

> **This is a Public Preview for evaluation and free testing, not the commercial release.** Testing is free and
> **no payment is required**: use the **free 7-day trial** or a **promotional code**. The preview takes no
> payments and its website has no payment method open: **never send real Bitcoin, USDT or any other money.**
> Trials, promotional time and licenses from the preview do not carry over to the commercial release.

## What Execution Cockpit is

Order entry and trade management for your own Interactive Brokers account, through TWS or IB Gateway on the same
Windows computer: hotkeys, broker-side or client-side protective stops, take-profit targets, partial exits
(25 / 50 / 75 %), FLATTEN and EMERGENCY EXIT, account reconciliation, and session recovery after a restart.

It places and manages the orders you choose. It does not predict prices, give trading signals or advice, or make
trading more profitable. Every trading decision and its result are yours.

**Your positions are always yours to manage.** A missing, expired or unreadable license only stops new entries and
adding to a position. Closing, reducing, stops, targets, FLATTEN and EMERGENCY EXIT always work.

## New in 0.5

* The bundled Python runtime is now 3.13.17 (security fixes until October 2029) instead of 3.10, which reached its
  end of life. Same application code and the same pinned libraries, rebuilt for 3.13.
* User Guide: what the program is and is not, system requirements, receipts, cancelling and refunds, and a
  "Limitations and trading risk" section.
* Installer: a short License Agreement page. *View License Agreement* opens the complete agreement in your browser,
  and the *I have read and accept* box continues. The agreement is preliminary, pending professional legal review,
  and is also installed next to the User Guide.

## System requirements

* Windows 10 or 11, 64-bit; about 300 MB free disk space; a screen at least 1280 pixels wide.
* No administrator rights and nothing else to install: no Python, Git or other tools. The program brings its own
  runtime.
* An Interactive Brokers account with TWS or IB Gateway on the same computer (API socket clients enabled,
  Read-Only API off). Real-time market data for quote-based features is bought from Interactive Brokers.

## Getting started

1. [Install](INSTALL.md): download, check the SHA-256, run the installer.
2. [Licensing and activation](LICENSING.md): start the free trial or use a promotional code.
3. Read the User Guide (installed with the program: Start menu → Execution Cockpit → User Guide).
4. Practise with an IBKR **Paper** account first.

Problems or questions: [Support](SUPPORT.md).

## Known limitations

* **Not code-signed yet.** Windows SmartScreen shows "Windows protected your PC" on the first run. Check the
  SHA-256 first, then choose *More info → Run anyway* ([Install](INSTALL.md), step 3).
* The License Agreement is preliminary; the final agreement comes before the commercial release.
* The program's window title still reads "Build 0.4". The program is version 0.5.0 (see *Settings → Apps*).
* Quote-priced orders, dollar or percent sizing of MARKET orders, and client-side protection need real-time
  market data for the symbol in your IBKR account.
* Interactive Brokers triggers broker-side stop orders in regular trading hours only.
* Client-side protection works only while the program runs and is connected.
* Creating a website account may need a manual e-mail confirmation while automatic e-mail is not set up. The free
  trial does not need an account.

## Build information

Version 0.5.0, built 2026-11-01 00:51 UTC (build 4fb4719bb9b8) · publisher BrightSpan Digital · bundled Python 3.13.17, PySide6 6.10.1,
ib_insync 0.9.86, numpy 2.1.3, cryptography 50.0.2. Third-party licenses are installed in the program's
`licenses` folder.

Trading involves substantial risk of loss. Execution Cockpit is trading software, not investment advice.
