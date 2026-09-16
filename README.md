# Mobile App Market Analysis: Google Play vs. App Store

## Business Question
Which mobile app categories are oversaturated versus underserved across the Google Play Store and Apple App Store, and where is there a viable, low-competition niche for a new app?

## Dataset
- **Source:** [Apple App Store dataset](data/AppleStore.csv) and [Google Play Store dataset](data/googleplaystore.csv) (Kaggle)
- **Size:** 18,000+ combined app records across both platforms
- **Description:** Each row represents one app, with fields including category/genre, install count (or install count band), rating, price, and content type, collected as a snapshot of each store's catalog.

## Tools Used
- Python (pandas) — data cleaning, deduplication, and null handling
- Python (matplotlib) — visualization of category composition and install distributions
- Jupyter Notebook — exploratory data analysis workflow

## Key Findings
1. **The App Store is heavily gaming-dominated, Google Play is not** — Games account for 58.2% of all free iOS apps, versus just 28.6% for Games + Family combined on Android, leaving 71.4% of Android's free-app catalog spread across productivity, tools, and lifestyle categories.
   
    <img src="visuals/market_composition.png" width="750">
   
3. **A handful of mega-apps distort category-level install averages** — Communication leads Android by raw average installs (~38.5M), but removing 100M+ install outliers (e.g. WhatsApp, Gmail) drops that average to ~3.6M — a ~90.6% reduction — revealing the "true" mid-market install expectation for a new entrant.

   <img src="visuals/outlier_impact_communication.png" width="600">
   
5. **Books & Reference is a high-engagement, underserved niche** — the category averages 8.7M installs despite far less competition than Games or Communication, pointing to a viable, less saturated space for a new app.

## Recommendations
- **Target the Books & Reference niche** with a differentiated product — not a generic ebook reader, but a single-topic interactive app (e.g. built-in narration, progress quizzes, community discussion) that avoids competing head-on with Kindle or Google Play Books.
- **Differentiate platform strategy at launch:** position as a premium/utility purchase on iOS, where users are more accustomed to paying for non-gaming utility apps; use a freemium, ad-supported model on Android to maximize reach given its larger and more price-sensitive user base.

## Files
- `data/AppleStore.csv`, `data/googleplaystore.csv` — raw source datasets
- `notebooks/analysis.ipynb` — full cleaning, EDA, and visualization workflow
- `visuals/` — exported charts referenced in this README

## Methodology
Both datasets were cleaned independently before comparison: duplicate entries were removed (~1,100 across the combined data), missing values in category and install fields were resolved, and install counts — which Google Play reports as bucketed ranges (e.g. "1,000,000+") rather than exact figures — were standardized to their lower-bound numeric value to allow consistent cross-platform aggregation.

Category-level analysis used custom pandas frequency tables to compare genre distribution and average installs across both stores. To avoid a small number of extreme outliers (globally dominant apps like WhatsApp and Gmail) skewing category averages, a secondary analysis recalculated installs after excluding apps above the 100M-install threshold, which reveals a more realistic benchmark for what a new, non-mega app in that category could expect.

**Limitations:** Google Play's bucketed install counts are approximate by design, so all Android install figures in this analysis represent a lower bound rather than an exact count. The dataset is also a single-point-in-time snapshot, so it reflects category saturation and demand at time of collection rather than current market conditions — a live app would need this analysis re-run against current data before acting on it.
