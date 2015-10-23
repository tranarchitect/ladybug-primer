## ![](../../images/icons/Sunpath Shading.png) Sunpath_Shading

![](../../images/components/Sunpath_Shading.png)

This component calculates the amount of annual shading of sun window due to location's surroundings. Sun (or solar) window being an area of the the sky dome between winter and summer solstice sun paths.

#### Inputs
* ##### _PVsurface [Required]
Input planar Surface (not polysurface) on which the PV modules/Solar hot water collectors will be applied. If you have a polysurface, explode it (using "Deconstruct Brep" component) and then feed its Faces(F) output to _PVsurface. Surface normal should be faced towards the sun.
* ##### _epwFile [Required]
Input .epw file path by using grasshopper's "File Path" component.
* ##### ACenergyPerHour_ [Optional]
Input the "ACenergyPerHour" output data from "Photovoltaics surface" component.
* ##### context_ [Optional]
Buildings, structures, mountains and other permanent obstructions. Input polysurfaces, surfaces, or meshes.
* ##### coniferousTrees_ [Optional]
This input allows for partial shading from coniferous(evergreen) context trees.
* ##### deciduousTrees_ [Optional]
This input allows for partial shading during in-leaf and leaf-less periods from deciduous context trees.
* ##### coniferousAllyearIndex_ [Optional]
All year round transmission index for coniferous(evergreen) context trees. It ranges from 0 to 1.0. 0 represents deciduous trees which do not allow solar radiation to pass through them (100% shading). 1 represents all solar radiation passing through deciduous trees, like the trees do not exist (0% shading).
* ##### deciduousInleafIndex_ [Optional]
Deciduous context trees transmission index for in-leaf period. In-leaf being a period from 21st March to 21st September in the northern hemisphere, and from 21st September to 21st March in the southern hemisphere.
* ##### deciduousLeaflessIndex_ [Optional]
Deciduous context trees transmission index for leaf-less period. Leaf-less being a period from 21st September to 21st March in the northern hemisphere, and from 21st March to 21st September in the in the southern hemisphere.
* ##### leaflessPeriod_ [Optional]
Define the leafless period for deciduous trees using Ladybug's "Analysis Period" component.
* ##### north_ [Optional]
Input a vector to be used as a true North direction, or a number between 0 and 360 that represents the clockwise degrees off from the Y-axis.
* ##### _______________ [Default]
Script variable PhotovoltaicsShading
* ##### scale_ [Optional]
Scale of the overall geometry (sunPath curves, sunWindow mesh).
* ##### hoursPositionScale_ [Optional]
Scale factor for positioning of solar time hour points (that's "hoursPositions" output).
* ##### precision_ [Optional]
Overall shading precision. Ranges from 1-100. It represents the square root number of shading analysis points per sun window quadrant.
* ##### legendPar_ [Optional]
Optional legend parameters from the Ladybug "Legend Parameters" component.
* ##### _______________ [Default]
Script input _________________.
* ##### bakeIt_ [Optional]
Set to "True" to bake the Sunpath shading results into the Rhino scene.
* ##### _runIt [Required]
...

#### Outputs
* ##### readMe!
...
* ##### _____________________
Script variable PhotovoltaicsShading
* ##### beamIndexPerHour
Transmission index of beam (direct) irradiance for each hour during a year.
* ##### sunWindowShadedAreaPer
Percent of the overall sun window shaded area. It is calculated for PVsurface area centroid. It ranges from 0-100(%).
* ##### unweightedAnnualShading
Annual unweighted shading of the active sun window quadrants. Active sun window quadrants are only those which produce AC energy (or solar radiation in case you are using this component for other purposes than Photovoltaics)
* ##### Sep21toMar21Shading
Weighted shading of the active sun window quadrants, for period between 21st September to 21st March. Active sun window quadrants are only those which produce AC energy (or solar radiation in case you are using this component for other purposes than Photovoltaics)
* ##### Mar21toSep21Shading
Weighted shading of the active sun window quadrants, for period between 21st March to 21st September. Active sun window quadrants are only those which produce AC energy (or solar radiation in case you are using this component for other purposes than Photovoltaics)
* ##### annualShading
Annual weighted shading of the active sun window quadrants. To calculate it, input data to "ACenergyPerHour_" input.
* ##### _____________________
Script variable PhotovoltaicsShading
* ##### annalysisPts
Each vertex of the inputted _PVsurface for which a separate shading analysis was conducted.
* ##### sunWindowCenPt
The center point of the "sunWindowCrvs" and "sunWindowMesh" geometry. It is calculated for PVsurface area centroid.
* ##### sunWindowCrvs
Geometry of the sun window based on 3D polar sun path diagram. Perpendical curves represent solar time hours. Horizontal arc curves represent sun paths for: 21st December, 21st November/January, 21st October/February, 21st September/March, 21st August/April, 21st July/May, 21st June.
* ##### sunWindowMesh
Sun window mesh based on 3D polar sun path diagram. It is calculated for PVsurface area centroid.
* ##### legend
A legend of the sunWindowMesh. Connect this output to a Grasshopper's "Geo" parameter in order to preview the legend separately in the Rhino scene.  
* ##### legendBasePt
Legend base point, which can be used to move the "legend" geometry with grasshopper's "Move" component.
* ##### quadrantCentroids
Centroid for each sun window active quadrant above the horizon.
* ##### quadrantShadingPercents
Shadinging percent per each sun window active quadrant above the horizon. Active quadrants with less than 0.01% are neglected.
* ##### quadrantACenergyPercents
AC energy percent per each sun window active quadrant above the horizon.
* ##### hoursPositions
Solar time hour point positions.
* ##### hours
Solar time hour strings.


[Check Hydra Example Files for Sunpath Shading](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Sunpath Shading)