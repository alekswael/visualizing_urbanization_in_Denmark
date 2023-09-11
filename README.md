# Visualizing three decades of urbanization in Denmark

### About the project
This project examines the urbanization process in Denmark over the past three decades using spatial analysis and visualization techniques. Municipal population data and topographical features are utilized to create altered maps that depict the changes in urbanization patterns. Choropleth maps and cartograms represent population distribution and size, while a time series approach visualizes the changes over time. The findings highlight population concentration around major cities like Copenhagen, Aarhus, Odense, and Aalborg, emphasizing the dominance of Copenhagen. The visualizations provide insights into a process of ongoing, moderate
urbanization in Denmark.

**Keywords**: spatial analytics, urbanization, cartogram, choropleth, time series

### Data

The municipal population data is acquired from noegletal.dk1, which is a free database provided by the Danish Ministry of Interior and Health. It contains municipal data regarding tax, debt, social relations, institutions and structural relations. The raw population count for each municipality from 1993 to 2023 was obtained through the web interface. The data is corrected for the Municipal Reform of 2007, wherein 271 municipalities were combined into 98, so all years include data in the 98-municipality format.

### Pipeline

The data pipeline is available in the `urbanization_denmark.Rmd` file, located in the ‘src’ folder. It contains code for data import, processing, map creation, plotting and saving the visualizations. The pipeline has the following structure:

1. Load necessary R packages
2. Import spatial data from GADM
3. Import population data
4. Join the spatial data with the municipal population data
5. Project geographic coordinates to ETRS89 / UTM zone 32N
6. Create choropleth map for Danish municipalities in 2023
7. Create cartogram/choropleth maps from 1993-2023
8. Animate plot and save .GIF

When the .Rmd is run, the animated visualization is saved as ‘animation.gif’ in the ‘out’ folder, along side the choropleth/cartogram map for each year and the choropleth
map for 2023.

# Visualizations

![animation](out/animation.gif)

*Animated cartogram/choropleth map of Danish municipalities. Population per municipality in the years 1993-2023.*

![choropleth](out/choropleth_X2023.png)

*Choropleth map of Danish municipalities, colored by total population ratio, using data from year 2023.*
