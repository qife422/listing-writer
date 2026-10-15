# Listing WriterA 270M-parameter **Gemma 3** running **100% in the browser** (Transformers.js) that turns
a quick item description into a polished eBay / Facebook Marketplace listing.

Built for the **DEV Hacktoberfest 2026 Open-Source AI Challenge — Week 2: Side Hustle**("build something with open-weight models or open-source AI that someone would actually pay for").

## What it does

Describe your item once — photo, brand, condition, flaws — and get back:

- **Title**: SEO-friendly, under 80 characters
- **Description**: honest, buyer-trustworthy, 2–4 sentences
- **Item specifics**: only facts you actually gave it
- **Pricing guidance**: what to check (sold comps), never an invented dollar amount

Each section has a copy button — paste straight into eBay.
## Why open weights

- **Zero marginal cost**: no per-listing API bill, which matters when your margin is $8 on a used headset.
- **Privacy**: your product photos and sourcing notes never leave the device.
- **No lock-in**: swap the model, tweak the prompt, run offline after the first download.

## Honesty rules (in the system prompt)- Never invents brand names, model numbers, or features.
- Refuses counterfeit / replica listings.
- Never hallucinates a price — pricing is guidance, not a number.

## Run it
Open `index.html` in a modern browser (Chrome recommended). First load downloadsthe model (~1 GB, fp32 — see the code note on why fp16/WebGPU is avoided for this model);
after that it is cached and works offline.

No build step, no server, no API key.

## Build log

| Date | Note |
|---|---|
| 2026-10-12 | Scaffolded from the Week 1 Touch Grass Card pipeline (same Gemma 3 270M fp32 setup) |
| 2026-10-12 | Prompt deck: listing-writer system prompt with honesty rules |
| 2026-10-12 | First real listing generated (live Mac test, v2 run): Sony WH-1000XM4 — 52-char title, 4-section output, no invented facts |
| _TBD_ | DEV post published |
