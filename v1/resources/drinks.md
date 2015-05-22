Drink
==============
The Drink is ADDb:s main resource. It contains all the information needed to create the drink.

### Drink Properties

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
			<td>The id of the drink</td>
			<td>string</td>
		</tr>
		<tr>
			<td>name</td>
			<td>the name of the drink</td>
			<td>string</td>
		</tr>
		<tr>
			<td>description</td>
			<td>a general text describing the steps needed to mix the drink</td>
			<td>string</td>
		</tr>
			<tr>
			<td>descriptionPlain</td>
			<td>a general text describing the steps needed to mix the drink, without tags</td>
			<td>string</td>
		</tr>
		<tr>
			<td>story</td>
			<td>a story about the drink if exists</td>
			<td>string</td>
		</tr>
		<tr>
			<td>color</td>
			<td>the color of the drink</td>
			<td>string</td>
		</tr>
		<tr>
			<td>languageBranch</td>
			<td>the language branch of the texts in the drink</td>
			<td>string</td>
		</tr>
		<tr>
			<td>rating</td>
			<td>the drinks rating by our bartender</td>
			<td>integer</td>
		</tr>
		<tr>
			<td>skill</td>
			<td>the skillevel needed to mix the drink</td>
			<td>skill</td>
		</tr>
		<tr>
			<td>video</td>
			<td>videos of this drink</td>
			<td>array of <a href="/drinks-api/docs/v1/general/video-reference">video reference</a>s</td>
		</tr>
		<tr>
			<td>isAlcoholic</td>
			<td>if the drink contains alcohol</td>
			<td>boolean</td>
		</tr>
		<tr>
			<td>isCarbonated</td>
			<td>if the drink is carbonated</td>
			<td>boolean</td>
		</tr>
		<tr>
			<td>isHot</td>
			<td>if the drink is hot</td>
			<td>boolean</td>
		</tr>
		<tr>
			<td>servedIn</td>
			<td>the type of glass the drink should be served in</td>
			<td><a href="/drinks-api/docs/v1/general/entity-reference">entity reference</a> to <a href="/drinks-api/docs/v1/glasses">glass</a></td>
		</tr>
		<tr>
			<td>ingredients</td>
			<td>the ingredients in the drink</td>
			<td>array of <a href="#drink-ingredient">drink ingredient</a></td>
		</tr>
		<tr>
			<td>tastes</td>
			<td>the tastes of the drink</td>
			<td>array of <a href="/drinks-api/docs/v1/general/entity-reference">entity reference</a> to <a href="/drinks-api/docs/v1/tastes">taste</a></td>
		</tr>
		<tr>
			<td>occasions</td>
			<td>the occasions this drink is suitable for</td>
			<td>array of <a href="/drinks-api/docs/v1/general/entity-reference">entity reference</a> to <a href="/drinks-api/docs/v1/occasions">occasion</a></td>
		</tr>
		<tr>
			<td>tools</td>
			<td>the tools that is used for this drink</td>
			<td>array of <a href="/drinks-api/docs/v1/general/entity-reference">entity reference</a> to <a href="/drinks-api/docs/v1/tools">tool</a></td>
		</tr>
		<tr>
			<td>drinkTypes</td>
			<td>the types this drink is filed under</td>
			<td>array of <a href="/drinks-api/docs/v1/general/entity-reference">entity reference</a> to <a href="/drinks-api/docs/v1/drinktypes">drink type</a></td>
		</tr>
		<tr>
			<td>actions</td>
			<td>the actions that needs to be performed to make this drink</td>
			<td>array of <a href="/drinks-api/docs/v1/general/entity-reference">entity reference</a> to <a href="/drinks-api/docs/v1/actions">action</a></td>
		</tr>
		<tr>
		<tr>
			<td>brands</td>
			<td>the brands that the drink belongs to</td>
			<td>array of string</td>
		</tr>
		<tr>
			<td>tags</td>
			<td>the tags you have applied on this drink (if any)</td>
			<td>array of <a href="/drinks-api/docs/v1/tags">tags</a></td>
		</tr>
	</tbody>
</table>

