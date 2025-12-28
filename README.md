# The Spatial Economy of Short-Term Rentals in Austin, Texas
> **Urban Data Science & Geodemographic Clustering | University of Liverpool**

## 🏙️ Project Overview
This computational essay investigates the spatial distribution of Airbnb listings in Austin, Texas. Beyond simple mapping, the project explores the relationship between tech-driven gentrification ("Silicon Hills"), historical economic segregation, and the clustering of "lifestyle" amenities.

### **Key Discovery:**
The analysis identifies distinct "lifestyle zones." While wealthy suburban areas ("Quiet Wealth") successfully insulate themselves from the tourist economy, central hubs experience significant "Airbnb pressure," creating a conflict between essential civic functions (like health services) and short-term rentals.

---

## 🛠️ Tech Stack
* **Spatial Analysis:** `Geopandas`, `Shapely`, `PySAL`
* **Machine Learning:** `Scikit-learn` (K-Means Clustering)
* **Visualisation:** `Matplotlib`, `Seaborn`
* **Projections:** Reprojected data to **EPSG:2277 (NAD83 / Texas Central)** for sub-meter distance accuracy.



## 🧪 Methodology & Innovation
* **Geodemographic Clustering:** Implemented a **K-Means algorithm** to segment Austin into four distinct neighborhood typologies based on income, education, and amenity density.
* **Spatial Join & Aggregation:** Linked Airbnb point data with census-tract polygons to calculate rental density per square mile.
* **Tech-Driven Gentrification Analysis:** Correlated listing clusters with the "Silicon Hills" tech corridor to visualize the impact of high-income professionals on the local housing market.
* **Coordinate Precision:** Utilized a localized Texas Central projection to ensure that the Euclidean distances used in the K-Means clustering were mathematically accurate and not distorted by global spherical projections.

## 📊 Cluster Insights
* **Cluster 0 (Silicon Hills):** "Quiet Wealth." High income ($130k+) but low Airbnb density, suggesting successful residential insulation.
* **Cluster 1 (Wider Centre):** "The Civic Hub." Contains the highest density of health services but faces significant "Airbnb pressure" (143 listings per sq mile), highlighting a conflict between essential city functions and short-term rentals.
* **Cluster 2 (The Disconnected East):** Historically underserved areas with low amenity density and negligible Airbnb investment.
* **Cluster 3 (The Entertainment Core):** High luxury consumption and massive Airbnb density (266 per sq mile), indicating a transition from residential to "tourism zones."

## ⚙️ Reflection & Professional Standards
* **Data Ethics:** The project specifically filters for inactive listings and price outliers to ensure the analysis reflects the actual "active" rental market.
* **Future Work:** This model could be extended into a "Gentrification Early-Warning System" by tracking the shift of neighborhoods from Cluster 2 (underserved) toward Cluster 3 (tourist-heavy).
