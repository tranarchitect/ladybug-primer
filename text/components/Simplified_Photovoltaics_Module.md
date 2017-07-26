## ![](../../images/icons/Simplified_Photovoltaics_Module.png) Simplified Photovoltaics Module

![](../../images/components/Simplified_Photovoltaics_Module.png)

Use this component to define simplified Photovoltaics crystalline silicon (c-Si) module settings.

#### Inputs
* ##### mountType [Optional]
Mounting type (configuration) of a module. There are three of them:
* ##### moduleEfficiency [Optional]
The ratio of electrical energy output from the PV module to input solar energy from the sun.
* ##### temperatureCoefficient [Optional]
A coefficient which accounts for the percentage the solar module's DC output power decrease/increase for every degree Celsius the solar cells temperature rises above/below 25C. 
* ##### moduleActiveAreaPercent [Optional]
Percentage of the module's area excluding module framing and gaps between cells. 

#### Outputs
* ##### readMe!
...
* ##### PVmoduleSettings
A list of PV module settings. Plug it to "Photovoltaics surface" component's "PVmoduleSettings_" input.


[Check Hydra Example Files for Simplified Photovoltaics Module](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Simplified Photovoltaics Module)