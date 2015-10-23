## ![](../../images/icons/Body Characteristics.png) Body_Characteristics

![](../../images/components/Body_Characteristics.png)

Use this component to calculate the Basal Metabolic Rate, Body Mass Index indices and to create the "bodyCharacterstics_" input for the "Thermal comfort indices" component.

#### Inputs
* ##### age_ [Optional]
An age of the person in years.
* ##### gender_ [Optional]
Person's gender.
* ##### height_ [Optional]
Person's height in centimetres.
* ##### weight_ [Optional]
Person's weight in kilograms.
* ##### bodyPosition_ [Optional]
Position of person's body.
* ##### clothingInsulation_ [Optional]
Clothing insulation of a person in "clo" units.
* ##### acclimated_ [Optional]
Determine whether the test person had previously experienced heat/cold stress.
* ##### metabolicRate_ [Optional]
Activity's metabolic rate in mets. If not supplied 2.32 will be used as default value
* ##### activityDuration_ [Optional]
Duration of the activity sequence in minutes.

#### Outputs
* ##### readMe!
...
* ##### BMR
Basal Metabolic Rate - represents the minimum daily amount of energy needed to keep your body functioning, including breathing and keeping your heart beating, without lossing weight. It does not include the the calories you burn from normal daily activities or exercise.
* ##### BMI
Body Mass Index - is the ratio of the persons weight to square of height. It is generally used as a method of screening for weight category.
* ##### BMILevel
Level of BMI for adult (18 years and older) males and females:
* ##### bodyCharacteristics
A list of inputted values (age, gender, height, weight, bodyPosition, clothingInsulation, acclimated, metabolicRate, activityDuration).


[Check Hydra Example Files for Body Characteristics](https://hydrashare.github.io/hydra/index.html?keywords=Ladybug_Body Characteristics)