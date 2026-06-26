# 🚗 European Used Car Market Analysis (eBay Kleinanzeigen)

<img width="1014" height="730" alt="eBayUsedCarsDashboard" src="https://github.com/user-attachments/assets/eb320b01-6e68-4de9-9102-a9e3b619ab1d" />

*Click [here](https://public.tableau.com/app/profile/nathan.chapero/viz/eBay_used_car_analysis/Dashboard1?publish=yes) to view the interactive dashboard on Tableau Public.*

## Table of Contents
- [Project Overview](#project-overview)
- [Data Cleaning & Preparation](#data-cleaning--preparation)
- [Dashboard UX & Design](#dashboard-ux--design)
- [Key Business Insights](#key-business-insights)
- [Technologies Used](#technologies-used)

## Project Overview
This project analyzes a dataset of over 263,000 used car listings from the German eBay classifieds platform. The goal was to identify market trends, understand vehicle depreciation curves by manufacturer, and build a highly interactive executive dashboard to allow users to isolate specific market segments.

* **Data Source:** [Link to Kaggle Dataset]
* **Python Analysis:** [Link to your Colab/Jupyter Notebook in repo]

## Data Cleaning & Preparation (Python / Pandas)
The raw dataset required extensive cleaning to ensure accurate dashboard aggregations. Using Python in Google Colab, I performed the following:
* Standardized column names and handled missing values.
* Filtered out extreme outliers and erroneous data entries (e.g., impossible vehicle ages or €0 prices).
* Translated localized German vehicle categories (e.g., converting "Kleinbus" to Minivan/Van) for a broader audience.

## Dashboard UX & Design (Tableau)
Instead of relying on standard, rigid quick-filters, this dashboard was engineered with an advanced User Experience (UX) in mind:
* **Parameter-Driven Interactivity:** Built a custom dropdown parameter combined with boolean calculated fields to act as a master control panel.
* **Contextual Highlighting:** Selecting a brand (e.g., BMW) dynamically highlights its market volume and median price in Navy Blue while dimming competitors to grey, preserving the context of the overall market.
* **Dynamic Axis Scaling:** Configured the lower charts (Depreciation Line Chart and Vehicle Type Box Plots) to automatically rescale their axes based on the user's selection, ensuring optimal readability for both luxury and economy brands.

## Key Business Insights
1. **The Volume vs. Value Disconnect:** Volkswagen dominates the market in sheer volume (68k+ listings), but luxury brands like Audi and BMW command nearly double the median listing price (€6,000+).
2. **Depreciation Cliffs:** Economy brands like Fiat experience severe value drop-offs around year 7, whereas premium brands maintain a flatter depreciation curve over a 15-year lifespan.
3. **The Premium Van Market:** Minivans from luxury manufacturers (like BMW's Active Tourer series) command surprisingly high market medians compared to traditional sedans, pushing €20,000+.

## Technologies Used
* **Data Manipulation:** Python, Pandas, Google Colab
* **Data Visualization:** Tableau Public
* **Techniques:** Parameter Actions, Calculated Fields, Boolean Logic, Outlier Handling
