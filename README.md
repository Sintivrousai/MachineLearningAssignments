This repository contains three Machine Learning assignments completed for the university course **Machine Learning**.  
Each assignment focuses on a different ML topic, including supervised learning, unsupervised learning, optimization, and model evaluation.

# Assignment 1 — Exploring AirBnB in Europe

**Objective**  
Explore InsideAirbnb data for selected European cities and produce summary statistics, density measures, activity/income estimates and interactive visualisations.

## Cities (latest 12-month period available)
Amsterdam, Athens, Barcelona, Berlin, Copenhagen, Dublin, Lisbon, London, Madrid, Paris, Rome, Venice, Vienna

---

## Tasks / Requirements

1. **AirBnB Listings**  
   - Compute the number of distinct AirBnB listings per city.  
   - Present results in a table and a plot.

2. **AirBnB Densities**  
   - Compute listings per 1,000 inhabitants for each city.  
   - Use an appropriate source to determine city populations (document source & method).  
   - Present results in a table and a plot.

3. **Activity (bookings & income per listing)**  
   - Estimate bookings per listing using `#reviews_last_12_months`, assuming:
     - half of bookings leave a review, and
     - average booking length = 3 nights.
   - For each listing: estimated_bookings = reviews_last_12_months * 2, estimated_nights = estimated_bookings * 3.  
   - Income per listing = price * estimated_bookings.  
   - Report average nights booked and average income per listing per city.

4. **Cross-check**  
   - Compute total bookings and total nights per city (sum of estimates above).  
   - Search for comparable publicly available statistics, document the data source(s) and methodology, assess quality and explain any differences with your estimates.

5. **Visualisation (interactive)**  
   - Replicate relevant visualisations from InsideAirbnb (e.g., Athens page) and make them interactive: user selects a city from a dropdown and the plots update.  
   - Recommended: Altair/Vega-Altair, Plotly, or Folium for maps.

---

## Data
- **Source:** InsideAirbnb (http://insideairbnb.com) — use the latest 12-month period extract per city.  
- **Typical files:** `listings.csv`, `reviews.csv`, `calendar.csv` (use listings & reviews for this assignment).  
- **Note:** store raw CSVs in `data/raw/` (do not commit large files to GitHub; include small sample or instructions to download).
