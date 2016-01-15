## ![](../../images/icons/Residential_Hot_Water.png) Residential Hot Water

![](../../images/components/Residential_Hot_Water.png)

Use this component to calculate domestic hot water consumption for each hour during a year, for a single family household (house).

#### Inputs
* ##### epwFile [Required]
Input .epw file path by using the "File Path" parameter, or Ladybug's "Open EPW And STAT Weather Files" component.
* ##### totalNumberOfPersons [Required]
Total number of persons in a household.
* ##### numberOfPreSchoolChildren [Optional]
Number of preschool children(0-5) in household.
* ##### numberOfSchoolChildren [Optional]
Number of school age(6-13) children in household.
* ##### numberOfAdults [Optional]
Number of adults (14 years and older) in household.
* ##### numberOfAdultsAtHome [Optional]
Number of adults that stay at home during a day.
* ##### seniorOnly [Optional]
Senior only household.
* ##### dishWasher [Optional]
A household owns a dish washer.
* ##### clothsWasher [Optional]
A household owns a cloths washer.
* ##### payUtilityBill [Optional]
Household occupants pay a utility bill.
* ##### firstWeekStartDay [Optional]
A day of week on which a year starts (1 - Monday, 2 - Tuesday, 3 - Wednesday...)
* ##### weekendDays [Optional]
Define a list of two weekend (nonworking) days. Through out the World, countries have different days as their weekend days:
* ##### holidayDays [Optional]
List of days (1 to 365) which are holiday (nonworking) days.
* ##### deliveryWaterTemperature [Optional]
Required (set) water temperature.
* ##### coldWaterTemperaturePerHour [Optional]
Cold (inlet) water temperature supplied from public water system, for each hour during a year. In Celsius.
* ##### runIt [Required]
...

#### Outputs
* ##### readMe!
...
* ##### heatingLoadPerHour
Thermal energy (or electrical energy) required to heat the domestic hot water consumption for each hour during a year.
* ##### hotWaterPerHour
Domestic hot water consumption for each hour during a year.
* ##### hotWaterPerYear
Domestic hot water consumption for a whole year.
* ##### averageDailyHotWaterPerYear
Average daily hot water consumption for a whole year.
* ##### maximumDailyConsumption
Maximal hot water consumption per day during a year.
* ##### maximumConsumptionDay
Day with maximal hot water consumption.
* ##### minimumDailyConsumption
Minimal hot water consumption per day during a year.
* ##### minimumConsumptionDay
Day with minimal hot water consumption.


[Check Hydra Example Files for Residential Hot Water](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Residential Hot Water)