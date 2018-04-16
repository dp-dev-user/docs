(DEPRECATED) ﻿How To Mix
==========
**The howToMix-text is included in the drink**
*The **How To Mix** resource is a step-by-step description on how to make the drink.*


### Resource Properties
Name|Description|Returns
--- | --- | ---
id|the id of the glass|string
name|the name of the glass|string
languageBranch|the language of the texts|string
steps|the steps needed to mix this drink|array of mixingStep

*MixingStep Properties*

Name|Description|Returns
--- | --- | ---
text|the localized text describing the actions needed to perform this step|string
description|a description of the ingredient used|string
imagePath|the image path on Media server for this step|string
imageName|the image to use for this step (apply a format and call the Media server)|string
action|the action used for this step, i.e. fill|string
quantity|the amount to use|number
unit|the unit of the quantity|string
ingredient|the name of the ingredient used in this step|string
ingredientType|the type of ingredient used in this step|string
container|the container used in this step|string
containerType|the type of the container used in this step|string

## HTTP(s) GET Operations
#### Showing Specific How To Mix

&gt; /drinks/*drink_id*/howtomix/

## JavaScript Client Library
#### Showing specific How To Mix

``` js
addb.drinks().howtomix('absolut-cosmopolitan', function(howtomix) { });
```

## .NET Client Library
#### Showing specific How To Mix

``` csharp
var howToMix = ADDbClient.Drinks().HowToMix("absolut-cosmopolitan");
```
