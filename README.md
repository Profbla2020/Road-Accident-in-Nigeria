# Road-Accident-in-Nigeria
The dataset records the total number of road traffic accidents in each state for the given period, categorizing the accidents into fatal, severe, and minor incidents. This comprehensive dataset is valuable for analyzing trends and patterns in road safety across the country, helping to identify regions with higher accident incidences.

# Methodology
Methods of Data Collection:
Data on number of Road Traffic Accident (RTA) was obtained from the Annual Abstract of statistics published by the National Bureau of Statistics, Nigeria. The data comprises of insurgence of Road Traffic Accident within the year 2013 to 2017 for the 36 states in Nigeria including the Federal capital Territory(Abuja) as well as the water body Area (lack chad) of the country.
included in the data obtained and adopted for this study are years of the accident, the state of the occurrence of accident, total number of the accident occurred during the years of study which include the addition of the fatal, severe and minor accident that occurred across the state of the country.

# Methods of Data Analysis:
R package version 4.0.5 and R studio was used to analyze the data in order to get adequate information from the data. Descriptive statistics of the data was performed using summary(), box plot was also plotted to further understand the shape of the distribution of the data.
the data were later subjected to map using tmap() and a geospatial analysis using mainly the two major different approaches namely Global Moran I and Local Moran I in order to determine the degree of spatial clustering.

# Descriptive Statistics
Descriptive statistics are a useful means of deriving quick information about a collective dataset. we would Notice that below, i made use of $ symbol to select a single variable from the Accidentdata object.
This is because If you type in Accidentdata$ (so the name of your data object followed by a $ sign), then press tab on your keyboard, RStudio will let you select a variable from a drop down window.
Repeat this step for your for the rest of the variable.
Another useful function i adopted for descriptive statistics is summary() which will produce multiple descriptive statistics as a single output. well this function can also be run for multiple variables or an entire data object.

# Univariate plots
Univariate plots are a useful means of conveying the distribution of a particular variable. Many of these can be produced very simply in R. In this study, Histogram, Boxplot and vioplot were adopted.

# Histograms
Histograms are perhaps the most informative means of visualizing a univariate distribution. In this study i created histogram for all variables using the hist() function

# Boxplots
In addition to histograms, another type of plot that shows the core characteristics of the distribution of values within a dataset, and includes some of the summary() information generated earlier, is a box and whisker plot commonly called boxplots. This is created by the function boxplot(). In this study, I created multiple box plots in order to compare the four main variables.

# Making Maps in R
Loading shapefiles into R:
A GIS shapefile is a file format for storing the location, shape, and attributes of geographic features. In other words, it contains the geographic information which allow it to be mapped as either points, lines or polygons.
First i need to load some packages.
The packages are:
* rgdal - Bindings for the Geospatial Data Abstraction Library.
* rgeos - Interface to Geometry Engine - Open Source.
* sp

Next, we need to load the output area shapefile into R.

Shapefiles are made up of multiple different files which, when combined by certain software packages, can be mapped using a common projection system.I will be using output area boundaries as this study data is at that level. Therefore, the data will be visualized as a polygon file whereby each individual polygon represents the outline of a unique output area from the study area.

# Measuring Spatial Autocorrelation of the study
This work covers various measures of spatial autocorrelation in R. i considered both statistics of global spatial autocorrelation and how to identify spatial clustering across our study area.

In this work i will:
* Run a global Spatial autocorrelation for the shapefile of this study area.
* Identify local indicators of spatial autocorrelation.

# Running a spatial Autocorrelation
A spatial autocorrelation measures how distance influences a particular variable. In other words, it quantifies the degree of which objects are similar to nearby objects. Variables are said to have a positive spaital autocorrelation when similar values tend to be nearer together than dissimilar values.

Waldo Tober’s first law of geography is that “Everything is related to everything else, but near things are more related than distant things.” so we would expect most geographic phenomena to exert a spatial autocorrelation of some kind.
in this work i will be using the spatial autocorrelation functions available from the spdep package.

