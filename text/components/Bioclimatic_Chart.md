## ![](../../images/icons/Bioclimatic Chart.png) Bioclimatic_Chart

![](../../images/components/Bioclimatic_Chart.png)

This is the Bioclimactic Chart. It is based in the originally proposed chart by V. Olgyay and then in the chart presented in the book "Sun, Climate and Architecture" by Brown.

#### Inputs
* ##### _dryBulbTemperature [Required]
A number representing the dry bulb temperature of the air in degrees Celcius. This input can also accept a list of temperatures representing conditions at different times or the direct output of dryBulbTemperature from the Import EPW component.  Indoor temperatures from Honeybee energy simulations are also possible inputs.
* ##### _relativeHumidity [Required]
A number between 0 and 100 representing the relative humidity of the air in percentage. This input can also accept a list of relative humidity values representing conditions at different times or the direct output of relativeHumidity from of the Import EPW component.
* ##### ------------------------------ []
...
* ##### metabolicRate_ [Optional]
A number representing the metabolic rate of the human subject in met. This input can also accept text inputs for different activities. Acceptable text inputs include Sleeping, Reclining, Sitting, Typing, Standing, Driving, Cooking, House Cleaning, Walking, Walking 2mph, Walking 3mph, Walking 4mph, Running 9mph, Lifting 10lbs, Lifting 100lbs, Shoveling, Dancing, and Basketball.  If no value is input here, the component will assume a metabolic rate of 1 met, which is the metabolic rate of a seated human being.
* ##### clothingLevel_ [Optional]
A number representing the clothing level of the human subject in clo. If no value is input here, the component will assume a clothing level of 1 clo, which is roughly the insulation provided by a 3-piece suit. A person dressed in shorts and a T-shirt has a clothing level of roughly 0.5 clo and a person in a thick winter jacket can have a clothing level as high as 2 to 4 clo.
* ##### passiveStrategy_ [Optional]
An optional text input of passive strategies to be laid over the Bioclimatic chart as polygons.  Text inputs include "Passive Solar Heating", "Evaporative Cooling", "Thermal Mass + Night Vent" and "Natural Ventilation". NOT WORKING RIGHT NOW!!
* ##### ------------------------------ []
...
* ##### cullMesh_ [Optional]
Set to "True" to cull the colored mesh to where they have climatic data on them. See chartMesh output. Deafult "False"
* ##### calculateCharts_ [Optional]
Set to "True" to calculate and show a column type graph showing the percentage of time each strategy is capable of providing comfort conditions. See resultsChart output. Deafult "False"
* ##### ------------------------------ []
Script variable BioclimacticChart
* ##### analysisPeriodWinter_ [Optional]
An optional analysis period from the Analysis Period component. If no Analysis period is given and epw data from the ImportEPW component has been connected, the analysis will be run for the enitre year. ONLY WORKS FOR THE WHOLE YEAR RIGHT NOW!!
* ##### analysisPeriodSummer_ [Optional]
An optional analysis period from the Analysis Period component. If no Analysis period is given and epw data from the ImportEPW component has been connected, the analysis will be run for the enitre year. ONLY WORKS FOR THE WHOLE YEAR RIGHT NOW!!
* ##### basePoint_ [Optional]
An optional base point that will be used to place the Bioclimatic Chart in the Rhino scene. If no base point is provided, the base point will be the Rhino model origin.
* ##### scale_ [Optional]
An optional number to change the scale of the Bioclimatic chart in the Rhino scene. By default, this value is set to 1.
* ##### legendPar_ [Optional]
Optional legend parameters from the Ladybug Legend Parameters component.
* ##### _runIt [Required]
Set to "True" to run the component and calculate the adaptive comfort metrics.

#### Outputs
* ##### readMe!
...
* ##### ------------------------------
...
* ##### comfortResults
The number of hours and percent of the input data that are inside all comfort and passive strategy polygons.
* ##### totalComfortOrNot
A list of 0's and 1's indicating, for each hour of the input data, if the hour is inside a comfort and/or strategy polygon (1) or not(0).
* ##### strategyOrNot
A list of 0's and 1's indicating, for each hour of the input temperature and humidity ratio, if the hour is inside (1) or not(0), for each passive strategy and comfort polygons.  If there are multiple comfort polyogns or passive strategies connected to the passiveStrategy_ input, this output will be a grafted list for each polygon.
* ##### ------------------------------
...
* ##### chartGridAndTxt
The grid and text labels of the Bioclimatic chart.
* ##### chartMesh
A colored mesh showing the number of input hours happen in each part of the Bioclimatic chart.
* ##### legendChartMesh
Script variable BioclimacticChart
* ##### chartHourPoints
Points representing each of the hours of input temperature and humidity ratio.  By default, this ouput is hidden and, to see it, you should connect it to a Grasshopper preview component.
* ##### hourPointColorsByComfort
Color the chartHourPoints above according to Comfort results. They can be hooked up to the "Swatch" input of a Grasshopper Preview component that has the hour points above connected as geometry.  By default, points are colored red if they lie inside comfort or strategy polygons and are colored blue if they do not meet such comfort criteria.
* ##### hourPointColorsByMonth
Colors that the chartHourPoints above according to each month. They can be hooked up to the "Swatch" input of a Grasshopper Preview component that has the hour points above connected as geometry.  By default, points are colored red if they lie inside comfort or strategy polygons and are colored blue if they do not meet such comfort criteria.
* ##### min_maxPoints
Plot each month's Minimal/Maximal values for Temperature and Relative Humidity. By default, this ouput is hidden and, to see it, you should connect it to a Grasshopper preview component.
* ##### comfort_strategyPolygons
A tree of polygons representing the comfort and passive strategies areas of the chart made comfortable.
* ##### legendComfortStrategies
A colored legend showing the number of hours that correspond to each color for the chartMesh output.
* ##### legendBasePt
The legend base point, which can be used to move the legend in relation to the chart with the grasshopper "move" component.
* ##### ------------------------------
Script variable AdaptiveComfortCalculator
* ##### resultsChart
A column type graph showing the percentage of time each strategy is capable of providing comfort conditions. These results are summarizing the whole year and each month. Each column shows three areas: 


[Check Hydra Example Files for Bioclimatic Chart](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Bioclimatic Chart)