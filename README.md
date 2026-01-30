# Airbnb Market Analysis – Tableau Dashboard

![Dashboard Preview](tableu-dashboard.png)

## Project Overview
This project analyzes Airbnb listings to help potential guests or investors understand pricing, location, and property characteristics before choosing an area to stay in. The analysis is built in Tableau using cleaned and joined Airbnb datasets, with a focus on 2016 data only.

The final output is an interactive Tableau dashboard that answers real-world questions such as:
- Which zip codes are more expensive?
- How does price change with the number of bedrooms?
- How many listings exist for each bedroom count?
- How does revenue change over time?

## Dataset Description
The project uses Airbnb data consisting of the following tables:
- **Listings** – Property-level information (bedrooms, zipcode, price, etc.)
- **Calendar** – Availability and pricing by date
- **Reviews** – Review-related data (not used in final analysis)

## Important Notes About the Data
- In the **Calendar** table, `listing_id` is the true identifier, not `id`.
- Tableau initially attempted default joins that were incorrect and required manual correction.
- The dataset included 2017 data, but the analysis was intentionally filtered to 2016 only.

## Data Preparation & Cleaning Steps
- Uploaded raw data into Tableau.
- Reviewed table structure instead of relying on Tableau’s automatic joins.
- Corrected joins manually:
  - Joined **Listings** to **Calendar** using:  
    `Listings.id = Calendar.listing_id`
  - Ensured joins were based on IDs, not price or other fields.
  - Used **INNER JOIN** to avoid orphaned records.
- Verified join accuracy by:
  - Checking row counts.
  - Validating values across tables.
- Filtered the dataset to only include **2016** data.
- Removed the **Reviews** table since it was not required and caused unnecessary complexity.

This process ensured data accuracy and full control over how tables were combined.

## Visualizations Created

### 1. Average Price per Bedroom
- Shows how price increases as the number of bedrooms increases.
- Helps users understand cost expectations by property size.

### 2. Distinct Count of Listings by Bedroom
- Displays how many listings exist for each bedroom category.
- Reveals market supply (e.g., many 1-bedroom listings, very few 5–6 bedroom listings).

### 3. Price by Zipcode
- Bar chart comparing average prices across zip codes.
- Highlights which areas are more expensive or affordable.

### 4. Price per Zipcode (Map)
- Geographic visualization for easier spatial comparison.
- Useful for users unfamiliar with the area.

### 5. Revenue per Week (2016)
- Time-series analysis showing revenue trends throughout the year.
- Indicates seasonality and peak periods.

## Dashboard Use Case
This dashboard is designed from the perspective of:

> “If I were opening Airbnb and wanted to research an area before booking.”

It helps users:
- Compare locations.
- Understand pricing patterns.
- Choose properties based on size and budget.
- Identify high- and low-demand periods.

## Tools Used
- **Tableau** – Data visualization and dashboard creation.
- **Airbnb open dataset** – Source data.
- **Manual join logic** – To ensure correct relational structure.

## Key Insights & Conclusion
- Price increases consistently with bedroom count, but larger properties are much less common.
- Zipcode plays a major role in pricing, with clear high- and low-cost areas.
- Revenue is seasonal, peaking mid-year and stabilizing toward the end of 2016.
- Manual joins significantly improved data accuracy compared to Tableau’s defaults.

## Files
- Tableau dashboard (`.twbx`)
- Dataset files
- `README.md`

---

**Created by:** Milena Cernjanski



