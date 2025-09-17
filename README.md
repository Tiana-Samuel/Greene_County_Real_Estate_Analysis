# Real Estate Market Analysis Report
### Study Area: Greene County, Georgia (Zillow Listings) 
### Analyst: Christiana Samuel

## 1. Executive Summary
This report provides a detailed look at the real estate market in Greene County, Georgia, using Zillow data to track long-term price movements and analyse current property listings. The goal was to understand price
evolution, identify high-demand areas, and find potential investment opportunities. The analysis combined two main data sources: the Zillow Home Value Index (ZHVI) for long-term trends and scraped Zillow
listings for a detailed, current view of the market.
The findings reveal a clear story: Greene County’s real estate market is not uniform. 30642 (Greensboro) is the established high-value market, with the highest average listing price ($468,000), driven by its desirable Lake Oconee location. The standout discovery is 30669 (Union Point), which is the county’s growth
champion, with home values skyrocketing by a remarkable 129% since 2015. 30678 (White Plains) also
showed strong growth (109%) and presents a unique profile with a high price per square foot, suggesting a market of newer or more renovated homes.
A key finding for investors is the market's stability. All three ZIP codes exhibited "Highly predictable growth," meaning prices have followed a steady, upward trend with low volatility, reducing investment risk. The included map visualizes these segments, colouring ZIP codes by their growth percentage and plotting current listings by price. This provides a clear geographic breakdown of where value and growth are
concentrated.
This report concludes with tailored investment recommendations, suggesting the best opportunities based on an investor's goals and risk tolerance.

## 2. Data Sources
Four main datasets formed the backbone of this study:
### 1. Zillow Home Value Index (ZHVI):
o Source: Zillow Research.
o Content: Monthly home value index (2000–2025) by ZIP code.
o Role: Used to measure long-term price growth, evaluate trends between 2015–2025, and check whether the market follows a linear or more volatile pattern.
### 2. Zillow Listings Dataset 1 (Scraper A):
o Headers: Id, Broker Name, Price, Baths, Beds, Status Type, Detail Url, Address, Area, LatLong, zpid, Scraped At.
o Role: Provided listings with latitude and longitude but had limited coverage compared to other scrapers.
 
### 3. Zillow Listings Dataset 2 (Scraper B):
o Headers: address, addressCity, addressState, detailUrl, price, statusType, statusText, brokerName.
o Role: Broader coverage but lacked geographic coordinates.
### 4. Zillow Listings Dataset 3 (Apify Extractor)
o Headers: address, bathrooms, bedrooms, cover_image, details, link, price, scraped_at, sqft, status, zpid.
o Role: Provided additional listing details such as square footage and property features.

## Data Cleaning & Preparation
All raw files were saved in a dedicated “Raw Data” folder within the project directory (Landcurator_Greene County_Georgia Project). Cleaning was conducted mainly in Excel and Power Query, with additional
support from Python where needed. The steps included:
• Removing irrelevant columns that added no analytical value.
• Renaming columns across different scrapers to maintain consistency.
• Filtering the data to keep only Greene County ZIP codes.
• Merging Datasets 2–4 into one consolidated file.
• Deduplicating listings across scrapers.
• Standardizing column formats (e.g., price as numeric, date fields as datetime).
• Removing incomplete rows where essential information was missing.
The cleaned dataset was then saved as Zillow_Real_Estate_Listings.xlsx in the “Cleaned Data” folder.
Coordinate Enrichment
One of the major gaps in the listings data was that many properties were missing geographic coordinates. To address this:
• All listings missing latitude/longitude were extracted to a separate file.
• Python scripts were used to retrieve accurate coordinates.
• Results were merged back into the master file using XLOOKUP in Excel.
The final enriched dataset was stored as Geocoding_File_Filled.xlsx, ensuring that most listing if not all, now included complete geographic and property details. This preparation process provided a foundation for both the Python-based analysis and the QGIS-based mapping that followed.
 
## 3. Pricing Trends and Market Analysis
Analysis of the Zillow Home Value Index (ZHVI) reveals powerful and consistent growth across all of Greene County, with each ZIP code more than doubling in value since 2015.
### Key Findings:
### Explosive Long-Term Growth:
Union Point (30669) is the undeniable growth leader, with a total increase of 129%. White Plains (30678) follows with a 109% increase, and Greensboro (30642) shows a strong 97% increase from a higher starting point.
### A Stable and Predictable Market:
Statistical analysis graded the price growth in all three areas as "Highly predictable." This means the market has seen steady, upward trends with low volatility, making it a less risky environment for investors.
### Current Market Snapshot:
Analysis of active listings shows the current price landscape, with average listing prices highest in Greensboro ($468k) and most affordable in Union Point ($132k).
 
## 4. Segmentation (By ZIP Codes)
The data segments the three ZIP codes into distinct market profiles:
### 30642 (Greensboro): The Premium Market
➢ The county's most active and expensive market. Strong value driven by premium lakefront properties.
➢ Investment Case: Best for investors seeking stability and proven demand. Higher entry cost, but lower risk.
### 30669 (Union Point): The Growth & Value Market
➢ It rules when it comes to percentage growth. Offers the most affordable entry point.
➢ Investment Case: Top choice for investors seeking high potential returns and affordability. Likely to benefit from continued demand spillover from Greensboro.
### 30678 (White Plains): The Niche Market
➢ Profile: A unique market with high costs per square foot but moderate overall prices, suggesting newer or renovated homes.
➢ Investment Case: Attractive for buyers wanting modern amenities at a more accessible total price than Greensboro. A balanced, strategic investment.
 
## 5. Anomalies and Undervalued Areas
A statistical analysis was performed to identify listings priced significantly outside the normal range for their area (e.g., an undervalued home in a premium neighbourhood). The results indicate a mature and efficient market. No significant statistical anomalies were found in the current listing data. This means sellers are
pricing their properties appropriately based on current conditions.

### What this means for investors: 
"Deals" based purely on a seller mispricing a property are rare. The best opportunities in Greene County come from long-term appreciation in the higher-growth segments, not from finding a single hidden gem.
 
## 6. Maps and Visual Breakdown
To provide a spatial perspective, the analysis was visualized in a map using QGIS.
Map Description:
The map provides a consolidated view of Greene County's real estate dynamics. The underlying ZIP code areas are coloured by their total percentage growth since 2015, revealing 30669 (Union Point) as the
highest-growth area. Individual property listings are overlaid and coloured by their current listing price, showing the concentration of higher-valued homes in the 30642 (Greensboro) region. This combined
visualization clearly shows that high growth does not always correlate with the highest absolute prices, highlighting Union Point's potential as an affordable growth market.
 
## 7. Investment Recommendations
Based on the full analysis, the following recommendations are made:
### For the Stability-Seeking Investor: 30642 (Greensboro)

o Best for investors seeking a lower-risk investment in a proven market with high demand, despite the higher buy-in price.
### For the Growth-Oriented Investor: 30669 (Union Point)

o The top recommendation for investors seeking the highest potential returns. Its incredible growth trajectory and low entry point offer a compelling value proposition.
### For the Strategic Niche Investor: 30678 (White Plains)
o Attractive for investors or homebuyers who want more modern amenities or newer construction at a more accessible total price point than Greensboro.
