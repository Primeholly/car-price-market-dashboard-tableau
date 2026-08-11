# Car Price Dynamics and Market Performance Dashboard
### A Tableau Data Visualization Project

**Author:** Olaoluwa Isaac
**Tool:** Tableau Desktop / Tableau Public
**Category:** Data Visualization · Exploratory Data Analysis · Business Intelligence

---

## 1. Project Overview

This project is an interactive Tableau dashboard that analyzes the automotive resale market, exploring how factors such as **brand, model, fuel type, transmission, vehicle condition, and age** influence car pricing over time. The dashboard consolidates multiple analytical views — KPI summaries, trend lines, category comparisons, and part-to-whole breakdowns — into a single, decision-ready interface aimed at helping stakeholders (dealerships, resellers, or market analysts) quickly understand pricing dynamics across the used and new car market.

The dashboard is titled **"Car Price Dynamic and Market Performance Dashboard"** and is built with a cohesive orange/rust color palette on a white background, optimized for a 1000px desktop viewport with a phone layout also configured for mobile responsiveness.

---

## 2. Objectives

The dashboard was designed to answer the following business questions:

1. What is the overall profile of vehicles in the dataset (average age, price, engine size, depreciation)?
2. Which car models command the highest average prices?
3. How does fuel type (Petrol, Diesel, Electric, Hybrid) affect price?
4. How has average car price evolved over time (2000–2025)?
5. How does transmission type (Manual vs. Automatic) impact price?
6. How does vehicle condition (New, Like New, Used) affect price positioning?
7. Which brands hold the highest average resale/market value?

---

## 3. Dashboard Structure

The workbook contains multiple supporting sheets consolidated into one main dashboard view:

| Sheet | Purpose |
|---|---|
| Average Price by Brand | Heat-map style tile grid comparing brand-level average price |
| Price Trend by Year | Time series line chart of average price, 2000–2025 |
| Top Performing Model | Horizontal bar chart ranking models by average price |
| Fuel Type by Price | Packed bubble chart comparing fuel types |
| Condition by Price | Pie/donut chart comparing New, Like New, and Used pricing |
| Transmission by Price | Bar chart comparing Manual vs. Automatic pricing |
| Analysis Board | Supporting sheet for deeper drill-down |
| Dashboard 1 / Sheet 7 | Final assembled dashboard and staging sheet |

### KPI Header Row
At the top of the dashboard, four key metrics summarize the dataset at a glance:
- **Average Car Age:** 14 years
- **Average Car Price:** $52,507
- **Average Engine Size:** 3 (liters)
- **Mileage Depreciation:** 4 (index/rate metric)

A **Transmission filter** (Automatic / Manual toggle) sits alongside the KPIs, allowing users to dynamically filter the entire dashboard by transmission type.

---

## 4. Key Visualizations & Design Choices

### 4.1 Top Performing Model by Price (Horizontal Bar Chart)
Ranks vehicle models by average price, from highest to lowest (Corolla, 3 Series, 5 Series, C-Class, A4, A3, Fiesta). A horizontal bar layout was chosen over a vertical one to comfortably display model names as labels without truncation, and a single-hue orange gradient reinforces relative magnitude.

### 4.2 Fuel Type Impact on Price (Packed Bubble Chart)
Diesel, Petrol, Hybrid, and Electric are shown as proportionally sized, color-coded circles (Diesel: $32.2M, Petrol: $29.0M, Hybrid: $28.8M, Electric: $28.1M). The bubble format was selected for high visual impact and quick magnitude comparison across only four categories — a case where a bar chart would work equally well, but bubbles add visual variety to the dashboard.

### 4.3 Price Trend by Year (Line Chart)
A continuous line chart spanning 2000–2025 tracks average price fluctuation year over year, with data labels on selected points (e.g., $5.08M → $4.51M → $4.17M → $4.60M → $3.91M → $4.85M → $5.23M → $5.55M). This view surfaces cyclical/volatile pricing behavior rather than a simple linear trend, useful for spotting market shocks or demand cycles.

