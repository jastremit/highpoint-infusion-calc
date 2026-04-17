# 🌿 HiPoint Infusion Lab

A personal cannabis infusion toolkit — dosage calculator, strain library, recipe browser, and product pricing tracker — built for home infusers.

**Live site:** [https://jastremit.github.io/highpoint-infusion-calc/](https://jastremit.github.io/highpoint-infusion-calc/)

> **PWA enabled** — install directly to your phone or desktop as an app. Works fully offline.

---

## Files

| File | Purpose |
|---|---|
| `index.html` | Main app — Calculator, History, Tools, Library, Recipes |
| `pricing.html` | Product pricing & expense tracker |
| `manifest.json` | PWA manifest — enables app install |
| `sw.js` | Service worker — enables offline use |

---

## Installing as an App (PWA)

**iPhone / iPad (Safari):**
Tap Share → Add to Home Screen → opens full screen with no browser bar

**Android (Chrome):**
Tap 3-dot menu → Install App (or tap the banner that appears automatically)

**Desktop (Chrome):**
Click the install icon in the address bar

---

## Calculator (`index.html`) — 5 Tabs

### 🧪 Calculator

The core dosage tool.

**Strain search:**
- 2,267 strains from the Leafly public dataset — name, type, effects, terpenes, flavors
- Live autocomplete — dropdown shows strain name, type, and dispensary
- THC/CBD/CBG are **never auto-filled** — always enter from your actual batch label
- Add custom strains via **+ Add New Strain** (saved to browser storage)
- Track dispensary, batch date, and notes per strain
- Duplicate detection — update existing or save as new batch

**Inputs:**
- Strain name (searchable, 2,267 strains)
- Flower weight (grams)
- Carrier: Butter · Coconut Oil · Olive Oil · Avocado Oil · Vegetable Oil · MCT Oil · Honey · Tincture · Veg Glycerin
- Carrier amount (fl oz, minimum 16)
- THC / CBD / CBG % (from your batch label)
- Machine: Magical Butter Machine or LEVO II+
- Batch quality: Good / Average / Rough

**MBM Settings card** — auto-populates when you select a carrier:
- Temperature, infuse time, which button to press
- Source-linked to official MagicalButter.com recipes
- Flammable warning for tincture

**Process efficiency** (tuned to your exact setup):

| Machine | Good | Average | Rough |
|---|---|---|---|
| Magical Butter Machine | 72% | 68% | 63% |
| LEVO II+ | 68% | 65% | 60% |

**Outputs:**
- mg THC / CBD / CBG per tablespoon, teaspoon, and fl oz
- Total active cannabinoids across the full batch
- Strain effects + terpene profile
- Batch summary with machine, efficiency %, carrier, flower weight
- Notes field + Save to History button

---

### 📋 History

- Log of every saved batch
- Shows strain, THC%, mg/tbsp, flower, oil, carrier, machine, dispensary, notes
- Delete individual entries
- Export as printable PDF

---

### 🛠 Tools

**⏱ Decarb Timer**
- 40-minute countdown for 220°F oven decarb (MBM method)
- Start / Pause / Resume / Reset
- Browser notification when complete

**💰 Cost Tracker**
- Enter grams purchased + total cost + THC% + carrier oz
- Returns: cost per gram, cost per mg THC, mg per tbsp of finished oil, input cost per tbsp

**🔄 Reverse Dose Calculator**
- Enter desired mg per piece + number of pieces + THC%
- Returns: how many grams of flower and how much carrier you need

**🍪 Recipe Scaler**
- Enter tbsp of oil in recipe + servings + mg per tbsp
- Returns: mg THC per serving

---

### 📚 Library

- View and delete custom strains you've saved
- Export saved strains as JSON (dated backup file)
- Import JSON to restore or transfer your library

---

### 🍳 Recipes — 27 recipes across 3 categories

**Base Recipes (7) — official MagicalButter.com recipes:**
- Infused Butter · Coconut Oil · Olive Oil · MCT Oil · Honey · Alcohol Tincture · Veg Glycerin Tincture
- Each shows MBM temp, time, button to press, and links to source

**Body Butter (10):**
- Classic Infused Body Butter
- Whipped Rose Body Butter
- Lavender + Eucalyptus Salve
- Chocolate Mint Lotion Bar
- Mango Hibiscus Whipped Butter
- Citrus Glow Body Oil
- Lemon Sugar Body Scrub
- Activated Charcoal + Tea Tree Salve
- Muscle Recovery Balm (arnica + peppermint)
- Blueberry Vanilla Whipped Butter

**Infused Meals (10):**

*Quick (30 min or less):*
- Infused Avocado Toast · Garlic Butter Pasta · Honey Lemon Vinaigrette · Banana Pancakes

*Full Dinners:*
- Herb Roasted Chicken · Coconut Curry · Steak Compound Butter

*Snacks & Appetizers:*
- Stovetop Popcorn · Garlic Bread · Mac & Cheese

Every recipe includes full ingredients, numbered steps, notes, and dosing tips (every infused meal recipe flags when to add infused oil/butter off heat to preserve potency).

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

## Product Pricing Tracker (`pricing.html`)

### 📊 Products Dashboard
All saved products with cost per unit, suggested sell price, and profit margin at a glance.

### ➕ Product Builder
- Name, category (Body Butter, Honey, Meal Prep, Gummies, Other), units per batch
- Add ingredients/materials with full cost-per-batch math
- Add packaging items (jars, lids, labels, bags)
- Labor (hourly rate × hours)
- Target profit margin %
- Live suggested sell price as you add items
- Every ingredient/packaging item supports a purchase link (Amazon, etc.)

### 🧺 Ingredient Library
Reusable ingredient database with cost-per-unit math and source links. Enter total purchased, total amount, and typical batch usage — app calculates cost per batch automatically.

### 🛠 Equipment Log
One-time business expense tracker with name, cost, date, notes, and purchase link. Running total shown.

---

## Process This App Is Tuned For

1. **Decarb:** 220°F / 40 minutes (MBM) or inside machine (LEVO II+)
2. **Infusion:** Magical Butter Machine or LEVO II+
3. **Straining:** Cheesecloth (LEVO built-in strainer not used)
4. **Minimum batch:** 16 fl oz of carrier

---

## Hosting Roadmap

| Phase | Status | Platform |
|---|---|---|
| Personal use | ✅ Live | GitHub Pages |
| Installable app | ✅ Live | PWA |
| Custom domain + selling | 🔜 Next | Netlify + Stripe |
| User accounts + cloud sync | 🔜 Future | React + Supabase |

---

## Tech

- Pure HTML / CSS / JavaScript — no frameworks, no build step, no dependencies
- 2,267 strain dataset from Leafly public data (Kaggle)
- Custom strains and batch history in browser localStorage
- PWA: `manifest.json` + `sw.js` service worker (cache-first, full offline support)
- Single-file architecture for easy version control and deployment
- Hosted free on GitHub Pages

---

*Built for personal use · HiPoint Aesthetics · Portland, OR*
