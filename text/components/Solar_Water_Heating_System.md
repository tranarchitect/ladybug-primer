## ![](../../images/icons/Solar_Water_Heating_System.png) Solar Water Heating System

![](../../images/components/Solar_Water_Heating_System.png)

Use this component to define Solar water heating system settings.

#### Inputs
* ##### collectorType [Optional]
Type of the collector. The following ones can be used:
* ##### activeSWHsystem [Optional]
Define whether the swh system is active (pumped) or passive (not pumped).
* ##### openLoop [Optional]
Define whether the swh system has an open (indirect) or closed (indirect) solar loop.
* ##### numberOfStories [Optional]
Total number of stories plus basement (if there is a basement).
* ##### skyViewFactor [Optional]
Continuous Sky View Factor - portion of the visible sky (dome). It defines the shading of the parts of diffuse irradiance. It ranges from 0 to 1.
* ##### beamIndexPerHour [Optional]
Transmission index of beam (direct) irradiance for each hour during a year. It ranges from 0-1.

#### Outputs
* ##### readMe!
...
* ##### SWHsystemSettings
A list of all Solar water heating system settings. Plug it to SWHsurface component's "SWHsystemSettings_" input.


[Check Hydra Example Files for Solar Water Heating System](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Solar Water Heating System)