### Drink Ingredient Properties
<table id="drink-ingredient">
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
			<td>the identifier of the ingredient</td>
			<td>string</td>
		</tr>
		<tr>
			<td>type</td>
			<td>the type of the ingredient</td>
			<td>string</td>
		</tr>
		<tr>
			<td>text</td>
			<td>the friendly text of this ingredient</td>
			<td>string</td>
		</tr>
		<tr>
			<td>textPlain</td>
			<td>the plain text of this ingredient without tags</td>
			<td>string</td>
		</tr>
	</tbody>
</table>

## HTTP(s) GET Operations

#### Listing Drinks

> /drinks/

#### Showing specific drink(s)

> /drinks/*drink_id*/

> /drinks/*drink_id1*,*drink_id2*/

#### Auto Suggest (on name)

> /quickSearch/drinks/*search query*/

### Filtering
A filter is made up with a key and filtering value ex. "with/lemon-juice". 
To make a query for drink recipes that contains *Lemon Juice* 
you call the url **/drinks/with/lemon-juice/**. If you also want to add a filter for drinks suitable for the 
evening the url would be **/drinks/with/lemon-juice/for/evening/**.

#### By Ingredients

> /drinks/with/*ingredient_id*/

#### By Ingredient type

> /drinks/withtype/*ingredient_type_id*/

#### By Taste

> /drinks/tasting/*taste_id*/

#### By Occasion

> /drinks/for/*occasion_id*/

#### By Tool

> /drinks/madewith/*tool_id*/

#### By Rating

> /drinks/rating/*numerical_condition*/

#### By Skill

> /drinks/skill/*skill_value*/

#### By Alcoholic

> /drinks/alcoholic/  
> /drinks/not/alcoholic/

#### By Existance of Video

> /drinks/hasvideo/  
> /drinks/not/hasvideo/  

#### By Carbonation

> /drinks/carbonated/  
> /drinks/not/carbonated/ 

#### By Serving Glass

> /drinks/servedin/*glass_id*/

#### By Action

> /drinks/doing/*action_id*/

#### By Color

> /drinks/colored/*color*/  

Available values for color are:

- red
- pink
- yellow
- brown
- blue
- green
- purple
- transparent
- white

#### By Tag

> /drinks/tagged/*tag_name*/

### Conditions

- **numerical_condition** 
	- "gt50" (greater than 50)
	- "gte30" (greater or equal than 30)
	- "lt50" (less than 50)
	- "lte60" (less or equal than 60)
	- "50" (exactly 50)

### Excluding filter

To exclude the next filter matches, add **/not/** before it: 
> /drinks/not/tasting/berry/  
> /drinks/not/with/lime/

### and/or filter

To build conditions in filter
> /drinks/with/absolut-vodka/and/lime/  
> /drinks/tasting/berry/or/sweet/

## Connections
#### [How To Mix](/drinks-api/docs/v1/howtomix)

> /drinks/*drink_id*/howtomix/

#### [Images](/drinks-api/docs/v1/assets#images)

> http://assets.absolutdrinks.com/drinks/*drink_id*.*format*

## JavaScript Client Library
#### Listing drinks

``` js
addb.drinks().loadSet(function(query) { });
addb.drinks('es').skip(10).take(25).loadSet(function(query) { });
```

#### Loading Specific drinks

``` js
addb.drinks().load('absolut-cosmopolitan', function(shake) { });
```

#### Auto Suggest Search (on name)

``` js
addb.drinks().quickSearch('some query', function(query) { });
```

#### Filtering

``` js
addb.drinks()
	.withIngredient('lemon')
	.and('apples')
	.tasting('sweet')
	.loadSet(function(query) { });
```

## .NET Client Library
#### Listing drinks

``` csharp
var drinks = ADDbClient.Drinks().Skip(5).Take(20);
```

#### Loading Specific drinks

``` csharp
var drinks = ADDbClient.Drinks().Load("absolut-cosmopolitan");
var drinks = ADDbClient.Drinks("es").Load(new [] { "absolut-cosmopolitan", "dry-martini" });
```

#### Auto Suggest (on name)

``` csharp
var drinks = ADDbClient.Drinks().QuickSearch("some query");
```

#### Filtering

``` csharp
var drinks = ADDbClient.Drinks()
	.With("lemon")
	.And("apples")
	.Tasting("sweet")
	.Skip(10)
	.Take(20);
```