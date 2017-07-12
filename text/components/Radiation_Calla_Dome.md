## ![](../../images/icons/Radiation_Calla_Dome.png) Radiation Calla Dome

![](../../images/components/Radiation_Calla_Dome.png)

Use this component to draw Radiation Calla Dome, which shows you how radiation would fall on an object from all directions for a given sky.

#### Inputs
* ##### selectedSkyMtx [Required]
The output from the selectSkyMtx component.
* ##### horAngleStep [Default]
An angle in degrees between 0 and 360 that represents the step for horizontal rotation. Smaller numbers will yeild a finer and smoother mesh with smoother colors.  The number input here should be smaller than 360 and divisible by 360.  The default is set to 10 degrees.
* ##### verAngleStep [Default]
Angle in degrees step between 0 and 90 that represents the step for vertical rotation. Smaller numbers will yeild a finer and smoother mesh with smoother colors.  The number input here should be smaller than 90 and divisible by 90.  The default is set to 10 degrees.
* ##### centerPoint [Default]
Input a point to locate the center point of the Calla Lily Graph
* ##### scale [Default]
Input a number here to change horizontal (XY) scale of the graph. The default value is set to 1.  Note that, for the dome representation, this input will change the scale of the entire dome (both horizontal and vertical).
* ##### projection [Default]
A number to set the projection of the sky hemisphere.  The default is set to draw a 3D hemisphere.  Choose from the following options:
* ##### legendPar [Optional]
Optional legend parameters from the Ladybug Legend Parameters component.
* ##### bakeIt [Optional]
An integer that tells the component if/how to bake the bojects in the Rhino scene.  The default is set to 0.  Choose from the following options:
* ##### runIt [Required]
Set to "True" to run the component and generate a radiation Calla Dome.

#### Outputs
* ##### readMe!
...
* ##### radiationMesh
A colored mesh representing radiation of the Calla Dome.
* ##### baseCrvs
A set of guide curves for the Calla Dome.
* ##### altitudeCrvs
Script variable radiationCallaLily
* ##### legend
A legend of the radiation on the Calla Dome. Connect this output to a grasshopper "Geo" component in order to preview the legend in the Rhino scene.  
* ##### testPts
The vertices of the Calla Dome mesh.  These are hidden by default.
* ##### testPtsInfo
Information for each test point of the Calla Dome mesh.  "HRA" stands for "Horizontal Rotation Angle" while "VRA" stand for "Vertical Rotation Angle."  HRA varies from 0 to 360 while VRA varies from 0 to 90.
* ##### values
The radiation values for each test points (or mesh faces) of the Calla Doem in kWh/m2.
* ##### maxRadPt
The point on the Cala Lilly with the greatest amount of solar radiation.  This is useful for understanding the best direction to orient solar panels.
* ##### maxRadVector
The vector that should be used to orient solar panels such that they recieve the greatest possible solar radiation.
* ##### maxRadInfo
Information about the test point with the greates amount of radiation in the Calla Dome.  "HRA" stands for "Horizontal Rotation Angle" while "VRA" stand for "Vertical Rotation Angle."  HRA varies from 0 to 360 while VRA varies from 0 to 90.


[Check Hydra Example Files for Radiation Calla Dome](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Radiation Calla Dome)