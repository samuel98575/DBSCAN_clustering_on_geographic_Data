# DBSCAN Clustering on Geographical Logistics Data

This project presents an exploratory and technical analysis of a logistics (delivery) dataset in India, focusing on the identification of spatial patterns, cleaning of geographical anomalies, and validation of *Last-Mile* delivery strategies.

## 1. Volume and Data Quality
The delivery dataset consists of **43,739 records**, featuring a solid structure of numerical data (`float64`) and a total absence of null values (NaN). However, the "visual" integrity of the database hides critical geographical inconsistencies. 

* **Geospatial Cleaning:** Statistical analysis revealed that while India is located above $8^\circ$ N, records with latitudes of -30.90 indicated input errors. 
* **Anomaly Detection:** Approximately **3,693 records (8.4%)** were identified in oceanic areas or with coordinates near zero, which would have distorted clustering algorithms if not properly sanitized.

## 2. Market Diagnosis and Economic Hubs
The analysis demonstrates a clear dominance of economic hubs, with strategic concentration in the states of **Maharashtra and Karnataka** (over 6,000 deliveries each). This reflects the importance of Mumbai and Bengaluru as financial and technological centers. 

The logistics network is perfectly aligned with demographic density: the Top 10 cities have populations between 8 and 12 million inhabitants, and the proximity between origin and destination points confirms a **low radial distance** operation. This validates the hypothesis of predominantly intra-municipal flows and a highly capillary *Last-Mile* strategy.



## 3. Demand Dynamics and Mid-Sized Centers
A crucial insight revealed by the logarithmic scale is the non-linearity of demand. 
* **Key Finding:** We identified a cluster of mid-sized cities (between $10^5$ and $10^6$ inhabitants) with delivery volumes that rival large metropolises. 
* **Operational Impact:** Cities with similar demographic profiles present distinct volumes, indicating that local infrastructure and proximity to distribution centers impact operational success more than just population size.



## Technologies Used
* **Python:** Core processing and analysis.
* **Pandas & NumPy:** Statistical manipulation and data cleaning.
* **Matplotlib & Seaborn:** Data visualization (Logarithmic Scales and Scatter Plots).
* **DBSCAN:** Density-based clustering algorithm for identifying geographical patterns and outliers.

---
*This project is part of a study on logistics optimization and geospatial data processing.*
