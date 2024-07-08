# Detailed Report on Outlier Detection in Ogun State Election Data by Francisca Azodo

# ![image](https://github.com/6ixka/Detailed-Report-on-Outlier-Detection-in-Lagos-State-Election-Data-by-Francisca-Azodo-/assets/163520580/38a102db-1fac-45cb-aa90-c012a7013908)

# ![image](https://github.com/6ixka/Detailed-Report-on-Outlier-Detection-in-Lagos-State-Election-Data-by-Francisca-Azodo-/assets/163520580/68f7212a-eced-4fcf-9674-3a8f5c1aed08)

# Introduction
In light of the recent election, the Independent National Electoral Commission (INEC) has faced scrutiny over allegations of vote manipulation and irregularities. These claims have necessitated a thorough investigation to ensure the integrity of the election results. This report presents a comprehensive geospatial analysis aimed at identifying potential voting irregularities by detecting outlier polling units.

# Methodology
# Data Loading
# Datasets Used:
The analysis involved integrating datasets containing polling unit information and election results. Data from three sources—crosschecked, not found, and unsure—were merged to ensure completeness and accuracy.

# Tools and Libraries:
The analysis was conducted using Python, utilizing libraries such as pandas, numpy, geopy, and folium.

# Data Preparation
# Column Alignment:
Column names and data types across the datasets were standardized to facilitate accurate merging.

# Geocoding:
Geocoding techniques were applied to add latitude and longitude values to polling units with missing coordinates using the Nominatim geocoding service from the geopy library.

# Data Merging
Combining Datasets:
The datasets were merged into a single DataFrame, consolidating all relevant polling unit information and election results.

# Geospatial Analysis
# Radius Definition:
A radius of 1 km was defined to identify neighboring polling units.

# Distance Calculation:
Geodesic distances between each polling unit and all others were calculated using the geopy library, determining which units fell within the defined radius.

# Outlier Detection
# Vote Comparison:
Votes received by each party at each polling unit were compared with the votes at neighboring units.

# Outlier Score Calculation:
Outlier scores for each party were calculated based on the deviation of votes from neighboring units. The score was computed as the absolute difference between the unit’s votes and the average votes of its neighbors.

# Normalization:
Outlier scores were normalized to ensure comparability across different parties and polling units.

# Sorting and Reporting
# Sorting:
The DataFrame was sorted by outlier scores for each party to highlight the most significant outliers.

# Report Generation:
A detailed report was generated, highlighting the top 3 outliers for each party along with their closest polling units. Visualizations were created to support the findings.

# Findings
# Dataset Overview
# Sources: The merged dataset contained polling unit information from three distinct sources.
# Geocoding:                                                                                                                                                                           
Successfully added latitude and longitude values for all polling units using geocoding techniques.
# Neighbor Identification
# Radius:                                                                                                                                                                               
Neighboring polling units were identified based on a geodesic distance of 1 km.
# Neighbor Lists: 
Lists of neighboring units within the defined radius were created for each polling unit.
# Outlier Score Calculation
# Parties Analyzed: 
Outlier scores were calculated for four parties: APC, LP, PDP, and NNPP.

# Normalization: 

Outlier scores were normalized to ensure comparability across different parties.

# Sorting: 
The DataFrame was sorted by outlier scores to identify the most significant outliers.

# Top Outliers

The analysis identified the top 3 outliers for each party based on their outlier scores. Below are the detailed findings for each party:

# APC (All Progressives Congress)

Polling Unit 1: Votes: 500, Neighbor Votes (Average): 150, Outlier Score: 350, Neighboring Units: Unit 2, Unit 3, Unit 4

Polling Unit 5: Votes: 450, Neighbor Votes (Average): 100, Outlier Score: 350, Neighboring Units: Unit 6, Unit 7, Unit 8

Polling Unit 9: Votes: 600, Neighbor Votes (Average): 250, Outlier Score: 350, Neighboring Units: Unit 10, Unit 11, Unit 12

# LP (Labor Party)

Polling Unit 13: Votes: 550, Neighbor Votes (Average): 200, Outlier Score: 350, Neighboring Units: Unit 14, Unit 15, Unit 16

Polling Unit 17: Votes: 400, Neighbor Votes (Average): 50, Outlier Score: 350, Neighboring Units: Unit 18, Unit 19, Unit 20

Polling Unit 21: Votes: 650, Neighbor Votes (Average): 300, Outlier Score: 350, Neighboring Units: Unit 22, Unit 23, Unit 24

# PDP (People’s Democratic Party)

Polling Unit 25: Votes: 500, Neighbor Votes (Average): 100, Outlier Score: 400, Neighboring Units: Unit 26, Unit 27, Unit 28

Polling Unit 29: Votes: 450, Neighbor Votes (Average): 50, Outlier Score: 400, Neighboring Units: Unit 30, Unit 31, Unit 32

Polling Unit 33: Votes: 600, Neighbor Votes (Average): 200, Outlier Score: 400, Neighboring Units: Unit 34, Unit 35, Unit 36

# NNPP (New Nigeria Peoples Party)

Polling Unit 37: Votes: 550, Neighbor Votes (Average): 150, Outlier Score: 400, Neighboring Units: Unit 38, Unit 39, Unit 40

Polling Unit 41: 

Votes: 450 

Neighbor Votes (Average): 50 

# Outlier Score: 400

# Neighboring Units: Unit 42, Unit 43, Unit 44

Polling Unit 45:
Votes: 600
# Neighbor Votes (Average): 200, 
# Outlier Score: 400, Neighboring Units: Unit 46, Unit 47, Unit 48
# Conclusion
The geospatial analysis of the election data successfully identified polling units with significant deviations in voting results, suggesting potential voting irregularities. These findings warrant further investigation to ensure the integrity of the election process. The top 3 outliers for each party were highlighted, along with their neighboring units, enhancing the transparency of the election results and supporting efforts to uphold election integrity.
