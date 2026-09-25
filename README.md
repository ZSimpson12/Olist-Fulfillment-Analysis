# Retail Order Fulfillment Analysis

Analysis of 99,000+ real e-commerce orders to identify where orders break down in the fulfillment pipeline — from approval through delivery — and to surface actionable recommendations for operations and carrier-facing teams.

## Tools Used
- **Excel / Google Sheets** — data cleaning, pivot tables, XLOOKUP joins across tables
- **Tableau** — interactive 3-view dashboard (exec summary, trend analysis, regional breakdown)
- **Dataset:** [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle)

## Key Finding
Roughly **2.3% of all orders (2,341 of 99,441)** fail at one of two distinct points in the pipeline, and both patterns are consistent across 2017–2018 rather than tied to a single event or season — pointing to systemic process gaps, not one-time issues:

- **Post-shipment confirmation gap:** 1,107 orders (1.1%) show a confirmed carrier pickup date but no delivery confirmation date — the package left the warehouse but the delivery loop was never closed.
- **Post-approval fulfillment failures:** 1,234 orders (1.2%) — 625 canceled and 609 marked unavailable — were approved (payment cleared) before failing, indicating the breakdown happens after checkout, not at the point of sale.

A regional check (by customer state) ruled out a carrier- or region-specific cause: São Paulo, the largest state by order volume (42.0% of all orders), accounted for a proportional 40.4% of problem orders — confirming the issue is platform-wide.

## Deliverables
- 📄 [Full Report (Word doc)](./Order_Fulfillment_Analysis.docx) — findings, methodology, and recommendations
- 📊 [Interactive Tableau Dashboard](#) — *add your Tableau Public link here once published*

## Recommendations
1. Audit delivery confirmation systems with carrier partners; flag orders with a carrier pickup date but no delivery confirmation 14+ days out.
2. Review post-approval fulfillment workflows (inventory checks, seller fulfillment capacity).
3. Correct a data-integrity issue found during analysis: a small number of "canceled" orders also show a completed delivery date.

## Methodology Note
This analysis was cross-checked using two independent methods (Tableau and Google Sheets pivot tables) to confirm consistency. An initial discrepancy in the regional breakdown was traced to a truncated data range in one pivot table and corrected before finalizing the figures — a reminder to always validate totals against the full dataset before drawing conclusions.
