# FoodWaste_Analysis_Project
End-to-end data project isolating Pakistan’s food waste footprint (25.32M tonnes). Utilizes Python (Pandas) for data validation/sanity checks, and transforms insights into an interactive Power BI dashboard featuring robust DAX measures, dynamic multi-sector slices, spatial tracking, and interactive data-confidence slicers.

# Pakistan Food Waste Analytics Dashboard

An end-to-end data analytics project that processes, validates, and visualizes national food waste metrics using **Python (Pandas)** and **Power BI**. The core focus is handling raw macro data, performing programmatic sanity checks, and translating it into high-signal business intelligence.

## Core Executive Metrics (Pakistan)
*   **Total Food Tonnage:** 25.32M Tonnes/Year (Engineered via custom DAX filtering)
*   **Per Capita Waste:** 118 kg/person/year
*   **Real-World Impact:** 2.53M Garbage Trucks (Modeled assuming an average 10-tonne load capacity)

##  Project Architecture

### 1. Data Validation Pipeline (Python / Pandas)
Before visualization, a Python script isolates the raw regional dataset, strips whitespace, and programmatically cross-checks individual economic sectors against the combined summary column to ensure flawless metric reconciliation with zero data-leakage.

### 2. Interactive Business Intelligence Layer (Power BI)
*   **Context-Aware KPI Cards:** Built using optimized DAX logic with explicit filter overrides.
*   **Dynamic Sector Breakdown:** A curated donut chart highlighting the structural composition of waste: **Household (62.98%)**, **Food Service (23.65%)**, and **Retail (13.38%)**.
*   **Interactive Control Panel:** Implemented standalone, high-contrast modern **Tile Slicers** utilizing data confidence intervals (`High`, `Medium`, `Low`, `Very Low`) to instantly stress-test data reliability across all visuals.

## Core DAX Blueprint
Total Tonnage = 
CALCULATE(
    SUM('Food Waste data and research - by country'[Household estimate (tonnes/year)]) + 
    SUM('Food Waste data and research - by country'[Retail estimate (tonnes/year)]) + 
    SUM('Food Waste data and research - by country'[Food service estimate (tonnes/year)]),
    'Food Waste data and research - by country'[Country] = "Pakistan"
)

## Key Strategic Insight
* **Domestic Dominance:** Household waste represents the overwhelming majority share ($>62\%$) of food waste in Pakistan.
* **Action Plan:** From an operational perspective, municipal waste reduction campaigns and ROI-driven sustainable initiatives should heavily prioritize domestic consumer awareness frameworks over commercial retail logistics to maximize environmental impact.

```

```
