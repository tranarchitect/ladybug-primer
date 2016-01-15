## ![](../../images/icons/Photovoltaics_Module.png) Photovoltaics Module

![](../../images/components/Photovoltaics_Module.png)

Use this component to define the Photovoltaics module settings.

#### Inputs
* ##### moduleType [Optional]
Module type and mounting configuration:
* ##### moduleEfficiency [Optional]
The ratio of electrical energy output from the PV module to input solar energy from the sun.
* ##### temperatureCoefficient [Optional]
A coefficient which accounts for the percentage the solar module's DC output power decrease/increase for every degree Celsius the solar cells temperature rises above/below 25°C. 
* ##### moduleActiveAreaPercent [Optional]
Percentage of the module's area excluding module framing and gaps between cells. 

#### Outputs
* ##### readMe!
...
* ##### PVmoduleSettings
A list of PV module settings. Plug it to "Photovoltaics surface" component's "PVmoduleSettings_" input.


[Check Hydra Example Files for Photovoltaics Module](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Photovoltaics Module)