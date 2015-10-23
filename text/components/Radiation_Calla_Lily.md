## ![](../../images/icons/Radiation Calla Lily.png) Radiation_Calla_Lily

![](../../images/components/Radiation_Calla_Lily.png)

Use this component to draw Radiation Calla Lily or Dome, which shows you how radiation would fall on an object from all directions for a given sky.

#### Inputs
* ##### _selectedSkyMtx [Required]
The output from the selectSkyMtx component.
* ##### _horAngleStep_ [Default]
An angle in degrees between 0 and 360 that represents the step for horizontal rotation. Smaller numbers will yeild a finer and smoother mesh with smoother colors.  The number input here should be smaller than 360 and divisible by 360.  The default is set to 10 degrees.
* ##### _verAngleStep_ [Default]
Angle in degrees step between 0 and 90 that represents the step for vertical rotation. Smaller numbers will yeild a finer and smoother mesh with smoother colors.  The number input here should be smaller than 90 and divisible by 90.  The default is set to 10 degrees.
* ##### _centerPoint_ [Default]
Input a point to locate the center point of the Calla Lily Graph
* ##### _horScale_ [Default]
Input a number here to change horizontal (XY) scale of the graph. The default value is set to 1.  Note that, for the dome representation, this input will change the scale of the entire dome (both horizontal and vertical).
* ##### _verScale_ [Default]
Input a number here to change vertical (Z) scale of the graph. The default value is set to 1. Note that, for the dome representation, this input will have no effect.
* ##### domeOrLily_ [Optional]
Set to "True" to have the component create a radiation dome and set to "False" to have it generate a Lily.  The default is set to "False" for a Lily.
* ##### legendPar_ [Optional]
Optional legend parameters from the Ladybug Legend Parameters component.
* ##### _runIt [Required]
Set to "True" to run the component and generate a radiation Calla Lily.
* ##### bakeIt_ [Optional]
Set to "True" to bake the Calla Lily into the Rhino scene.

#### Outputs
* ##### readMe!
...
* ##### radiationLilyMesh
A colored mesh representing radiation of the Calla Lily or Dome.
* ##### baseCrvs
A set of guide curves for the Calla Lily.
* ##### legend
A legend of the radiation on the Calla Lily. Connect this output to a grasshopper "Geo" component in order to preview the legend in the Rhino scene.  
* ##### testPts
The vertices of the Calla Lily mesh.  These are hidden by default.
* ##### testPtsInfo
Information for each test point of the Calla Lily mesh.  "HRA" stands for "Horizontal Rotation Angle" while "VRA" stand for "Vertical Rotation Angle."  HRA varies from 0 to 360 while VRA varies from 0 to 90.
* ##### values
The radiation values for each test points (or mesh faces) of the Calla Lily in kWh/m2.
* ##### maxRadPt
The point on the Cala Lilly with the greatest amount of solar radiation.  This is useful for understanding the best direction to orient solar panels.
* ##### maxRadVector
The vector that should be used to orient solar panels such that they recieve the greatest possible solar radiation.
* ##### maxRadInfo
Information about the test point with the greates amount of radiation in the Calla Lily.  "HRA" stands for "Horizontal Rotation Angle" while "VRA" stand for "Vertical Rotation Angle."  HRA varies from 0 to 360 while VRA varies from 0 to 90.


[Check Hydra Example Files for Radiation Calla Lily](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Radiation Calla Lily)