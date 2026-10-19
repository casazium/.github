# Casazium

**Developer infrastructure for indie software vendors — self-hosted or hosted.**

Casazium is a one-person studio run by Bob Casazza in Merrimack, New Hampshire. Most of the
source is private; this page is here so you can see who's behind it and where to look.

## License Server

Issue, verify, and track product licenses, and gate your own release downloads behind them.
Run it on your own infrastructure, or use the hosted service. It's the same API either way.

- **Hosted:** free for up to 50 active licenses; $39/month ($374/year) for up to 1,000, or
  $79/month ($758/year) for up to 10,000.
- **Self-hosted:** licensed, with no usage limits imposed by Casazium. $399/year
  single-tenant, $1,800/year for multi-tenant deployments, after a 30-day free evaluation
  that starts the first time an installation boots.
  [Contact](https://casazium.com/contact) for a license.
- **Leaving is documented:** hosted accounts can export their data from Settings at any time,
  and a hosted service won't shut down without 90 days' written notice
  ([Terms](https://casazium.com/terms)). Self-hosted licensees get the same notice, plus a
  final build with the license check and all contact with Casazium's servers removed
  ([EULA §8](https://docs.casazium.com/docs/license-server/eula#_8-discontinuation-of-the-software)).

### Selling without writing fulfillment code

Connect a storefront once and every purchase after that issues a license and emails the buyer
their key, with no integration code on your side. **Stripe**, **Lemon Squeezy** and **Paddle**
are supported, including refunds, chargebacks and subscription renewals.

### Getting started

- **Self-hosted:** a [one-command bundle](https://docs.casazium.com/docs/license-server/getting-started/installation)
  — `docker compose up`, with the admin console included and its secrets generated on first boot.
- **In your app:** [`@casazium/license-sdk`](https://www.npmjs.com/package/@casazium/license-sdk)
  on npm, or the plain HTTP API. Worked examples in JavaScript, Python, Java and Go.
- **A working example:** [`license-demo`](https://github.com/casazium/license-demo) — a small
  Electron app showing how a desktop app activates, stores and re-checks a license. MIT, and
  the one piece of Casazium you can read the source of.
- **Guides:** [end-to-end walkthroughs](https://casazium.com/guides) — licensing a desktop app,
  issuing keys from each storefront, offline verification with public-key signatures, and
  licensing server software you ship to customers.

[Documentation](https://docs.casazium.com/docs/license-server/intro) ·
[Pricing](https://casazium.com/pricing) ·
[Self-hosted binaries](https://github.com/casazium/license-releases/releases)

## Also from Casazium

- **[Library Server](https://bibliophilicbob.us/)** — book cataloguing for personal and shared
  libraries: print, ebooks, and audiobooks. Live demo.
- **[Games](https://games.casazium.com)** — released prototypes, free to download. Currently
  Casazium Tank Command, a real-time-strategy prototype built in Godot.
- **Storage Server** — content-addressed object storage with verifiable integrity.
  **Not in development.** Work on it has stopped; don't plan around it.

[Website](https://casazium.com) · [Documentation](https://docs.casazium.com) ·
[Contact](https://casazium.com/contact)
