# National Bank of Romania Exchange Rates API — bnr-exchange-rate

[![npm version](https://img.shields.io/npm/v/bnr-exchange-rate.svg)](https://www.npmjs.com/package/bnr-exchange-rate)
[![license](https://img.shields.io/npm/l/bnr-exchange-rate.svg)](https://github.com/AllRates-Today/bnr-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/bnr-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![EUR/RON today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fbnr%3Fsource%3DEUR%26target%3DRON&query=%24.rate&label=EUR%2FRON%20published%20by%20National%20Bank%20of%20Romania&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/bnr/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fbnr%3Fsource%3DEUR%26target%3DRON&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/bnr/)

**Official National Bank of Romania (Romania) daily exchange rates for Node.js and TypeScript. The published central bank rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers National Bank of Romania itself prints, every business day.**

## 🚀 Why this client?

- 🏛️ **Official published rates** — National Bank of Romania's own table, with the publisher's own `rate_date` on every response
- 📅 **History back to 2005** — point-in-time tables and daily series for any past date
- 🔀 **Published vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number National Bank of Romania itself published, fixed once printed and carrying the central bank's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## ⚡ Try it without a key

The latest National Bank of Romania table is also served keyless, CORS-open and edge-cached, for evaluation, embeds and AI agents:

```bash
curl "https://allratestoday.com/api/open/central-bank/bnr?source=EUR&target=RON"
```

```js
const r = await fetch('https://allratestoday.com/api/open/central-bank/bnr').then((x) => x.json());
console.log(r.rate_date, r.rates.length); // the central bank's latest published table, no key
```

The open endpoint serves the *latest* table only (JSON by default; add `?format=csv`, `xml` or `xlsx` for a file) and is free to use with a visible, followable link where the rates are shown: `<a href="https://allratestoday.com">Exchange rates by AllRatesToday</a>` (terms: <https://allratestoday.com/terms/#attribution>). The client below uses the keyed API, which adds point-in-time tables and history; with a key the link is appreciated, not required.

## 📈 Latest published table

[![Latest National Bank of Romania table](https://allratestoday.com/api/open/central-bank/bnr/table.svg)](https://allratestoday.com/central-bank-rates-api/bnr/)

The image is rendered live from the keyless endpoint above, so it follows the central bank's publications on npm and on GitHub alike without a new release. The same table as text is folded below for search and copy-paste: on GitHub [a daily Action](.github/workflows/daily-table.yml) refreshes it whenever the central bank publishes a new table; on npm it is as of the package's publish date.

<!-- daily-table:start -->
<details>
<summary>Table as text: published 2026-10-27 by National Bank of Romania — 37 rates. Updated 2026-10-27.</summary>

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| AED | RON | reference | 1.3063 |
| AUD | RON | reference | 3.374 |
| BRL | RON | reference | 0.8931 |
| CAD | RON | reference | 3.4236 |
| CHF | RON | reference | 5.7921 |
| CNY | RON | reference | 0.7196 |
| CZK | RON | reference | 0.2197 |
| DKK | RON | reference | 0.7156 |
| EGP | RON | reference | 0.0854 |
| EUR | RON | reference | 5.3487 |
| GBP | RON | reference | 6.3892 |
| HKD | RON | reference | 0.6116 |
| HUF | RON | reference | 0.014577 |
| IDR | RON | reference | 0.000264 |
| ILS | RON | reference | 1.5696 |
| INR | RON | reference | 0.0504 |
| ISK | RON | reference | 0.039213 |
| JPY | RON | reference | 0.030431 |
| KRW | RON | reference | 0.003613 |
| MDL | RON | reference | 0.2646 |
| MXN | RON | reference | 0.2579 |
| MYR | RON | reference | 1.1735 |
| NOK | RON | reference | 0.5148 |
| NZD | RON | reference | 2.7348 |
| PHP | RON | reference | 0.0749 |
| PLN | RON | reference | 1.2145 |
| RSD | RON | reference | 0.0455 |
| RUB | RON | reference | 0.0595 |
| SEK | RON | reference | 0.4824 |
| SGD | RON | reference | 3.7451 |
| THB | RON | reference | 0.1422 |
| TRY | RON | reference | 0.0962 |
| UAH | RON | reference | 0.1052 |
| USD | RON | reference | 4.7977 |
| XAU | RON | reference | 19253.5 |
| XDR | RON | reference | 6.49 |
| ZAR | RON | reference | 0.2881 |

</details>

Source: [Official rates published by BNR, served by AllRatesToday](https://allratestoday.com/central-bank-rates-api/bnr/). Rates are as printed by the central bank; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 📦 Installation

```bash
npm install bnr-exchange-rate
```

```bash
yarn add bnr-exchange-rate
```

```bash
pnpm add bnr-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/bnr-exchange-rate`](https://www.npmjs.com/package/@allratestoday/bnr-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'bnr-exchange-rate';

const pair = await getRate('EUR', 'RON', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official National Bank of Romania rate, on the central bank's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest published table
- [Full published table](#full-published-table) — everything the central bank printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the central bank does not print directly are resolved from its table and flagged (see *Published vs derived rates* below).

```js
const pair = await getRate('EUR', 'RON', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'bnr',
  name: 'National Bank of Romania',
  rate_date: '2026-10-14',   // National Bank of Romania's own publication date
  source: 'EUR',
  target: 'RON',
  rate: 5.3393,
  rate_type: 'reference',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full published table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'bnr-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'bnr',
  name: 'National Bank of Romania',
  rate_date: '2026-10-14',
  rates: [
    { "base": "EUR", "quote": "RON", "type": "reference", "value": 5.3393 },
    // … the rest of the published table (37 currencies vs RON)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 2005 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'bnr-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'EUR', target: 'RON' });
```

**Response:**

```javascript
{
  bank: 'bnr',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'bnr-exchange-rate';

const series = await getHistory(
  { source: 'EUR', target: 'RON', from: '2026-01-01', to: '2026-10-14' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'bnr',
  source: 'EUR',
  target: 'RON',
  from: '2026-01-01',
  to: '2026-10-14',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-10-14', rate: 5.3393, rate_type: 'reference', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'EUR' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

National Bank of Romania currently publishes rates covering **37 currencies** against the RON (as of the latest table):

🇦🇪 `AED` · 🇦🇺 `AUD` · 🇧🇷 `BRL` · 🇨🇦 `CAD` · 🇨🇭 `CHF` · 🇨🇳 `CNY` · 🇨🇿 `CZK` · 🇩🇰 `DKK` · 🇪🇬 `EGP` · 🇪🇺 `EUR` · 🇬🇧 `GBP` · 🇭🇰 `HKD` · 🇭🇺 `HUF` · 🇮🇩 `IDR` · 🇮🇱 `ILS` · 🇮🇳 `INR` · 🇮🇸 `ISK` · 🇯🇵 `JPY` · 🇰🇷 `KRW` · 🇲🇩 `MDL` · 🇲🇽 `MXN` · 🇲🇾 `MYR` · 🇳🇴 `NOK` · 🇳🇿 `NZD` · 🇵🇭 `PHP` · 🇵🇱 `PLN` · 🇷🇸 `RSD` · 🇷🇺 `RUB` · 🇸🇪 `SEK` · 🇸🇬 `SGD` · 🇹🇭 `THB` · 🇹🇷 `TRY` · 🇺🇦 `UAH` · 🇺🇸 `USD` · `XAU` · `XDR` · 🇿🇦 `ZAR`

## 🏛️ Source

The National Bank of Romania announces the leu's official reference rates for around 37 currencies each business day at about 13:00 Bucharest time — the rate Romanian accounting, tax, and customs rules reference for leu conversion.

- Publisher's own page: [Exchange rates — XML feeds](https://www.bnr.ro/en/24006-exchange-rate-list-in-xml-format) · [www.bnr.ro/en](https://www.bnr.ro/en)
- Publication: every business day; the exact schedule, freshness status and any current delay are on the [National Bank of Romania rates page](https://allratestoday.com/central-bank-rates-api/bnr/)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- National Bank of Romania quotes **RON per 1 unit of foreign currency** (e.g. `base: "USD", quote: "RON"` means RON per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- Precious-metal codes (`XAU`, `XAG`, `XPT`, `XPD`) are quoted **per troy ounce**.
- `rate_type` tells you which of the central bank's series a row belongs to (`reference` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official National Bank of Romania rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/bnr/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('bnr')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate bnr ...` command
- Evaluating? Agents can self-issue a trial key with no signup: `POST https://allratestoday.com/api/agent/keys` (send `Content-Type: application/json`) returns a 100-call key valid 7 days that covers the free-plan methods (latest table, pairs); dated tables and history need a [paid plan](https://allratestoday.com/pricing/). The MCP servers expose it as `request_trial_key`
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Published vs derived rates

If National Bank of Romania does not print a pair directly, the API resolves it from the central bank's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The central bank printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via RON from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('EUR', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by National Bank of Romania |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'bnr-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('bnr-exchange-rate');

getRate('EUR', 'RON', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once per business day — cache the published table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the published table |
| `getLatestRates({ apiKey })` | Free | The central bank's full latest published table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 2005 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same published tables are mirrored daily as open data:

- Hugging Face: [AllRatesToday/central-bank-exchange-rates](https://huggingface.co/datasets/AllRatesToday/central-bank-exchange-rates) — one CSV per institution (`rates/bnr.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- Raw JSON on GitHub: `https://raw.githubusercontent.com/AllRates-Today/central-bank-exchange-rates/main/data/bnr/latest.json`

## 🔗 Links

- [National Bank of Romania rates page](https://allratestoday.com/central-bank-rates-api/bnr/) — live table, publication cadence, FAQ
- [All central bank sources](https://allratestoday.com/central-bank-rates-api/)
- [Package docs on the site](https://allratestoday.com/docs/sdk/bnr-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (Free)](https://allratestoday.com/register) · [Dashboard](https://allratestoday.com/profile) · [Pricing](https://allratestoday.com/pricing/)
- [Status](https://allratestoday.com/status)
- [Postman collection](https://allratestoday.com/postman/)
- [GitHub](https://github.com/AllRates-Today/bnr-exchange-rate)

## 📜 License

MIT
