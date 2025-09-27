# Overview
This project analyzes Airbnb property data in Bristol, UK to investigate whether listings are overpriced or underpriced compared to similar properties.
The main goal is to help Airbnb hosts adjust their pricing strategies by comparing occupancy performance and price positioning within their local market.

The project is inspired by the availability of publicly shared Airbnb datasets (Inside Airbnb).
### Objective:
### Methodology
The project began with exploratory analysis of London Airbnb data before focusing on a deeper analysis of Bristol listings to provide more localized insights.

#### 1. Data Cleaning & Preparation

- Handled duplicates in id across listings.

- Verified consistency between listings.id and calendar.listing_id.

- Verified consistency between given boroughs and coordinates.

- Converted price to numeric for analysis.

- Grouped accommodates into bands (e.g. 1–2, 3–4, 5+) for fairer comparisons.

#### 2. Occupancy Estimation

- Used estimated_occupancy_l365d (last 365 days) as a proxy for actual bookings.

- Normalized occupancy by comparing it to availability where possible.

- Flagged issues such as properties with no future availability but high past occupancy.

#### 3. Grouping for Fair Comparison

- Listings were grouped by: neighbourhood_cleansed (borough/ward), room_type, accommodates_band.

#### 4. Price vs Occupancy Benchmarking

For each group: Calculated average price and median occupancy.

Flagged properties as:

-- Overpriced: Above group average price & below median occupancy.

-- Underpriced: Below group average price & above median occupancy.

#### 5. Export Results

Listings flagged as overpriced or underpriced were exported into an Excel file for easy review.

### Key Features Analyzed

- Pricing strategy (price)

- Booking performance (estimated_occupancy_l365d)

- Host availability patterns (availability_365, availability_eoy)

- Property characteristics (property_type, room_type, accommodates)

### Insights

- Many listings with consistently high occupancy but lower-than-average prices were flagged as undervalued.

- Listings with low occupancy despite higher-than-average pricing were flagged as overvalued.

- Some properties had 0 upcoming availability, making future occupancy estimation challenging.
- 
### Key Skills & Tools:
Python | SQL | LinearRegression (machine learning tool) |Data Visualization | Problem-Solving
### Outcome:
<img width="211" height="156" alt="image" src="https://github.com/user-attachments/assets/b5daa2cf-e946-49d1-8c76-2d4907db6e4a" />
<img width="482" height="517" alt="image" src="https://github.com/user-attachments/assets/1d44b17b-c69a-41f8-b079-65f026a37cf7" />
