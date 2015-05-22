How To Mix
==========
The **How To Mix** resource is a step-by-step description on how to make the drink.

### Resource Properties
<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Returns</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>id</td>
            <td>the id of the glass</td>
            <td>string</td>
        </tr>
        <tr>
            <td>name</td>
            <td>the name of the glass</td>
            <td>string</td>
        </tr>
        <tr>
            <td>languageBranch</td>
            <td>the language branch of the texts in the glass</td>
            <td>string</td>
        </tr>
        <tr>
            <td>steps</td>
            <td>the steps needed to mix this drink</td>
            <td>array of <a href="#mixing-step">mixing step</a></td>
        </tr>
    </tbody>
</table>

<h4 id="mixing-step">Mixing Step Properties</h4>
<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Returns</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>text</td>
            <td>the localized text describing the actions needed to perform this step</td>
            <td>string</td>
        </tr>
        <tr>
            <td>description</td>
            <td>a description of the ingredient used</td>
            <td>string</td>
        </tr>
		<tr>
            <td>imagePath</td>
            <td>the image path on Media server for this step</td>
            <td>string</td>
        </tr>
        <tr>
            <td>imageName</td>
            <td>the image to use for this step (apply a format and call the Media server)</td>
            <td>string</td>
        </tr>
		<tr>
            <td>action</td>
            <td>the action used for this step, i.e. fill</td>
            <td>string</td>
        </tr>
        <tr>
            <td>quantity</td>
            <td>the amount to use</td>
            <td>number</td>
        </tr>
		<tr>
            <td>unit</td>
            <td>the unit of the quantity</td>
            <td>string</td>
        </tr>
		<tr>
            <td>ingredient</td>
            <td>the name of the ingredient used in this step</td>
            <td>string</td>
        </tr>
		<tr>
            <td>ingredientType</td>
            <td>the type of ingredient used in this step</td>
            <td>string</td>
        </tr>
		<tr>
            <td>container</td>
            <td>the container used in this step</td>
            <td>string</td>
        </tr>
		<tr>
            <td>containerType</td>
            <td>the type of the container used in this step</td>
            <td>string</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
#### Showing Specific How To Mix

> /drinks/*drink_id*/howtomix/

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
