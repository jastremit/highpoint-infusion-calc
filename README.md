# 🌿 Highpoint Infusion Lab

A personal cannabis batch dosage calculator with built-in strain library, process efficiency tracking, and batch history.

**Live site:** [https://jastremit.github.io/highpoint-infusion-calc/](https://jastremit.github.io/highpoint-infusion-calc/)

---

## What it does

Calculates precise THC/CBD/CBG dosage per tablespoon, teaspoon, and fl oz for home infusion batches — tuned to your specific machine, batch quality, and infusion process.

---

## Features

### Strain library
- 128 preloaded strains with full profiles (type, THC/CBD/CBG%, effects, terpenes, flavors)
- Live autocomplete as you type
- Auto-fills cannabinoid percentages when a strain is selected
- Add your own strains through the interface
- Track which dispensary each batch came from
- Duplicate detection — update existing or save as new batch

### Color-coded strain types
- 💜 **Indica** — Purple
- 💜→💚 **Indica-Dominant Hybrid** — Purple-to-green gradient
- 💚 **Hybrid** — Green
- 💚→❤️ **Sativa-Dominant Hybrid** — Green-to-red gradient
- ❤️ **Sativa** — Red

### Infusion inputs
- Flower weight (grams)
- Carrier type: Butter, Coconut Oil, Olive Oil, Avocado Oil, Vegetable Oil, MCT Oil
- Carrier amount (fl oz, minimum 16 oz)
- THC, CBD, and CBG percentages
- Infusion machine: Magical Butter Machine or LEVO II+
- Batch quality: Good / Average / Rough

### Process efficiency (tuned to real-world workflow)
Accounts for decarb loss, heat degradation, and cheesecloth strain loss.

| Machine | Good | Average | Rough |
|---|---|---|---|
| Magical Butter Machine | 72% | 68% | 63% |
| LEVO II+ | 68% | 65% | 60% |

### Outputs
- mg THC / CBD / CBG **per tablespoon**
- mg per teaspoon
- mg per fl oz
- Total active cannabinoids across the full batch
- Strain effects + terpene profile displayed with results
- Batch summary (machine, efficiency %, carrier, flower weight)

### Data management
- **Export** saved strains as JSON (dated filename)
- **Import** JSON to restore or share strain libraries
- Strains saved locally to browser storage for persistence

---

## Usage

### Option 1: Use the live site
Visit [https://jastremit.github.io/highpoint-infusion-calc/](https://jastremit.github.io/highpoint-infusion-calc/)

### Option 2: Use offline
Download `index.html` and open in any browser. No installs, no dependencies, works completely offline.

---

## Process this calculator is tuned for

1. **Decarb:** 220°F for 40 minutes in oven (for MBM) or inside machine (for LEVO)
2. **Infusion:** Either Magical Butter Machine or LEVO II+
3. **Strain:** Cheesecloth after infusion (built-in LEVO strainer is not used — too many particles pass through)
4. **Minimum batch:** 16 fl oz of carrier

---

## Roadmap

Features under consideration:

- Batch history log (save past calculations with dates)
- Reverse dose calculator ("I want X mg per piece, how much oil per piece?")
- Recipe scaler
- Cost tracking per mg THC
- Edit/delete saved strains
- Notes field per batch
- PDF export of batch records
- Built-in decarb timer

---

## Tech notes

- Pure HTML/CSS/JS — no frameworks, no build step
- Strain library stored in-file as JSON
- Custom strains persist via browser localStorage
- Hosted free on GitHub Pages

---

*Built for personal use by Jas · HiPoint Aesthetics*