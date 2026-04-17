# 🌿 HiPoint Infusion Lab

A personal cannabis infusion toolkit — dosage calculator, strain library, recipe browser with yield/dosing calculator, batch planner, and product pricing tracker — built for home infusers.

**Live site:** [https://jastremit.github.io/highpoint-infusion-calc/](https://jastremit.github.io/highpoint-infusion-calc/)

> **PWA enabled** — install directly to your phone or desktop. Works fully offline.

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
Tap Share → Add to Home Screen → opens full screen, no browser bar

**Android (Chrome):**
Tap 3-dot menu → Install App (or tap the install banner automatically)

**Desktop (Chrome):**
Click the install icon in the address bar

---

## Calculator (`index.html`) — 5 Tabs

### 🧪 Calculator

**Strain search:**
- 2,267 strains from the Leafly public dataset — name, type, effects, terpenes, flavors
- Live autocomplete dropdown shows strain name, type badge, and dispensary
- THC/CBD/CBG are **never auto-filled** — always enter from your actual batch label
- Add custom strains via **+ Add New Strain** with duplicate detection
- Track dispensary, batch date, and notes per strain

**Inputs:**
- Strain name (searchable, 2,267 strains)
- Flower weight (grams)
- Carrier: Butter · Coconut Oil · Olive Oil · Avocado Oil · Vegetable Oil · MCT Oil · Honey · Tincture · Veg Glycerin
- Carrier amount (fl oz, minimum 16)
- THC / CBD / CBG % (from your batch label)
- Infusion Method: Magical Butter Machine · LEVO II+ · Manual
- Batch quality: Good / Average / Rough

**Method Settings card** — auto-populates when you select a carrier:
- Temperature, infuse time, and button to press (MBM/LEVO) or stir instructions (Manual)
- Adapts automatically when switching between methods
- Source-linked to official MagicalButter.com recipes (MBM/LEVO)
- Red flammable warning for tincture on all methods

**Process efficiency:**

| Method | Good | Average | Rough |
|---|---|---|---|
| Magical Butter Machine | 72% | 68% | 63% |
| LEVO II+ | 68% | 65% | 60% |
| Manual (double boiler / crockpot) | 65% | 60% | 55% |

**Outputs:**
- mg THC / CBD / CBG per tablespoon, teaspoon, and fl oz
- Total active cannabinoids across full batch
- Strain effects + terpene profile
- Batch summary (method, efficiency %, carrier, flower weight)
- Notes field + Save to History button

**Active Batch Save:**
Every time you calculate, the app saves your batch (strain, mg/tbsp, carrier, THC%, method, timestamp) to storage. Persists across sessions and pre-fills the dosing calculator in every recipe automatically.

---

### 📦 Batch Planner (appears automatically after calculating)

Shows below the results card after every calculation.

- **Estimated oil recovery** — input oz × straining yield % (default 85% for cheesecloth, adjustable via slider)
- **Product selector** — choose any body butter or meal recipe
- **Custom tbsp field** — enter your own oil-per-batch amount for any recipe not listed
- **Live output:**
  - Full batches possible from your recovered oil
  - Total jars / units produced
  - Per-batch and total product weight
  - Leftover oil note

Example: 32 fl oz MCT oil at 85% = ~27 fl oz recovered = **13 batches of body butter = 104 × 2oz jars**

---

### 📋 History

- Full log of every saved batch
- Strain, THC%, mg/tbsp, flower, oil, carrier, method, dispensary, notes
- Delete individual entries
- Export as printable PDF

---

### 🛠 Tools

**⏱ Decarb Timer** — 40-min countdown at 220°F, pause/resume, browser notification on complete

**💰 Cost Tracker** — grams + cost + THC% + carrier oz → cost per gram, cost per mg THC, mg/tbsp of finished oil, input cost per tbsp

**🔄 Reverse Dose Calculator** — target mg per piece + pieces + THC% → grams of flower and carrier needed

**🍪 Recipe Scaler** — tbsp of oil + servings + mg/tbsp → mg per serving

---

### 📚 Library

- View and delete custom saved strains
- Export strains as JSON (dated backup)
- Import JSON to restore or transfer your library

---

### 🍳 Recipes — 27 recipes across 3 categories

**Browse by:** All · Base Recipes · Body Butter · Infused Meals · My Recipes

**Search:** by name, ingredient, tag, or description

---

#### Base Recipes (7) — official MagicalButter.com recipes
Each shows temp, infuse time, which button to press, and links to the source recipe.

- 🧈 Infused Butter — 160°F · 2 hrs · 2 HR BUTTER
- 🥥 Infused Coconut Oil — 160°F · 2 hrs · 2 HR OIL
- 🫒 Infused Olive Oil — 160°F · 1 hr · 1 HR OIL
- 💧 Infused MCT Oil — 160°F · 1 hr · 1 HR OIL
- 🍯 Infused Honey — 130°F · 1 hr · 1 HR OIL
- 🧪 Alcohol Tincture — 130°F · 4–8 hrs · 4 HR TINCTURE ⚠️ flammable
- 🌿 Vegetable Glycerin Tincture — 130°F · 4–8 hrs · 4 HR TINCTURE

#### Body Butter (10)
- 🧴 Classic Infused Body Butter (shea + mango butter)
- 🌹 Whipped Rose Body Butter
- 🌿 Lavender + Eucalyptus Salve
- 🍫 Chocolate Mint Lotion Bar
- 🌸 Mango Hibiscus Whipped Butter
- ☀️ Citrus Glow Body Oil
- 🍋 Lemon Sugar Body Scrub
- 🖤 Activated Charcoal + Tea Tree Salve
- 💪🏽 Muscle Recovery Balm (arnica + peppermint)
- 🫐 Blueberry Vanilla Whipped Butter

#### Infused Meals (10)
*Quick (30 min or less):* Avocado Toast · Garlic Butter Pasta · Honey Lemon Vinaigrette · Banana Pancakes

*Full Dinners:* Herb Roasted Chicken · Coconut Curry · Steak Compound Butter

*Snacks & Appetizers:* Stovetop Popcorn · Garlic Bread · Mac & Cheese

Every recipe flags exactly when to add infused oil/butter off heat to preserve potency.

---

### 📊 Yield & Dosing Calculator (inside every recipe)

Built into the detail view of every non-base recipe.

- **Your oil potency (mg/tbsp)** — auto pre-fills from your last calculated batch
- **Infused oil in recipe (tbsp)** — how much your recipe calls for
- **Scale: 1× · 2× · 3× · custom** — scales ingredient amounts and total mg
- **Servings +/−** — divides total mg across portions, independent from scale

Live output: infused oil scaled, total THC in recipe, mg per serving.

---

### 📦 Batch Yield & Packaging (inside every body butter / product recipe)

- **Total batch yield** — oz and grams
- **Per serving fill** — oz, grams, and tbsp
- **Suggested jar size**
- **Jar Size Calculator** — tap 0.5 / 1 / 2 / 4 / 8 oz or enter custom
  - Shows: full jars from this batch, fill each jar to X grams, leftover
  - Reminder: tare your jar on a scale, fill to target grams every time

Meal recipes show serving count and portion description. Base recipes show variable yield note.

---

### ⚗️ Active Batch Banner

When you open the Recipes tab after calculating, a green banner shows your active batch pre-filled in every recipe's dosing calculator. Persists across sessions until you run a new batch or tap Clear.

---

### ✦ Add Your Own Recipe

Tap **+ Add** in the Recipes tab. Includes name, emoji, category, description, difficulty, time, infused ingredient amount and carrier, total yield, default servings, dynamic ingredient and step builder, and notes. Saved recipes appear in **My Recipes** with a ✦ badge.

---

## Strain Color Coding

| Type | Color |
|---|---|
| Indica | 💜 Purple |
| Indica-Dom Hybrid | 💜→💚 |
| Hybrid | 💚 Green |
| Sativa-Dom Hybrid | 💚→❤️ |
| Sativa | ❤️ Red |

---

## Product Pricing Tracker (`pricing.html`)

### 📊 Products Dashboard
All saved products with cost per unit, suggested sell price, and margin at a glance. Business summary shows avg cost, avg sell price, and total equipment investment.

### ➕ Product Builder
- Name, category (Body Butter, Honey, Meal Prep, Gummies, Other), units per batch
- Ingredients/materials — total cost + total amount + amount per batch → auto cost per batch
- Packaging (jars, lids, labels, bags) with same math
- Labor (hourly rate × hours)
- Target profit margin %
- Live suggested sell price
- Every item supports a purchase link (Amazon, etc.)

### 🧺 Ingredient Library
Reusable ingredients with cost-per-unit math and source links.

### 🛠 Equipment Log
One-time business expenses with name, cost, date, notes, and purchase link. Running total at bottom.

---

## Process This App Is Tuned For

1. **Decarb:** 220°F / 40 min oven (or inside LEVO II+)
2. **Infusion:** Magical Butter Machine, LEVO II+, or manual double boiler / crockpot
3. **Straining:** Cheesecloth
4. **Minimum batch:** 16 fl oz carrier

---

## Hosting Roadmap

| Phase | Status | Platform |
|---|---|---|
| Personal use | ✅ Live | GitHub Pages |
| Installable app | ✅ Live | PWA (offline capable) |
| Custom domain + selling | 🔜 Next | Netlify + Stripe |
| User accounts + cloud sync | 🔜 Future | React + Supabase |

---

## Tech

- Pure HTML / CSS / JavaScript — no frameworks, no build step, no dependencies
- 2,267 strain dataset from Leafly public data (Kaggle)
- All user data (strains, batches, recipes, active batch) in browser localStorage
- PWA: `manifest.json` + `sw.js` service worker (cache-first, full offline support)
- Single-file architecture — easy to version control and deploy anywhere
- Hosted free on GitHub Pages

---

*Built for personal use · HiPoint Aesthetics · Portland, OR*
