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

## Key Results


<div style="text-align:center;  justify-content: center;" class="hello">
<img src="https://github.com/vasupaliwal/Bush-fire-score/blob/main/Fire_risk.png" alt="Fire Risk Score" width="50%" height="300px" >
</div>

The plot basically shows the fire risk in each neighbourhood using different colours itshows or neighbourhoods with the highest fire risk the legend next to the plot basically describes the colour code used for fire risk score from 0-1.


### Correlation Analysis

<div style="display:flex; <div style="display:flex; justify-content: center;" class="hello1">" class="hello1">
    <img src="https://github.com/vasupaliwal/Bush-fire-score/blob/main/analysis.png" alt="Image 1" style="width:45%; height:300px;">
    <img src="https://github.com/vasupaliwal/Bush-fire-score/blob/main/analysis2.png" alt="Image 2" style="width:45%; height:310px;">
</div>

As we can see from the graph, there is a positive correlation between the bushfire risk score and the median income and rent of a neighbourhood in Sydney. However, the
correlation coefficient is quite low which suggests that income and rent are weakly related to the bushfire score of a region in Sydney.The correlation coefficient between
the bushfire risk score and the median income of a household is 0.12 whereas the correlation coefficient between the bushfire risk score and the rental price of a region is
0.36.This shows that the relationship between bushfire risk score and rental price is relatively stronger than the relationship between bushfire risk score and median income
of a neighbourhood