### 4.4 Average Price by Brand (Heat Tile Grid)
A treemap/tile-style grid ranks seven brands (Toyota, Mercedes, Tesla, Ford, BMW, Audi, Honda) with both **label + color intensity** encoding price, allowing two dimensions (categorical + quantitative) to be read simultaneously.

### 4.5 Transmission by Price (Bar Chart)
A simple two-bar comparison (Manual: $62.42M, Automatic: $55.72M) tied directly to the dashboard's global transmission filter, reinforcing the KPI-to-chart interactivity pattern.

### 4.6 Condition-Based Price Performance (Donut/Pie Chart)
Splits average price by condition — Used ($40.46M), Like New ($39.54M), New ($38.14M) — using a three-slice donut chart to show part-to-whole distribution at a glance.

---

## 5. Technical Implementation

**Tools & Environment:**
- Tableau Desktop (Public Edition)
- Data Source: structured car listings dataset (make, model, year, price, fuel type, transmission, condition, mileage, engine size)

**Techniques applied:**
- **Calculated Fields** for derived KPIs (average price, mileage depreciation index)
- **Dashboard Actions / Filters** — the global Transmission toggle filters across all linked worksheets
- **Color Encoding** — a consistent orange/brown sequential palette used across all charts for visual cohesion and brand consistency
- **Mixed Chart Types** — bar, line, packed bubble, donut, and heat-tile visualizations combined into a single interface to match each variable's data story
- **Responsive Layout** — separate Default (desktop) and Phone dashboard layouts configured via Tableau's Device Preview
- **Dashboard Containers** — horizontal and vertical containers used to organize KPI cards and chart panels into a clean grid

---

## 6. Key Insights

- **Diesel vehicles command the highest average fuel-type price** ($32.2M), ahead of Petrol, Hybrid, and Electric — suggesting diesel vehicles in this dataset skew toward larger/premium vehicle classes.
- **Manual transmission vehicles average higher prices than Automatic** ($62.42M vs. $55.72M) in this dataset, which may reflect performance/enthusiast vehicle segments rather than general market preference.
- **Toyota leads brand-level average price** ($17.97M), narrowly ahead of Mercedes and BMW, with Honda and Ford at the lower end of the brand comparison.
- **Compact/sedan models (Corolla, 3 Series, 5 Series) top the model price ranking**, indicating strong pricing performance for these nameplates within the dataset.
- **Price trends show volatility rather than steady growth** across 2000–2025, with peaks and troughs suggesting sensitivity to broader market or economic cycles.
- **Condition has a relatively narrow price spread** ($38.14M–$40.46M) between New, Like New, and Used, implying depreciation is more gradual than dramatic in this dataset.

---

## 7. Challenges & Solutions

| Challenge | Solution |
|---|---|
| Displaying many chart types cohesively without visual clutter | Standardized on a single orange/rust color family and consistent typography across all sheets |
| Long model/brand names crowding chart labels | Used horizontal bar orientation and tile-grid layout to preserve label readability |
| Making the dashboard interactive without overwhelming the user | Limited global filtering to a single, prominent Transmission toggle rather than exposing every possible filter |
| Ensuring usability across devices | Built a dedicated Phone layout alongside the Default desktop layout using Tableau's Device Designer |

---

## 8. Skills Demonstrated

- Dashboard design and visual hierarchy
- Data storytelling through chart-type selection
- Calculated fields and KPI design
- Interactive filtering and dashboard actions
- Color theory and branding consistency in BI reporting
- Responsive dashboard design (desktop + mobile)

---

## 9. Future Improvements

- Add brand/model-level drill-down actions from the summary tiles into detailed sub-views
- Incorporate mileage vs. price scatter analysis to strengthen the "Mileage Depreciation" KPI
- Add a year-range parameter to make the Price Trend chart more explorable
- Publish to Tableau Public with an embedded link for live interactivity in the portfolio

---

## 10. Links

- **Live Dashboard:** *[Add Tableau Public link here]*
- **Dataset Source:** *[Add dataset source/citation here]*

---

*This report documents the design rationale, technical approach, and analytical findings behind the Car Price Dynamics and Market Performance Dashboard, built as part of a data analytics portfolio.*
