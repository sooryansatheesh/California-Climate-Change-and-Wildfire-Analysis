# California Climate Change and Wildfire Analysis
 Spring 2023 UC Berkeley : Analysing the last 20 years of temeprature and wildfire data from California to unearth key insights
# Welcome to the 20 years California Climate Change Analysis and Data Visualization project repository (INFO247- Spring 2023)
**Wadzanai Makomva and Soorya Narayan Satheesh**
## Project Goals
Our project aims to provide knowledge and understanding of key climate change indicators, with a focus on California. We strive to educate users about the impacts of climate change and raise awareness of its urgency. As data scientists, we are also interested in exploring visualization techniques to convey this critical information effectively.
## Our goals include:
Stirring Curiosity: We aim to pique the user's interest and encourage them to seek more information on climate change and its effects.

Raising Awareness: We believe that building awareness is crucial in addressing climate change and garnering support for necessary policies and initiatives.
## Visualization Description
Our project focuses on three categories of visualizations:

1. Temperature Changes in California
1. Precipitation Changes in California
1. Wildfires in California

We utilize color, labels, annotations, and interactivity to effectively communicate data and provide a clear understanding of climate change indicators in California.
### Temperature Changes in California
We visualize maximum and minimum temperature trends over time for different California counties, allowing users to compare temperature changes by location. Anomaly temperature heat maps highlight significant temperature shifts.
### Precipitation Changes in California
We showcase average precipitation trends over the past 20 years in six California counties. Line charts display annual averages, while precipitation heat maps illustrate variations in different regions over time.
### Wildfires in California
Our visualizations depict annual forest fires detected in California from 2000 to 2020, emphasizing the alarming increase in wildfires. We also explore the monthly variation in forest fires and the relationship between forest fires, population density, and county areas.
## Datasets and Tools
We utilized reliable and accredited data sources for our project:

**Temperature and Precipitation Dataset**: We obtained data from the National Centers for Environmental Information, cleaned and processed it using Python, and merged it to create a single dataset.

**Wildfire Dataset**: Our dataset contains information on forest fires in California from 2000 to 2022, sourced from NASA's MODIS Satellite. We processed and filtered the data to focus on forest fires.

**California Counties Demographics Dataset**: We acquired data on demographics, including population density and area, from the World Population Review website.

## Approach 
### Temperature and Precipitation Dataset 
Given the copious amount of data available relating to changes in climate indicators, we were intentional about finding data sources that were verifiable, accredited and trustworthy whilst also being easy to understand. We downloaded our data from the National Centers for Environmental Information  which provided us with simplified data on temperature and precipitation changes over time. 
(https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/county/time-series)
We downloaded csv files for each of the 58 counties separately. These files were then cleaned, processed and merged to form a single dataset using Python coding. In the raw file the year and month were fused together which prevented creation of any visualization. This was separated to form two separate fields. Additionally , a new field for county names was created.

### Wildfire Dataset
The dataset is a collection of over 283k data points containing information of Forest fires in the different National Park of California from 2000 to 2022 detected through the NASA Land, Atmosphere Near real-time Capability for EOS (LANCE) Fire Information for Resource Management System (FIRMS) using the Moderate Resolution Imaging Spectroradiometer (MODIS) on the Terra/Aqua satellites. 
Dataset source website 
Dataset was downloaded as a csv file.
Summary of dataset download-
    Download Id     : 343028
    Data Source     : MODIS C6.1
    Start Date      : 2000-11-01
    End Date        : 2023-04-10
    Output Format   : csv
    Area of Interest: -124.8,32.6,-114.4,42.1

**Transformations of the dataset**
1. The dataset includes fire locations that may be forest fire, other terrestrial fire, fire in sea and fire from volcanic activity. It is a set of x/y locations with details of map. The dataset was filtered using tools in ArcMap to include only the forest fires.
2. Using QGIS, two new fields were created in the attribute table for year and month of the forest fire.
3. The dataset was processed in ArcMap using the intersection tool with a layer of California counties to filter the fire points on the basis of California counties (Source -  https://gis.data.ca.gov/datasets/CALFIRE-Forestry::california-county-boundaries/about ). This provided every datapoint with a new field having the name of the respective California county.
4. The csv file was then processed in Python using Pandas library to convert the numeric values of months to text data. Irrelevant fields in the dataset were dropped. 

### California Counties Demographics Dataset
We used information on demographics of the different counties of California including population density, population growth, 2023 population and area from the World Population review website. 
(https://worldpopulationreview.com/states/california/counties). The data was downloaded as a CSV file. The county names were cleaned in Excel so as to match the county names in the other two datasets. 

## Tools 

For all three datasets, data was cleaned and sorted using Python/QGIS/ArcMap/Excel whilst visualization generation was conducted in Tableau. Other visualizations included in the screenshots were also created using d3 in Observable plot, however, these were not included in our final website. The webpage was made using HTML, CSS and Visual Studio Code for coding. Other illustrations were also made using Figma but were not used in the final website. Other visualizations and code lists are linked at the end of this document and all used resources are referenced at the bottom of the page. 


Thank you for exploring our Climate Change Analysis and Data Visualization project repository. We hope our visualizations inspire awareness and action regarding climate change in California and beyond.

## Acknowledgments 
●	This research benefited from the support and services of UC Berkeley's Geospatial Innovation Facility (GIF), gif.berkeley.edu.
●	We acknowledge the use of data and/or imagery from NASA's Fire Information for Resource Management System (FIRMS) (https://earthdata.nasa.gov/firms), part of NASA's Earth Observing System Data and Information System (EOSDIS).
●	We acknowledge the use of information from NOAA website for this project https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/county/time-series

