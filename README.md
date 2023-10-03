# Bush-fire-score Dataset and Fire Risk Score Analysis

## Dataset Description:

We have gathered comprehensive data to analyze the bushfire risk in different neighborhoods. The datasets include:

- **Statistical Area 2 Data (SA2):** This data is in the .shp file format and was obtained from the Australian Bureau of Statistics.

- **Bush Fire Prone Land Vegetation Data:** This information was sourced from the NSW Rural Fire Service.

- **Census Data:** This dataset encompasses various neighborhood details, such as population density, number of dwellings, and business locations.

The data is organized into five files: `StatisticalAreas.csv`, `Neighbourhoods.csv`, `BusinessStats.csv`, `RFSNSW_BFPL_small.shp`, and `SA2_2016_AUST.shp`.

## Fire Risk Score Analysis:

To calculate the fire risk score, we utilized the following formula:


Certainly! Below is the information presented in a README.md format:

markdown
Copy code
# Bush-fire-score Dataset and Fire Risk Score Analysis

## Dataset Description:

We have gathered comprehensive data to analyze the bushfire risk in different neighborhoods. The datasets include:

- **Statistical Area 2 Data (SA2):** This data is in the .shp file format and was obtained from the Australian Bureau of Statistics.

- **Bush Fire Prone Land Vegetation Data:** This information was sourced from the NSW Rural Fire Service.

- **Census Data:** This dataset encompasses various neighborhood details, such as population density, number of dwellings, and business locations.

The data is organized into five files: `StatisticalAreas.csv`, `Neighbourhoods.csv`, `BusinessStats.csv`, `RFSNSW_BFPL_small.shp`, and `SA2_2016_AUST.shp`.

## Fire Risk Score Analysis:

To calculate the fire risk score, we utilized the following formula:

fire_risk = S(z(population_density) + z(dwelling_density + business_density) + z(bfpl_density) - z(assistive_service_density) + z(m_temp))


Here's a breakdown of the variables and methodology used in the analysis:

- **`S` (Logistic Function):** This function helps in mapping any real-valued number to a value between 0 and 1, making it suitable for probability calculations.

- **`z` (Z-score/Standard Score):** It standardizes a measure, making it easier to compare different variables on a similar scale.

  - **`z(population_density)`:** Population divided by neighborhood land area, standardized.
  
  - **`z(dwelling_density + business_density)`:** Total number of dwellings and businesses divided by neighborhood land area, standardized.
  
  - **`z(bfpl_density)`:** Area and category of Bush Fire Prone Land divided by neighborhood land area, standardized.
  
  - **`z(assistive_service_density)`:** (Public Administration and Safety + Health Care and Social Assistance) divided by neighborhood land area, standardized.
  
  - **`z(m_temp)`:** Mean temperature data, standardized.

This analysis provides a comprehensive understanding of the fire risk in different neighborhoods, considering population density, dwelling and business density, bush fire prone land density, availability of assistive services, and mean temperature.



