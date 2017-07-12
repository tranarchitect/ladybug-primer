## ![](../../images/icons/WetBulbTemp.png) WetBulbTemp

![](../../images/components/WetBulbTemp.png)

Use this component to calculate Wet Bulb Temperature and Dew Point Temperature

#### Inputs
* ##### dryBulbTemperature [Required]
The dry bulb temperature [°C] from Import epw component and Ladybug_Average Data or generic lists of numbers.
* ##### relativeHumidity [Required]
The relative humidity [%] from Import epw component and Ladybug_Average Data or generic lists of numbers.
* ##### barometricPressure [Default]
The barometric pressure [Pa] from Import epw component and Ladybug_Average Data or generic lists of numbers. If no value is connected here, the default pressure will be 101325 Pa, which is air pressure at sea level.

#### Outputs
* ##### readMe!
...
* ##### wetBulbTemp
The lowest temperature that can be reached by evaporating water into the air.
* ##### dewPointTemp
The temperature at which the water vapor contained in a volume of air at a given atmospheric pressure reaches saturation and condenses to form dew.


[Check Hydra Example Files for WetBulbTemp](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_WetBulbTemp)