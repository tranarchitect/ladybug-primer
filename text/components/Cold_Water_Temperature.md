## ![](../../images/icons/Cold_Water_Temperature.png) Cold Water Temperature

![](../../images/components/Cold_Water_Temperature.png)

Use this component to calculate the cold (inlet, mains) water temperature, if water pipes are burried undeground.

#### Inputs
* ##### method [Optional]
A method by which the cold water temperature will be calculated:
* ##### dryBulbTemperature [Required]
Hourly Dry Bulb Temperature (air temperature).
* ##### minimalTemperature [Optional]
The minimum cold temperature value.
* ##### soilThermalDiffusivity [Optional]
The ability of a soil to conduct thermal energy relative to its ability to store thermal energy.
* ##### pipesDepth [Optional]
The soil depth at which cold water pipes are burried at.

#### Outputs
* ##### readMe!
...
* ##### coldWaterTemperaturePerHour
Cold water temperature for picked pipesDepth_ and soilThermalDiffusivity_, for each hour during a year.
* ##### avrJanuaryColdWaterTemperature
Average January cold water temperature for picked pipesDepth_ and soilThermalDiffusivity_.
* ##### avrColdWaterTemperaturePerYear
Average annual cold water temperature for picked pipesDepth_ and soilThermalDiffusivity_.


[Check Hydra Example Files for Cold Water Temperature](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Cold Water Temperature)