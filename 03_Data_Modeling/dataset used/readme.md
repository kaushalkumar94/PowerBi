# 03 — Data Modeling

## What is Data Modeling?

Data modeling in Power BI is the process of defining **relationships between tables** so that visuals can pull data from multiple tables correctly.

A good model is the backbone of any Power BI report — bad relationships = wrong numbers.

---

## The Apocalypse Dataset

Three tables were loaded for this module:

| Table | Type | Description |
|-------|------|-------------|
| `Apocolypse Sales` | Fact Table | Transactional data — one row per order |
| `Customer Information` | Dimension Table | Customer details (name, address, city, state) |
| `Apocolypse Store` | Dimension Table | Product details (name, price, production cost) |

---

## Relationships Built

### Model View

![Data Model](./screenshots/data_model.png)

### Relationship 1 — Sales ↔ Customers

| Setting | Value |
|---------|-------|
| From | `Apocolypse Sales[Customer]` |
| To | `Customer Information[Customer]` |
| Cardinality | Many-to-One (\* → 1) |
| Cross-filter | Single |

### Relationship 2 — Sales ↔ Store

| Setting | Value |
|---------|-------|
| From | `Apocolypse Sales[Product ID]` |
| To | `Apocolypse Store[Product ID]` |
| Cardinality | Many-to-One (\* → 1) |
| Cross-filter | Single |

---

## Schema Pattern

```
Customer Information          Apocolypse Store
  (Dimension)                   (Dimension)
       |  1                           1  |
       |                               |
       * ——————— Apocolypse Sales ——————*
                  (Fact Table)
```

This is a **Star Schema** — the industry standard for BI modeling.

- The **Fact table** sits in the center and holds measurable events (sales, orders)
- **Dimension tables** surround it and provide descriptive context (who, what, where)

---

## Key Concepts

**Cardinality** — describes how many rows on each side of a relationship match:
- `1` side = unique values (e.g. one Customer ID per customer)
- `*` side = repeated values (e.g. same customer appears in many sales rows)

**Cross-filter direction** — controls which way filters flow:
- `Single` = filters flow from the `1` side to the `*` side (standard)
- `Both` = filters flow both ways (use carefully, can cause ambiguity)

**Active vs Inactive relationships** — Power BI only allows one active relationship between two tables; extras are inactive and must be activated via DAX using `USERELATIONSHIP()`

---

## Visualizations Built

Using this model, the following visuals were created:

- **Total Revenue by Product** — Bar chart using `Price` and `Product Name` from `Apocolypse Store`
- More visuals in `relationships.pbix`

![Dashboard](./screenshots/visualizations.png)

---

## Key Takeaways

- [ ] Always model before building visuals
- [ ] Star schema = fact table in center, dimensions around it
- [ ] Relationships are built on matching key columns (Customer ID, Product ID)
- [ ] Cardinality is almost always Many-to-One from fact → dimension
- [ ] Use Model View to inspect and manage all relationships

---

## Files

| File | Description |
|------|-------------|
| `relationships.pbix` | Power BI file with full model and visuals |
| `screenshots/data_model.png` | Screenshot of the Model View |
| `screenshots/visualizations.png` | Screenshot of the report page |
