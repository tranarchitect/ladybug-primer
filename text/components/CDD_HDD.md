## ![](../../images/icons/CDD_HDD.png) CDD_HDD

![](../../images/components/CDD_HDD.png)

Calculates heating and cooling degree-days.

#### Inputs
* ##### _hourlyDryBulbTemperature [Required]
Annual dry bulb temperature from the Import epw component (in degrees Celsius).
* ##### _coolingBaseTemperature_ [Default]
Base temperature for cooling (in degrees Celsius).  Default is set to 18.3C but this can be much lower if the analysis is for a building with high heat gain or insulation.
* ##### _heatingBaseTemperature_ [Default]
Base temperature for heating (in degrees Celsius).  Default is set to 23.3C but this can be much lower if the analysis is for a building with high heat gain or insulation.
* ##### useDailyAvrMethod_ [Optional]
set to "True" to use the traditional method of degree days calculation, which will calculate the average temperature of each day and sum up all of these temperatures over the year.  This is opoosed to this component's default analysis, which will will examine each hour of the year and then convert results to degree-days.

#### Outputs
* ##### readMe!
A summary of the input.
* ##### daily_coolingDegDays
Cooling degree-days summed for each day of the year. For visualizations of over the whole year, connect this to the grasshopper chart/graph component. 
* ##### daily_heatingDegDays
Heating degree-days summed for each day of the year. For visualizations of over the whole year, connect this to the grasshopper chart/graph component. 
* ##### monthly_coolingDegDays
Cooling degree-days summed for each month of the year.
* ##### monthly_heatingDegDays
Heating degree-days summed for each month of the year.
* ##### annual_coolingDegDays
The total cooling degree-days for the entire year.
* ##### annual_heatingDegDays
The total heating degree-days for the entire year.


[Check Hydra Example Files for CDD_HDD](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_CDD_HDD)