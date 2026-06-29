# 🚗 European Used Car Market Analysis (eBay Kleinanzeigen)

<img width="1044" height="744" alt="eBayUsedCarsDashboard" src="https://github.com/user-attachments/assets/d223afce-50ea-4ba4-99a4-93c6965d03df" />

*Click [here](https://public.tableau.com/app/profile/nathan.chapero/viz/eBay_used_car_analysis/Dashboard1?publish=yes) to view the interactive dashboard.*

## Table of Contents
- [Project Overview](#project-overview)
- [Data Cleaning & Preparation](#data-cleaning--preparation-python--pandas)
- [Dashboard UX & Design](#dashboard-ux--design-tableau)
- [Key Business Insights](#key-business-insights)
- [Technologies Used](#technologies-and-techniques)

## Project Overview
This project analyzes a 2016 dataset of over 263,000 used car listings from the German eBay classifieds platform. The goal was to analyze pricing behavior, depreciation patterns, manufacturer segmentation, and develop an interactive dashboard for exploring the German used car market.

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
Instead of relying on rigid quick-filters, this dashboard was designed to improve usability and exploratory analysis through parameter-driven interactions:
* **Parameter-Driven Interactivity:** Built a custom dropdown parameter combined with boolean calculated fields to act as a master control panel.
* **Contextual Highlighting:** Selecting a brand (e.g., BMW) dynamically highlights its listing volume and median price in navy blue while dimming competitors to grey, preserving the context of the overall market.
* **Dynamic Axis Scaling:** Configured the lower charts (Depreciation Line Chart and Vehicle Type Box Plots) to automatically rescale their axes based on the user's selection, ensuring optimal readability for both luxury and economy brands.
* **Dynamic KPIs:** Four primary statistics update instantly based on the user's brand selection:
  * Total Listing Count
  * Median Car Age
  * Median Listing Price
  * Most Common Vehicle Type

## Key Business Insights
1. **The 21-Year Depreciation Floor:** Vehicle depreciation reaches a remarkably consistent low point between 19 and 21 years of age, with 70% of the top 10 manufacturers bottoming out at year 21. Beyond this point, economy brands generally stabilize at their lowest values, while several premium brands begin appreciating, consistent with vehicles entering the classic car market.

2. **The Volume vs. Value Disconnect:** Volkswagen dominates the marketplace with over 68,000 listings, yet Audi and BMW maintain median listing prices exceeding €6,000—nearly double many mass-market competitors. This highlights how listing volume and vehicle value reflect different market segments.

3. **The SUV Premium Ceiling:** SUVs exhibit the widest price dispersion across nearly all manufacturers. While older utility-focused models keep median prices relatively moderate, the upper quartile extends far beyond comparable sedans and wagons, suggesting buyers place a premium on newer, higher-trim SUVs.

4. **Market Segmentation by Utility:** The most common vehicle type for each manufacturer closely aligns with its market positioning. Economy brands are dominated by small cars, German luxury brands by sedans, while Audi stands out with wagons as its largest segment, consistent with the popularity of its Avant lineup in Europe.

## Technologies & Techniques
* **Programming:** Python, Pandas, Google Colab
* **Visualization:** Tableau Public
* **Techniques:** Data Cleaning, Outlier Handling, Calculated Fields, Parameter Actions, Boolean Logic, Interactive Dashboard Design
