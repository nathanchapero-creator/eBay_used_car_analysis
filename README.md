# 🚗 European Used Car Market Analysis (eBay Kleinanzeigen)

<img width="1044" height="744" alt="eBayUsedCarsDashboard" src="https://github.com/user-attachments/assets/d223afce-50ea-4ba4-99a4-93c6965d03df" />

*Click [here](https://public.tableau.com/app/profile/nathan.chapero/viz/eBay_used_car_analysis/Dashboard1?publish=yes) to view the interactive dashboard.*

## Table of Contents
- [Project Overview](#project-overview)
- [Data Cleaning & Preparation](#data-cleaning--preparation-python--pandas)
- [Dashboard UX & Design](#dashboard-ux--design-tableau)
- [Key Business Insights](#key-business-insights)
- [Technologies Used](#technologies-used)

## Project Overview
This project analyzes a 2016 dataset of over 263,000 used car listings from the German eBay classifieds platform. The goal was to identify market trends, understand vehicle age depreciation curves, price trends, and build a highly interactive executive dashboard to allow users to isolate specific brands and market segments.

* **Data Source:** [https://www.kaggle.com/datasets/sijovm/used-cars-data-from-ebay-kleinanzeigen]
* **Python Analysis:** [https://github.com/nathanchapero-creator/eBay_used_car_analysis/blob/main/eBay_car_listings_cleaning.ipynb]

## Data Cleaning & Preparation (Python / Pandas)
The raw dataset required extensive cleaning to ensure accurate dashboard metrics. Using Python/Pandas in Google Colab, I performed the following:
* Standardized column names and handled missing values.
* Filtered out extreme outliers and listing errors (e.g., impossible vehicle ages or €0 prices).
* Translated German vehicle categories (e.g., converting "Kleinbus" to "Minivan") for a broader audience.
* Began with an original dataset of 371,528 listings, cleaned down to 327,514 listings.
* Filtered the final export to the Top 10 brands, retaining 263,260 listings (80.4% of the cleaned data) to focus the dashboard on the most relevant market trends.

## Dashboard UX & Design (Tableau)
Instead of relying on rigid quick-filters, this dashboard was engineered with an advanced User Experience (UX) in mind:
* **Parameter-Driven Interactivity:** Built a custom dropdown parameter combined with boolean calculated fields to act as a master control panel.
* **Contextual Highlighting:** Selecting a brand (e.g., BMW) dynamically highlights its listing volume and median price in navy blue while dimming competitors to grey, preserving the context of the overall market.
* **Dynamic Axis Scaling:** Configured the lower charts (Depreciation Line Chart and Vehicle Type Box Plots) to automatically rescale their axes based on the user's selection, ensuring optimal readability for both luxury and economy brands.
* **Dynamic KPIs:** Four primary statistics update instantly based on the user's brand selection:
  — Total Listing Count
  — Median Car Age
  — Median Listing Price
  — Most Common Vehicle Type

## Key Business Insights
1. **The 21-Year Depreciation Floor:** Across the top 10 manufacturers, the absolute trough of vehicle depreciation is remarkably consistent, clustering tightly between 19 and 21 years of age (with 70% of brands bottoming out exactly at year 21). At this two-decade mark, the market distinctly bifurcates: economy brands permanently level off at their lowest functional baseline value, while legacy premium brands pivot into an appreciation phase as they are preserved for the classic car market.
2. **The Volume vs. Value Disconnect:** Volkswagen dominates the market in sheer volume (68k+ listings), but luxury brands like Audi and BMW command nearly double the median listing price (€6,000+).
3. **The SUV Premium Ceiling:** While vehicle types like convertibles and minivans maintain tightly clustered market values, SUVs exhibit massive price variance (the widest Interquartile Range) across nearly all manufacturers. While older, utilitarian SUVs keep the median price anchored, the 75th percentile for SUVs stretches significantly higher than standard sedans or wagons. This highlights a massive "premium ceiling" driven by consumer demand, where buyers are willing to pay heavy premiums for higher-trim modern crossovers.
4. **Market Segmentation by Utility**: The highest-volume vehicle type for each manufacturer perfectly mirrors its target demographic and market positioning. The economy tier (Opel, Ford, Renault, Peugeot, Fiat, Seat) is driven entirely by the "Small Car" segment, highlighting their primary role as affordable urban commuters. Conversely, legacy German brands (BMW, Mercedes, VW) are anchored by "Sedans," reflecting their dominance in the executive and family commuter markets. Notably, Audi stands alone with the "Wagon" as its most common vehicle, reflecting the strong European consumer preference for its premium "Avant" touring models.

## Technologies Used
* **Data Manipulation:** Python, Pandas, Google Colab
* **Data Visualization:** Tableau Public
* **Techniques:** Parameter Actions, Calculated Fields, Boolean Logic, Outlier Handling, Interactive Filtering, Data Cleaning, Data Visualization
