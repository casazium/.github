# Casazium

**Licensing infrastructure for indie software vendors, and tools for the people who debug HTTP.**

Casazium is a one-person studio run by Bob Casazza in Merrimack, New Hampshire. Most of the
source is private — Wirescry's core is the exception — so this page is here to show you who's
behind it and where to look.

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
  small enough to read in one sitting.
- **Guides:** [end-to-end walkthroughs](https://casazium.com/guides) — licensing a desktop app,
  issuing keys from each storefront, offline verification with public-key signatures, and
  licensing server software you ship to customers.

[Documentation](https://docs.casazium.com/docs/license-server/intro) ·
[Pricing](https://casazium.com/pricing) ·
[Self-hosted binaries](https://github.com/casazium/license-releases/releases)

## Wirescry

**See and change your app's HTTP traffic.** Launch a browser or a terminal from Wirescry and
its traffic appears — decrypted, formatted and searchable. Nothing is installed system-wide, no
certificate is added to your machine's trust store and your system proxy settings are untouched,
so there is nothing to undo when you close it.

- **The free app is the whole tool, not a trial.** Every HTTP and HTTPS request and response,
  filters like `status>=400` or `host=api.*`, bodies decoded from gzip, Brotli or zstd and
  formatted rather than dumped, and one-click launching of browsers, terminals and the Docker
  containers they start. macOS, Windows and Linux, with no time limit and no account.
- **Open source**, AGPL-3.0: [`casazium/wirescry`](https://github.com/casazium/wirescry).
- **No telemetry** — no analytics, no usage tracking and no crash reporting anywhere in the app.
  HTTPS is decrypted with a certificate authority generated on your own computer the first time
  it starts, and intercepted traffic is never sent to Casazium: it goes where it was already
  headed, or wherever your own rules send it.
- **Pro** adds the parts that change traffic: rules (mock, reply from a file, forward, rewrite,
  simulate failures), breakpoints, saved requests, variables, Copy as code, and checking traffic
  against your OpenAPI specs. **$59/year founding price until 1 May 2027, $79/year after**, three
  computers, a 14-day free trial and 30-day refunds. Students 50% off; free for maintainers of
  active open-source projects. If you stop paying, Pro keeps working in every version released
  while you were subscribed, on the computers where it is activated.

[Download](https://github.com/casazium/wirescry-releases/releases) ·
[Documentation](https://docs.casazium.com/docs/wirescry/intro) ·
[Product page](https://casazium.com/wirescry) ·
[Source](https://github.com/casazium/wirescry)

## Also from Casazium

- **[Library Server](https://bibliophilicbob.us/)** — book cataloguing for personal and shared
  libraries: print, ebooks, and audiobooks. Live demo.
- **[Games](https://games.casazium.com)** — released prototypes, free to download. Currently
  Casazium Tank Command, a real-time-strategy prototype built in Godot.
- **Storage Server** — content-addressed object storage with verifiable integrity.
  **Not in development.** Work on it has stopped; don't plan around it.

[Website](https://casazium.com) · [Documentation](https://docs.casazium.com) ·
[Contact](https://casazium.com/contact)
