## Project Overview

This workbook is an order analytics and operations reporting project designed to transform transaction-level order records into KPI summaries, pivot-based analysis, and visual dashboards.

It supports analysis of sales performance, customer mix, product and SKU contribution, geography, payment behavior, category performance, and delivery efficiency.

## Workbook Structure

### `Orders`
The `Orders` sheet is the primary source-data table. It contains one row per order and includes:

- Order identifiers and dates
- Customer names, types, and segments
- City and payment method
- Product and SKU details
- Product category
- Quantity and pricing fields
- Discounts, tax, delivery fees, and surge fees
- Total sales
- Delivery-time metrics

A helper weekday field is derived from the order date for time-based analysis. The main analytical source range is `Orders!A1:T1499`. (`Orders!A1:T1499`)

### `Kpi`
The `Kpi` sheet provides headline business metrics and summary calculations. It is designed to answer high-level questions such as:

- How much sales were generated?
- How many products and SKUs are represented?
- How many orders were placed?
- What is the average delivery time?
- How are sales distributed by city or region?

The sheet uses formulas linked directly to the `Orders` data and includes summary output areas for pivot-style analysis. (`Kpi!A1:B16`)

### `Charts`
The `Charts` sheet contains analytical questions, chart-supporting summary blocks, and dashboard visualizations. The analysis covers:

- Sales by weekday
- Top-performing products
- Lowest-performing SKUs
- Sales contribution by region
- Delivery time by city
- Sales by product category
- Customer counts by customer segment

The chart layer is intended to make operational trends and performance differences easier to interpret without reviewing the raw transaction table. (`Charts!A1:B28`)

### `Report`
The `Report` sheet appears to be reserved for a higher-level presentation or executive summary. It currently contains minimal visible content and can be used as the future landing page for key findings, management commentary, and selected charts. (`Report!N15`)

## Data Flow

The workbook follows a straightforward reporting pipeline:

1. Order-level records are maintained in `Orders`.
2. Formula-driven KPIs are calculated in `Kpi`.
3. Pivot-style summaries are generated from the order data.
4. Chart outputs visualize the main performance dimensions in `Charts`.
5. `Report` can serve as the final presentation layer for decision-makers.

## Intended Use

This workbook can support:

- Sales performance monitoring
- Product and SKU prioritization
- Regional comparison
- Customer-segment analysis
- Delivery-service monitoring
- Payment-method analysis
- Operational dashboarding
- Management reporting and presentation preparation

## Maintenance Guidance

When updating the workbook:

- Add new order records to the existing `Orders` structure.
- Preserve the existing column names and field meanings.
- Extend helper formulas, especially the weekday calculation, for any new rows.
- Refresh pivot-based summaries after adding or changing source data.
- Confirm that KPI formulas continue to reference the full order-data range.
- Review charts after refresh to ensure their source summaries remain current.
- Use the `Report` sheet for final conclusions rather than exposing raw transaction detail.

## Design Notes

The workbook separates detailed transactional data from summary analysis and visualization. This makes it suitable for both operational review and management-level reporting while keeping the underlying records available for deeper investigation.

The recommended next enhancement is to complete the `Report` sheet with a concise executive dashboard containing headline KPIs, selected charts, key observations, and refresh instructions.
