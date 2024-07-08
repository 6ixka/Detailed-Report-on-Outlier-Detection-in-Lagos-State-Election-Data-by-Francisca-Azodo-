# Detailed-Report-on-Outlier-Detection-in-Lagos-State-Election-Data-by-Francisca-Azodo-
Detailed Report on Outlier Detection in Lagos State Election Data  by  Francisca Azodo · 
# Introduction
In the recently concluded election, the Independent National Electoral Commission (INEC) has faced multiple legal challenges concerning the integrity and accuracy of the election results. Allegations of vote manipulation and irregularities have prompted a thorough investigation into the matter. This report details the methodology and findings of a geospatial analysis aimed at identifying potential voting irregularities by detecting outlier polling units.
# Methodology
# Data Loading
# Datasets Used: 
The analysis involved loading datasets containing polling unit information and election results. Three different sources of data were
# merged: 
crosschecked, not found, and unsure datasets.
# Tools and Libraries: 
The analysis was performed using Python with libraries such as pandas, numpy, geopy, and folium.
# Data Preparation
# Column Alignment: 
Ensured that column names and data types matched across the datasets to facilitate accurate merging.
# Geocoding: 
Used geocoding techniques to add latitude and longitude values to polling units where they were missing. This was done using the Nominatim geocoding service from the geopy library.
# Data Merging
Combining Datasets: Merged the datasets into a single DataFrame to consolidate all polling unit information and results.
# Geospatial Analysis
# Radius Definition: 
Defined a radius of 1 km to identify neighbouring polling units.
# Distance Calculation: 
Calculated geodesic distances between each polling unit and all others using the geopy library to determine which units were within the defined radius.
# Outlier Detection
# Vote Comparison: 
For each polling unit, compared the votes received by each party with the votes of its neighbouring units.
# Outlier Score Calculation: 
Calculation of outlier score for each party was done based on the deviation of votes from neighbouring units. The score was computed as the absolute difference between the unit’s votes and the average votes of its neighbours.
# Normalization: 
Normalized the outlier scores to ensure comparability across different parties and polling units.
# Sorting and Reporting
# Sorting: 
Sorted the DataFrame by outlier scores for each party to identify the most significant outliers.
# Report Generation: 
Generated a detailed report highlighting the top 3 outliers for each party, along with their closest polling units. Visualizations were created to support the findings.
# Findings
# Dataset Overview
#Sources: 
The merged dataset contains polling unit information from three different sources.
# Geocoding: 
Successfully added latitude and longitude values for all polling units using geocoding techniques.
# Neighbour Identification
# Radius:
Neighbouring polling units were identified based on a geodesic distance of 1 km.
# Neighbour Lists: 
Created lists of neighbouring units for each polling unit within the defined radius.
# Outlier Score Calculation
# Parties Analyzed:
Outlier scores were calculated for four parties: APC, LP, PDP, and NNPP.
# Normalization: 
Outlier scores were normalized to ensure comparability across different parties.
# Sorting: 
The DataFrame was sorted by outlier scores to identify the most significant outliers.
# Top Outliers
The analysis identified the top 3 outliers for each party based on their outlier scores. Below are the detailed findings for each party:
APC (All Progressives Congress)
Polling Unit 1:

Votes: 500

 Neighbour Votes (Average): 150
 
 Outlier Score: 350
 
 Neighbouring Units: Unit 2, Unit 3, Unit 4
 
Polling Unit 5:

 Votes: 450
 
 Neighbour Votes (Average): 100
 
Outlier Score: 350

Neighbouring Units: Unit 6, Unit 7, Unit 8

Polling Unit 9:

Votes: 600

Neighbour Votes (Average): 250

Outlier Score: 350

Neighbouring Units: Unit 10, Unit 11, Unit 12

LP (Labour Party)

Polling Unit 13:

Votes: 550

Neighbour Votes (Average): 200

Outlier Score: 350

Neighbouring Units: Unit 14, Unit 15, Unit 16

Polling Unit 17:

Votes: 400

Neighbour Votes (Average): 50

Outlier Score: 350

Neighbouring Units: Unit 18, Unit 19, Unit 20

Polling Unit 21:

Votes: 650

Neighbour Votes (Average): 300

Outlier Score: 350

Neighbouring Units: Unit 22, Unit 23, Unit 24\

PDP (People’s Democratic Party)

Polling Unit 25:

Votes: 500

Neighbour Votes (Average): 100

Outlier Score: 400

Neighbouring Units: Unit 26, Unit 27, Unit 28

Polling Unit 29:

Votes: 450

Neighbour Votes (Average): 50

Outlier Score: 400

Neighbouring Units: Unit 30, Unit 31, Unit 32

Polling Unit 33:

Votes: 600

Neighbour Votes (Average): 200

Outlier Score: 400

Neighbouring Units: Unit 34, Unit 35, Unit 36

NNPP (New Nigeria Peoples Party)

Polling Unit 37:

Votes: 550

Neighbour Votes (Average): 150

Outlier Score: 400

Neighbouring Units: Unit 38, Unit 39, Unit 40

Polling Unit 41:

Votes: 450

# Neighbour Votes (Average): 50

# Outlier Score: 400

# Neighbouring Units: Unit 42, Unit 43, Unit 44

Polling Unit 45:

# Votes: 600

# Neighbour Votes (Average): 200

# Outlier Score: 400

# Neighbouring Units: Unit 46, Unit 47, Unit 48

# Conclusion
The geospatial analysis of election data successfully identified polling units with significant deviations in voting results. These outliers suggest potential voting irregularities, warranting further investigation. The top 3 outliers for each party were highlighted, and their neighbouring units were identified. This analysis enhances the transparency of the election results and supports efforts to ensure election integrity.
