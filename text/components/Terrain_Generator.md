## ![](../../images/icons/Terrain_Generator.png) Terrain Generator

![](../../images/components/Terrain_Generator.png)

This component uses Google Maps API to achieve elevation data and satellite images of the terrain generated.

#### Inputs
* ##### location [Required]
It accepts two type of inputs.
* ##### basePoint [Default]
Input a point here to georeference the terrain model.
* ##### radius [Default]
A radius to make the terrain 3D model in Rhino model units. The default is set to 100.
* ##### type [Optional]
Select the type of output:
* ##### numOfTiles [Default]
Set the number of tiles (e.g. 4, that means 4x4). If no input is connected this will be 3 (tiles: 3x3).
* ##### numDivision [Default]
Set the number of points for each tile. If no input is connected this will be 12 (grid: 13x13).
* ##### imgResolution [Default]
Connect an integer number which manage the quality of single satellite image.
* ##### mapType [Optional]
Connect an integer number, from 0 to 3, which manages the formats of map.
* ##### folder [Optional]
The folder into which you would like to write the image file. This should be a complete file path to the folder.  If no folder is provided, the images will be written to C:/USERNAME/AppData/Roaming/Ladybug/IMG_Google.
* ##### runIt [Required]
Set to "True" to run the component and generate the 3D terrain model. 

#### Outputs
* ##### readMe!
...
* ##### pointsGeo
WSG84 coordinates of the grid points (longitude, latitude).
* ##### pointsXY
Cartesian coordinates of the grid points (X, Y).
* ##### pointsZ
Z values of the grid points. Connect this output to a Z vector to move the pointsXY in the right positions.
* ##### tiles
The area which will be calculated. If you want to visualize Satellite images connect this output to 'G' input of 'Human Custom Preview Material'.
* ##### imagePath
Satellite images from Google Static Maps API. Connect it to 'DB' input of 'Human Custom Preview Material' to apply textures to the 3d model or to the list of input surfaces.
* ##### terrain
3D terrain model.
* ##### origin
The origin (center) point of the "terrain" geometry.
* ##### elevation
Elevation of the origin_ input.


[Check Hydra Example Files for Terrain Generator](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Terrain Generator)