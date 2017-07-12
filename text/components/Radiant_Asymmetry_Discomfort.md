## ![](../../images/icons/Radiant_Asymmetry_Discomfort.png) Radiant Asymmetry Discomfort

![](../../images/components/Radiant_Asymmetry_Discomfort.png)

Use this component to calculate discomfort from radiant assymetry.

#### Inputs
* ##### radTempDifference [Required]
The temperature difference between one side of a pla
* ##### radAsymmType [Required]
An integer that represents the type of radiant assymetry being evaluated.  Occupants are more sensitive to warm cielings and cool walls than cool ceilings and warm walls.  Choose from the following options:
* ##### PPDThreshold [Optional]
The percentage of people dissatisfied (PPD) above which conditions are not longer considered acceptable.  The default is set to 5%, which is the specification for the ASHRAE 55 comfort standard.  The EN-7730 varies from 6% to 10% depending on the building class.

#### Outputs
* ##### readMe!
...
* ##### PPD
The percentage of people dissatisfied (PPD) from radiant asymmetry.
* ##### comfOrNot
A lidt of 0's and 1's (or "False" and "True" values) indicating whether occupants are comfortable under the input conditions.


[Check Hydra Example Files for Radiant Asymmetry Discomfort](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Radiant Asymmetry Discomfort)