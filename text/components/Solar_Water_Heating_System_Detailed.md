## ![](../../images/icons/Solar_Water_Heating_System_Detailed.png) Solar Water Heating System Detailed

![](../../images/components/Solar_Water_Heating_System_Detailed.png)

Use this component to define a detailed Solar water heating system settings.

#### Inputs
* ##### collectorOpticalEfficiency [Optional]
Fr(tau alpha) Collector's optical efficiency coefficient. Also called Collector heat removal factor. Varies based on collector's type. Some default values by type:
* ##### collectorThermalLoss [Optional]
(FrUL) Collector's thermal loss coefficient. Varies based on collector's type. Some default values by type:
* ##### collectorActiveAreaPercent [Optional]
Percentage of the collector's area excluding collector framing, lateral insulation, or gaps between evacuated tubes... Also called aperture area.
* ##### workingFluidHeatCapacity [Optional]
Specific heat of the working fluid.
* ##### flowRatePerM2 [Optional]
Test flow rate of working fluid through the collector per square meter of collector's area.
* ##### IAMcoefficient [Optional]
Incidence angle modifier coefficient (bo) - Use this input to account for collector efficiency losses due to different angles of incidence.
* ##### skyViewFactor [Optional]
Continuous Sky View Factor - portion of the visible sky (dome). It defines the shading of the parts of diffuse irradiance. It ranges from 0 to 1.
* ##### beamIndexPerHour [Optional]
Transmission index of beam (direct) irradiance for each hour during a year. It ranges from 0-1.
* ##### maxWorkingTemperature [Optional]
Maximal working temperature of the tank storage.
* ##### dischargeTemperature [Optional]
Storage tank temperature at which the discharge of the excess heat and cold water makeup stops.
* ##### deliveryWaterTemperature [Optional]
Water heater lower thermostat setting. Depends on the type of usage of solar hot water system. In Celsius
* ##### avrJanuaryColdWaterTemperature [Optional]
Average January cold water inlet temperature. This is the temperature of the water from the local pipe grid.
* ##### mechanicalRoomTemperature [Optional]
Temperature of the room where the storage tank will be located.
* ##### pipeLength [Optional]
Total pipes length run in the solar loop.
* ##### pipeDiameter [Optional]
Average pipes inner diameter, in milimeters.
* ##### pipeInsulationThickness [Optional]
Thickness of the pipes insulation, in milimeters.
* ##### pipeInsulationConductivity [Optional]
Pipe's insulation thermal conductivity (k value).
* ##### pumpPower [Optional]
Overall circulation pumps power.
* ##### pumpEfficiency [Optional]
Circulation pumps efficiency (ni) - ratio between hydraulic and supplied, electrical power.
* ##### tankSize [Optional]
Storage tank volume in liters.
* ##### tankLoss [Optional]
Storage tank's heat loss coefficient (U). Varies from 0.30 to 0.50 depending on the tank volume, insulation type, thickness ...
* ##### heightDiameterTankRatio [Optional]
Storage tank height and diameter ratio. It mostly ranges from 1 to 3.
* ##### heatExchangerEffectiveness [Optional]
Depends on the type of heat exchanger: its transfer coefficient, surface, flow rates, working fluid...

#### Outputs
* ##### readMe!
...
* ##### SWHsystemSettings
A list of all Solar water heating system settings. Plug it to SWHsurface component's "SWHsystemSettings_" input.


[Check Hydra Example Files for Solar Water Heating System Detailed](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Solar Water Heating System Detailed)