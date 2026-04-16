# 🌿 HiPoint Infusion Lab

A personal cannabis batch dosage calculator with strain library, process efficiency tracking, batch history, cost tracking, and tools — built for home infusers.

**Live site:** [https://jastremit.github.io/highpoint-infusion-calc/](https://jastremit.github.io/highpoint-infusion-calc/)

---

## Overview

A single-file web app that calculates precise THC/CBD/CBG dosage for home infusion batches. Tuned to real-world process loss for the Magical Butter Machine and LEVO II+. No installs, no accounts, works offline.

---

## Tabs

### 🧪 Calculator
The main dosage calculator. Enter your batch details and get mg breakdowns per tablespoon, teaspoon, and fl oz.

**Strain search:**
- 2,267 strains from the Leafly public dataset — name, type, effects, flavors, terpenes
- Live autocomplete as you type
- Strain selection shows type, effects, and terpenes — **THC/CBD/CBG are never auto-filled**
- You always enter your actual batch % from your dispensary label
- Add your own strains via the **+ Add New Strain** button
- Track which dispensary each batch came from
- Duplicate detection — update existing or save as new batch with date label

**Inputs:**
- Strain name (searchable)
- Flower weight (grams)
- Carrier type: Butter, Coconut Oil, Olive Oil, Avocado Oil, Vegetable Oil, MCT Oil
- Carrier amount (fl oz, minimum 16)
- THC, CBD, CBG % — entered from your actual batch label
- Infusion machine: Magical Butter Machine or LEVO II+
- Batch quality: Good / Average / Rough

**Process efficiency** (tuned to MBM + LEVO II+ + cheesecloth straining):

| Machine | Good | Average | Rough |
|---|---|---|---|
| Magical Butter Machine | 72% | 68% | 63% |
| LEVO II+ | 68% | 65% | 60% |

**Outputs:**
- mg THC / CBD / CBG per tablespoon
- mg per teaspoon
- mg per fl oz
- Total active cannabinoids across the full batch
- Strain effects and terpene profile
- Batch summary (machine, efficiency %, carrier, flower weight)
- Notes field + **Save to History** button

---

### 📋 History
Log of every saved batch.

- Strain, THC%, mg/tbsp, flower weight, oil amount, carrier, machine, efficiency, dispensary
- Your notes per batch
- Delete individual entries
- **Export as printable PDF** for records

---

### 🛠 Tools

**⏱ Decarb Timer**
- 40 min countdown tuned to 220°F oven decarb (MBM method)
- Start / Pause / Resume / Reset
- Browser notification when complete

**💰 Cost Tracker**
- Enter grams purchased + total cost paid + THC% + carrier oz
- Calculates: cost per gram, cost per mg THC, mg THC per tbsp of finished oil, input cost per tbsp
- Useful for pricing gummies, honey, and other infused products

**🔄 Reverse Dose Calculator**
- Enter desired mg per piece + number of pieces + THC%
- Calculates how many grams of flower you need and minimum carrier amount

**🍪 Recipe Scaler**
- Enter tbsp of oil used in recipe + number of servings + mg per tbsp (from calculator)
- Calculates mg THC per serving

---

### 📚 Library
Manage your custom saved strains — view and delete entries you've added.

---

## Strain Color Coding

| Type | Color |
|---|---|
| Indica | 💜 Purple |
| Indica-Dom Hybrid | 💜→💚 Purple-to-green |
| Hybrid | 💚 Green |
| Sativa-Dom Hybrid | 💚→❤️ Green-to-red |
| Sativa | ❤️ Red |

---

## Data Management

- **Export saved strains** as JSON (dated filename) — use to back up your custom library
- **Import JSON** — restore or transfer your strain library between devices
- **Batch history** stored in browser localStorage (up to 50 batches)
- Custom strains persist via browser localStorage

---

## Usage

### Option 1 — Live site
Visit [https://jastremit.github.io/highpoint-infusion-calc/](https://jastremit.github.io/highpoint-infusion-calc/)

### Option 2 — Offline
Download `index.html` and open in any browser. No internet required.

---

## Process This Calculator Is Tuned For

1. **Decarb:** 220°F for 40 minutes in oven (MBM) or inside machine (LEVO)
2. **Infusion:** Magical Butter Machine or LEVO II+
3. **Strain:** Cheesecloth after infusion (LEVO built-in strainer not used)
4. **Minimum batch:** 16 fl oz of carrier

---

## Tech

- Pure HTML / CSS / JavaScript — no frameworks, no build step, no dependencies
- 2,267 strain dataset embedded from Leafly public data (Kaggle)
- Custom strains and batch history stored in browser localStorage
- Single file — easy to update, version control, and host anywhere
- Hosted free on GitHub Pages

---

*Built for personal use · HiPoint Aesthetics · Portland, OR*
