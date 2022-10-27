# Earthquake-project
### Dataset
Worldwide earthquake data from beginning of February 2022 to now of at least magnitude 2.5. This data was taken from the USGS earthquakes website by running the following data search query to return both json and csv data : 
https://earthquake.usgs.gov/earthquakes/map/?extent=-89.50704,-382.5&extent=89.50096,742.5&range=search&timeZone=utc&search=%7B%22name%22:%22Search%20Results%22,%22params%22:%7B%22starttime%22:%222022-2-01%2000:00:00%22,%22endtime%22:%222022-10-01%2023:59:59%22,%22minmagnitude%22:2.5,%22orderby%22:%22time%22%7D%7D

### Metadata 
<title>Web Tools - Earthquake Hazards | U.S. Geological Survey</title>
<link rel="stylesheet" media="all" href="/core/assets/vendor/jquery.ui/themes/base/core.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/assets/vendor/jquery.ui/themes/base/controlgroup.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/assets/vendor/jquery.ui/themes/base/checkboxradio.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/assets/vendor/jquery.ui/themes/base/resizable.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/assets/vendor/jquery.ui/themes/base/button.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/assets/vendor/jquery.ui/themes/base/dialog.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/ajax-progress.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/align.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/autocomplete-loading.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/fieldgroup.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/container-inline.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/clearfix.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/details.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/hidden.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/item-list.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/js.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/nowrap.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/position-container.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/progress.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/reset-appearance.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/resize.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/sticky-header.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/system-status-counter.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/system-status-report-counters.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/system-status-report-general-info.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/tabledrag.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/tablesort.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/system/css/components/tree-child.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/modules/contrib/responsive_table_filter/css/responsive-table-filter.css?rjxc41" />
<link rel="stylesheet" media="all" href="/modules/contrib/jquery_ui_tabs/jquery.ui/themes/base/tabs.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/modules/views/css/views.module.css?rjxc41" />
<link rel="stylesheet" media="all" href="/core/assets/vendor/jquery.ui/themes/base/theme.css?rjxc41" />
<link rel="stylesheet" media="all" href="/modules/contrib/addtoany/css/addtoany.css?rjxc41" />
<link rel="stylesheet" media="all" href="/modules/contrib/extlink/extlink.css?rjxc41" />
<link rel="stylesheet" media="all" href="/modules/contrib/improved_multi_select/css/improved_multi_select.css?rjxc41" />
<link rel="stylesheet" media="all" href="/modules/contrib/better_exposed_filters/css/better_exposed_filters.css?rjxc41" />
<link rel="stylesheet" media="all" href="/modules/contrib/paragraphs/css/paragraphs.unpublished.css?rjxc41" />
<link rel="stylesheet" media="all" href="//use.fontawesome.com/releases/v5.1.0/css/all.css" />
<link rel="stylesheet" media="all" href="/themes/custom/usgs_tantalum/css/styles.css?rjxc41" />

      </head>



### Topic & Rationale 
As the world changes around us we are seeing ever increasing natural cataclysmic events resulting in the further need to reflect on historical events to better allow us to predict what may happen in the future. For this project we decided to focus on recent worldwide Earthquake Data available at earthwake.usgs.gov to create an user-friendly worldwide map of Earthquakes using the following criteria from the observed columns Latitude, Longitude, Magnitude, Depth, Time & Place. We then also created other relevant visualizations utilizing the data retrieved.

### Process

The data was extracted from the above link into a CSV file utilizing a Juypter Notebook and importing Panda's Library the CSV was read in to review what columns would be relevent to the visulisations that we wanted to create. After identifying the columns of interest as being place, mag, depth, longitude,latitude & time, a cleaned data frame was created and then exported to a new output CSV.

![image](https://user-images.githubusercontent.com/108265105/197743730-020c0b46-b732-4ea2-8ab7-2d5d686d311c.png)

Utilizing pymongo and MongoDB this Data Frame was stored in a non relational DataFrame

![image](https://user-images.githubusercontent.com/108265105/197745343-97ded53b-8b94-4f3b-8a5e-1fdb05cdeb0e.png)

Interactive visualizations were then created using Leafet and Java Script files as well as using flexbox to deploy to the web.
GeoJson data taken from earthquake.usgs.gov website for all earthquakes from February to October 2022.
HTML file including leaflet CSS, leaflet javascript file, and the div element where we inserted the map.
Multiple interactive layers were added to the map to allow the user to choose from satellite, street, topographic or terrain views as well as the option to click on the relevant data point to get further information as well as the magnitude being colour coded. http://127.0.0.1:5500/index.html

![image](https://user-images.githubusercontent.com/108265105/197766096-58e2267e-362c-4c6d-9ea5-a6d13260741c.png)

### Analysis
Earthquakes over time
Total earthquakes in 2022 for each month were very similar.
This supports the idea that there is an approximately equal distribution of earthquakes in cold, hot and rainy weather.
There is some evidence of very large low-pressure changes associated with major storm events that can trigger slow earthquakes in the Earth’s crust but the numbers are very small.

![Earthquakes Over Time](https://user-images.githubusercontent.com/108265105/198258650-a5c52ff3-0720-4574-aa85-1d1de69d2c98.png)

Magnitude and Depth Relationship
The p-value is 7.36 e-93.
The r-squared is 0.02.
The model is statistically significant but the low r-squared indicates low predictability.
Most earthquakes around magnitude 4 occur at any depth below the Earth’s surface.
Earthquakes above magnitude 6 tend to occur closer to the Earth’s surface.

![Magnitude vs Depth](https://user-images.githubusercontent.com/108265105/198258680-a411c4d0-81da-4bcb-b4dc-c71dae7cdb83.png)

Webpage was then created 

![Webpage](https://user-images.githubusercontent.com/108265105/198265288-404d665d-ffba-4cec-9b9e-b235f4b0fec9.png)






