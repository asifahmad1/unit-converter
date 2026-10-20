# Unit Converter

By **Dr. Asif Ahmad** — Asif SaaS Studio

Category **Productivity** · Version **1.0** · MIT License

Convert length, weight, volume, temperature, area, currency and digital storage — instantly, in your browser.

## Run it

Open `index.html` in any modern browser, or serve this folder with any static host. No build step, no dependencies, no server. Everything works offline except the optional live currency-rate refresh, which needs an internet connection.

## What it does

- **7 categories, 66 units** — Length (mm–miles), Weight (mg–stone), Volume (mL, litres, US cooking units, US & UK gallons), Temperature (°C / °F / K by exact formula), Area, Currency (20 currencies), Digital storage.
- **Area includes marla & kanal** — the Pakistani land units most converters omit (1 marla = 272.25 ft², 1 kanal = 20 marla), alongside m², ft², acres and hectares.
- **Currency with live rates** — fetched keyless from open.er-api.com (no account, no API key, no backend) and labelled LIVE with the update time; offline it falls back to a built-in snapshot dated 20 Oct 2026 that is always labelled "indicative", never presented as live. Reference-grade rates — not for trade settlement.
- **Digital storage in both families** — SI (KB = 1,000 bytes) and IEC (KiB = 1,024 bytes) side by side, so the two are never confused.
- **Swap, Clear, Copy result** — one tap reverses direction, one tap empties the field, one tap copies the result line.
- **"In every unit" table** — each entered value shown in every unit of its category at once, plus a "1 unit = X units" factor line.
- **Forgiving input, strict validation** — accepts `1,234.5`, `.5`, `-3`, `1e3`; rejects `abc`, `1.2.3`, `NaN`, `Infinity` with a plain-language error; an empty field is a neutral state.

## Files

- `index.html` — the complete app, self-contained: all CSS and JavaScript inline, 17,397 bytes. No localStorage, no service workers, no browser permissions, no parent-window access — safe in a sandboxed iframe.
- `unit-converter-test-report.md` — the full test report with the Wix listing fields and the post-upload testing checklist.
- Documentation (PDF) → `docs/unit-converter-docs.pdf` — user guide & technical documentation (11 pages).

## Testing

3,208 automated checks run against the shipped PURE CORE in Node — **all passed, 0 failed**: exact international definitions (1 in = 2.54 cm, 1 lb = 0.45359237 kg, 1 US gal = 3.785411784 L, 1 kanal = 20 marla…), temperature identities (0 °C = 32 °F, −40 °C = −40 °F, 0 °C = 273.15 K), currency maths against the built-in snapshot plus cross-rate consistency, round-trip sweeps of every unit pair in every category, and the full input-validation set.

## Documentation

Full documentation: `docs/unit-converter-docs.pdf` — categories and factors, how conversion works, the currency design (live fetch + dated indicative fallback), validation rules, interface walkthrough, verification summary, and the tested core verbatim in the appendix.

Created by Dr. Asif Ahmad · Asif SaaS Studio · v1.0
