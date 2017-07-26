## ![](../../images/icons/Import_Sandia_Photovoltaics_Module.png) Import Sandia Photovoltaics Module

![](../../images/components/Import_Sandia_Photovoltaics_Module.png)

Use this component to import Photovoltaics module settings for particular module from "Sandia National Laboratories Modules" library.

#### Inputs
* ##### modulesLibraryFile [Required]
Add "Sandia National Laboratories Modules" .csv file path to this input.
* ##### moduleIndex [Optional]
An index corresponding to chosen module from "allModuleNames" output.
* ##### newModuleMountType [Optional]
New mounting type (configuration) of the module.
* ##### moduleActiveAreaPercent [Optional]
Percentage of the module's area excluding module framing and gaps between cells. 

#### Outputs
* ##### readMe!
...
* ##### allModuleNames
Names of all crystalline silicon modules from the "_modulesLibraryFile" file.
* ##### moduleName
Name of the chosen module, according to "moduleIndex_" input.
* ##### moduleMaterial
Material of the chosen module.
* ##### moduleMountType
Final mount type (configuration) of the chosen module.
* ##### moduleArea
Area of the chosen module.
* ##### modulePower
Module's power at maximum-power point of the chose module.
* ##### moduleEfficiency
Module's aperture (active area) efficiency.
* ##### sourceNotes
Source notes corresponding to the chosen module.
* ##### PVmoduleSettings
A list of PV module settings. Plug it to "Photovoltaics surface" component's "PVmoduleSettings_" input.


[Check Hydra Example Files for Import Sandia Photovoltaics Module](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Import Sandia Photovoltaics Module)