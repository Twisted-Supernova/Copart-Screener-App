# 🚗 Copart UK Deal Screener v6

A fast GO / NO-GO tool for screening Copart UK auction deals — built for use at auction, on a phone or desktop.

## 📋 What It Does

- ✅ Instant GO / NO-GO verdict from just two inputs (hammer + resale)
- ✅ Maximum bid calculator — know your walk-away number before bidding starts
- ✅ Full cost breakdown (hammer, Fee B, internet fee, retrieval, repairs, transport, HPI, insurance, advertising, MOT, Cat S re-inspection, V5C replacement)
- ✅ Red & amber flags for common deal-killers
- ✅ Budget cap warning at £9k (amber) and £10k (red)
- ✅ Buying discount check — flags if you're overpaying vs clean retail for your category
- ✅ Save & compare multiple deals side by side
- ✅ Deals persist across browser sessions (localStorage)
- ✅ Load any saved deal back into the screener to re-evaluate
- ✅ Export saved deals to CSV

## 💰 Built Around

- 2026 Copart Fee B schedule
- Budget up to £10,000 per deal
- £500 minimum profit target (£750 when all-in exceeds £5k)
- Pre-bid saves exactly £12.60 on the internet fee across all price tiers

## 🚀 How To Use

1. Open `copart_deal_screener_v6.html` in any browser
2. Enter **Hammer Price** and **Resale Price** (★ starred fields) — you get an instant verdict
3. Add repairs, transport and other costs to sharpen the numbers
4. Fill in vehicle details and run the red flag checks
5. Check the sticky results panel on the right — verdict, max bid, and cost breakdown update live
6. Don't bid above the maximum bid figure
7. Hit **Save This Deal** to add it to your comparison list

## 🧭 Field Guide

### ★ Required for a verdict
| Field | Notes |
|-------|-------|
| Hammer Price | Your expected winning bid (excluding fees) |
| Your Resale Price | Realistic quick-sale price — private sellers, lowest 3–5 listings, minus 5–10% |

### Step 2 — Your Costs (optional but recommended)
| Field | Notes |
|-------|-------|
| Repairs | Pre-contingency estimate — tool adds 20% buffer by default |
| Transport | Recovery/delivery to your location |
| Lot Type | VAT Margin (most lots) or VAT Qualifying (+20% on hammer). VAT-registered buyers can reclaim VAT Qualifying uplift — seek advice if applicable |
| Condition | Non-runner adds transport risk warning |
| 20% contingency | Checked by default — uncheck only if quotes are firm |
| Pre-bid | Saves £12.60 on internet fee — check if you intend to pre-bid |
| MOT needed | Adds £55 to costs |

### Step 3 — Vehicle Details (optional, for records)
Make, model, year, lot number, auction date, mileage, category, keys, V5C

### Step 4 — Resale Guidance (optional)
Enter the clean retail price (Autotrader private) to get suggested resale ceilings by category and a buying-discount health check.

### Step 5 — Red Flag Checks
Any box ticked triggers an automatic **NO GO** regardless of the numbers:
- Outstanding finance on HPI
- Mileage discrepancy on MOT history
- Structural / chassis damage visible in photos
- Repair quotes vary wildly (hidden damage likely)

## 🚦 Verdict Logic

| Verdict | Condition |
|---------|-----------|
| **GO** | No hard stops, profit ≥ £500 (or £750 if all-in > £5k) |
| **NO GO — walk away** | Hard stop flag triggered (Cat A/B, no keys, finance, mileage discrepancy, structural damage, wild quotes) |
| **NO GO — margin too thin** | Profit below the minimum target at the current hammer price |

## 🔴 Hard Stops (always NO GO regardless of price)

- Cat A or Cat B vehicle
- No keys included
- Outstanding finance on HPI check
- Mileage discrepancy on MOT history
- Structural / chassis damage visible
- Repair quotes vary wildly

## 🟡 Amber Warnings (caution — check before bidding)

- No V5C (£25 DVLA V62 replacement cost added automatically)
- VAT Qualifying lot
- Non-runner condition
- Cat S (re-inspection required, £150 added)
- Cat N (permanent HPI marker, disclosure required on sale)
- Buying discount below framework target for the category
- All-in cost within 10% of £10,000 budget cap

## 🔧 v6 Changes

- 🏗 **Redesigned layout** — sticky results panel on the right; inputs reordered with the two required fields (hammer + resale) at the top
- ⭐ **Required field markers** — clear ★ indicators so you know what's needed for a verdict
- 💷 **£ prefix** on every monetary input field
- 🔢 **Numbered steps** (1–5) to guide you through the form
- 💾 **localStorage persistence** — saved deals survive page refreshes
- 📂 **Load** button on saved deals — reload any deal back into the screener
- 📊 **Export CSV** — download all saved deals to a spreadsheet
- 📍 **Lot number + Auction date** fields added
- 🚨 **Budget cap warning** — amber at 90% of £10k, red when over
- 🔍 **Buying discount check extended** to clean title deals (not just Cat N/S)
- 🔄 **Reset / New Deal** button (now a subtle link — won't be clicked by accident)
- 🐛 Various bug fixes: fee calculation guard on empty hammer, profit guard on empty resale, max bid now correctly uses pre-bid checkbox state

## 📂 Companion Files

- `Copart_Car_Flipping_Framework.docx` — full strategy guide
- `Copart_Deal_Calculator.xlsx` — spreadsheet version
