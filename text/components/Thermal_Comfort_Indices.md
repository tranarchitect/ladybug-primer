## ![](../../images/icons/Thermal Comfort Indices.png) Thermal_Comfort_Indices

![](../../images/components/Thermal_Comfort_Indices.png)

Use this component to calculate different thermal comfort indices

#### Inputs
* ##### _comfortIndex [Required]
Choose one of the comfort indices:
* ##### _____________________ [Default]
Script variable ThermalComfortIndices
* ##### _location [Required]
Input data from Ladybug's "Import epw" "location" output, or create your own location data with Ladybug's "Construct Location" component
* ##### _dryBulbTemperature [Required]
Hourly Dry Bulb Temperature (air temperature), in Celsius
* ##### dewPointTemperature_ [Optional]
Hourly Dew Point Temperature, in Celsius
* ##### _relativeHumidity [Required]
Hourly Relative Humidity, in percent (from 0% to 110%)
* ##### windSpeed_ [Optional]
Hourly Wind Speed, in meters/second
* ##### globalHorizontalRadiation_ [Optional]
Total amount of direct and diffuse solar radiation received on a horizontal surface, in Wh/m2.
* ##### totalSkyCover_ [Optional]
Amount of sky dome in tenths covered by clouds or obscuring phenomena, in tenths of coverage (from 1 to 10). For example: 1 is 1/10 covered. 10 is total coverage (10/10).
* ##### metabolicRate_ [Optional]
Input metabolic rate in mets. If not supplied 2.32 will be used as default value
* ##### age_ [Optional]
An age of the person. This input is only important for HR (Heart Rate) index.
* ##### gender_ [Optional]
Input 0 or "male"  or  1 or "female". This input is only important for HR (Heart Rate) index.
* ##### acclimated_ [Optional]
Input True if person in subject is acclimatized, or False if it's not. This input is only important for DhRa (Dehydration risk).
* ##### _____________________ [Default]
Script variable thermalComfortIndices
* ##### HOY_ [Optional]
An hour of the year for which you would like to calculate thermal indices.  This must be a value between 1 and 8760.
* ##### analysisPeriod_ [Optional]
An optional analysis period from the Analysis Period component. 
* ##### _runIt [Required]
...

#### Outputs
* ##### readMe!
...
* ##### comfortIndexValue
Humidex (°C) - the human-perceived increase in air temperature due to Dew point temperature increase. Used by Canadian Meteorologist service.
* ##### comfortIndexCategory
Each number (from 0 to 5) represents a certain humidex thermal sensation category. With categories being the following:    
* ##### comfortableOrNot
Outputs 0 or 1. 0 indicates that a person is not comfortable, 1 that he/she is comfortable at that hour (meaning humidex is < 30°C)
* ##### percentComfortable
Percentage of time chosen for analysis period, during which humidex is < 26.6°C
* ##### percentHotExtreme
Percentage of time chosen for analysis period, during which humidex is > 54.4°C
* ##### percentColdExtreme
 


[Check Hydra Example Files for Thermal Comfort Indices](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Thermal Comfort Indices)