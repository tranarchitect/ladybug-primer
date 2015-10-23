## ![](../../images/icons/Comfort Shade Benefit Evaluator.png) Comfort_Shade_Benefit_Evaluator

![](../../images/components/Comfort_Shade_Benefit_Evaluator.png)

This is a component for visualizing the desirability of shade in terms of comfort temperature by using solar vectors, a series of hourly temperatures (usually outdoor temperatures), and an assumed balance temperature.  The balance temperature represents the median temperture that people find comfortable, which can vary from climate to climate but is usually somewhere around 20C.

#### Inputs
* ##### _location [Required]
The location output from the importEPW or constructLocation component.  This is essentially a list of text summarizing a location on the earth.
* ##### _temperatures [Required]
A stream of 8760 temperature values (including a header) representing the temperature at each hour of the year that will be used to evaluate shade benefit.  This can be the dryBulbTemperature from the 'Import EPW' component, the univeralThermalClimateIndex (UTCI) output from the 'Outdoor Comfort Calculator' component, or the standardEffectiveTemperature (SET) output from the 'PMV Comfort Calculator' component.  If you are using this component to evaluate shade for a passive building with no heating/cooling, this input can also be the indoor temperature of the zone to be shaded.
* ##### balanceTemperature_ [Optional]
An estimated balance temperature representing median temperture that people find comfortable, which can vary from climate to climate. The default is set to 17.5C, which is the median outdoor comfort temperature (UTCI) that defines the conditions of no thermal stress (9 < UTCI <26).
* ##### temperatureOffest_ [Optional]
An number represeting the offset from the balanceTemperature_ in degrees Celcius at which point the shade importance begins to have an effect.  The default is set to 8.5 C, which is the range of outdoor comfort temperature (UTCI) that defines the conditions of no thermal stress (9 < UTCI <26).
* ##### ============ []
...
* ##### _testShades [Required]
A Brep representing the shade to be evaluated for its benefit.
* ##### _testRegion [Required]
A brep representing an outdoor area for which shading is being considered or the window of a building that would be affected by the shade. Note that only breps with a single surface are supported now and volumetric breps will be included at a later point.
* ##### gridSize_ [Optional]
The length of each of the shade's test cells in model units.  Please note that, as this value gets lower, simulation times will increase exponentially even though this will give a higher resolution of shade benefit.
* ##### context_ [Optional]
Script variable ShadeBenefit
* ##### ============ []
Script variable Shade Benefit
* ##### north_ [Optional]
Input a vector to be used as a true North direction for the sun path or a number between 0 and 360 that represents the degrees off from the y-axis to make North.  The default North direction is set to the Y-axis (0 degrees).
* ##### skyResolution_ [Optional]
An interger equal to 0 or above to set the number of times that the tergenza sky patches are split.  A higher number will ensure a greater accuracy but will take longer.  At a sky resolution of 4, each hour's temperature is essentially matched with an individual sun vector for that hour.  At a resolution of 5, a sun vector is produced for every half-hour, at 6, every quarter hour, and so on. The default is set to 4, which should be high enough of a resolution to produce a meaningful reault in all cases.
* ##### delNonIntersect_ [Optional]
Set to "True" to delete mesh cells with no intersection with sun vectors.  Mesh cells where shading will have little effect because an equal amount of warm and cool temperature vectors will still be left in white.
* ##### legendPar_ [Optional]
Legend parameters that can be used to re-color the shade, change the high and low boundary, or sync multiple evaluated shades with the same colors and legend parameters.
* ##### parallel_ [Optional]
Set to "True" to run the simulation with multiple cores.  This can increase the speed of the calculation substantially and is recommended if you are not running other big or important processes.
* ##### _runIt [Required]
Set to 'True' to run the simulation.

#### Outputs
* ##### readMe!
...
* ##### ==========
...
* ##### sunVectors
The sun vectors that were used to evaluate the shade (note that these will increase as the sky desnity increases).
* ##### regionTestPts
Points across the test region surface from which sun vectors will be projected
* ##### shadeMesh
A colored mesh of the _testShades showing where shading is helpful (in satuated blue), harmful (in saturated red), or does not make much of a difference (white or desaturated colors).
* ##### legend
Legend showing the numeric values of degree-days that correspond to the colors in the shade mesh.
* ##### legendBasePoint
Script variable Shade Benefit
* ##### ==========
Script variable Shade Benefit
* ##### shadeHelpfulness
The cumulative temperture degree-days/square Rhino model unit helped by shading the given cell. (C-day/m2)*if your model units are meters.
* ##### shadeHarmfulness
The cumulative heating degree-days/square Rhino model unit harmed by shading the given cell. (C-day/m2)*if your model units are meters. Note that these values are all negative due to the fact that the shade is harmful. 
* ##### shadeNetEffect
The sum of the helpfulness and harmfulness for each cell.  This will be negative if shading the cell has a net harmful effect and positive if the shade has a net helpful effect.


[Check Hydra Example Files for Comfort Shade Benefit Evaluator](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Comfort Shade Benefit Evaluator)