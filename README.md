# Bush-fire-score

# Dataset Description

○ Statistical Area 2 data in the .shp file which was obtained from the Australian Bureau of Statistics.
○ Bush fire prone land vegetation data which was obtained from the NSW Rural Fire Service.
○ Census data for the given neighbourhoods including population density,number of dwellings and number of businesses locations.
○ The data was distributed among five datasets- StatisticalAreas.csv,Neighbourhoods.csv, BusinessStats.csv, RFSNSW_BFPL_small.shp and SA2_2016_AUST.shp. 

# Fire Risk Score Analysis(used the following forrmula to  calculate the fire risk):
fire_risk = S(z(population_density)+z(dwelling & business_density)+z(bfpl_density)−z(assistive_service_density)+z(m_temp))
S = logistic function
z = z-score/standard score of a measure
population_density = population/neighbourhood land area
dwelling_density = number of dwellings/neighbourhood land area
business_density = number of businesses/neighbourhood land area
bfpl_density = area and category of BFPL/ neighbourhood land area
assistive_service_density=(public_administration_and_safety+health_care_and_social_assistance)/neighbourhood land area
