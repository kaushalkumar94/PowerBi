# 06 — Conditional Formatting

## What is Conditional Formatting?

Conditional Formatting in Power BI lets you **automatically format cells based on data rules** — making patterns, outliers, and rankings instantly visible without the reader having to analyze raw numbers.

Applied to **Table** and **Matrix** visuals.

---

## What Was Built

Two tables using the **Apocalypse Store** dataset, both showing `Product Name`, `Price`, `Sum of Units Sold`, and `Sum of Revenue`.

![Conditional Formatting Tables](.01_conditional_formatting/screenshots/conditional_formatting.png)

---

## Table 1 — Background Color + Icons + Data Bars

### Price — Background Color by Rules

Cells are color-coded based on price tier:

| Price Range | Color | Example Products |
|-------------|-------|-----------------|
| Low (< ~10) | 🟢 Green | N95 Mask (2.75), Duct Tape (6.25), Waterproof Matches (7.99) |
| Mid (~10–45) | 🟠 Orange | Solar Flashlight (26.49), Water Purifier (30.25), Backpack (39.99) |
| High (> 45) | 🔴 Red | Stainless Steel Axe (45.50), Weatherproof Jacket (79.99) |

### Sum of Units Sold — Data Bars

Green horizontal bars represent units sold proportionally inside each cell:

- Multitool Survivial Knife **(477)** → longest bar
- Waterproof Matches **(190)** and Solar Battery Flashlight **(182)** → shorter bars

### Sum of Units Sold — Icons

Icons appear alongside the data bars to signal performance tier:

| Icon | Meaning |
|------|---------|
| 🔺 Orange Triangle | Mid-range |
| 🔷 Orange Diamond | Below average |
| ⬤ Grey Circle | Average |

---

## Table 2 — Data Bars + Font Color on Revenue

### Sum of Revenue — Data Bars (Dark Green)

Proportional bars make revenue comparison instant across products:

| Product | Revenue | Rank |
|---------|---------|------|
| Weatherproof Jacket | 13,091.00 | 1st — longest bar |
| Multitool Survivial Knife | 8,781.57 | 2nd |
| Nylon Rope | 6,754.80 | 3rd |
| Duct Tape | 503.70 | Last — shortest bar |

> Table is **sorted by Revenue descending** — always sort by your key metric for maximum readability.

### Sum of Revenue — Font Color

Revenue values are formatted in **dark green font**, making the most important column stand out from the plain black number columns.

---

## How to Apply Conditional Formatting

1. Click on your **Table or Matrix visual**
2. Go to **Visualizations pane → Format visual → Cell elements**
3. Toggle on the formatting type you want per column:

| Option | What it does |
|--------|-------------|
| **Background color** | Colors the cell background by gradient or rules |
| **Font color** | Changes text color based on value |
| **Data bars** | Adds proportional bars inside the cell |
| **Icons** | Adds icon sets (arrows, shapes, flags) based on rules |

4. Click **fx** next to each option to configure:
   - **Gradient** — smooth color scale from min to max
   - **Rules** — custom buckets (e.g. if value > 40 → red background)
   - **Field value** — color driven by a separate column

---

## Key Takeaways

- [ ] Conditional formatting is applied per-column inside a Table or Matrix
- [ ] Data bars give instant visual comparison without needing a separate chart
- [ ] Icons add a traffic-light style signal to any numeric column
- [ ] Background color rules work best for categorizing into tiers (low / mid / high)
- [ ] Font color draws attention to the most important metric column
- [ ] Always sort the table by the key metric for maximum readability

---

## Files

| File | Description |
|------|-------------|
| `conditional_formatting.pbix` | Power BI file with both formatted tables |
| `01_conditional_formatting/screenshots/conditional_formatting.png` | Screenshot of both tables |
