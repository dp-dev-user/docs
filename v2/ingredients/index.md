Ingredient
==========

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
            <td>the identifier of the ingredient</td>
            <td>string</td>
        </tr>
        <tr>
            <td>name</td>
            <td>the name of the ingredient</td>
            <td>string</td>
        </tr>
        <tr>
            <td>languageBranch</td>
            <td>the language of the texts in the ingredient</td>
            <td>string</td>
        </tr>
        <tr>
            <td>description</td>
            <td>a text describing the ingredient</td>
            <td>string</td>
        </tr>
        <tr>
            <td>isCarbonated</td>
            <td>whether the ingredient is carbonated or not</td>
            <td>bool</td>
        </tr>
        <tr>
            <td>isAlcoholic</td>
            <td>whether the ingredient contains alcohol</td>
            <td>bool</td>
        </tr>
        <tr>
            <td>isBaseSpirit</td>
            <td>whether the ingredient is a base spirit</td>
            <td>bool</td>
        </tr>
        <tr>
            <td>isJuice</td>
            <td>whether the ingredient is a juice</td>
            <td>bool</td>
        </tr>
        <tr>
            <td>type</td>
            <td>the id of the type this ingredient falls under</td>
            <td>string</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
#### Listing Ingredients

> /ingredients/

#### Showing specific Ingredient(s)

> /ingredients/*ingredient_id*/

> /ingredients/*ingredient_id1*,*ingredient_id2*/

#### Search

> /ingredients/search/*search query*/

## Connections
#### [Drinks By Ingredient](/drinks-api/docs/v2/drinks)

> /drinks/with/*ingredient_id*/

#### [Images](/drinks-api/docs/v2/assets#images)

> http://assets.absolutdrinks.com/ingredients/*ingredient_id.format*

## JavaScript Client Library
#### Listing Actions

``` js
addb.ingredients().loadSet(function(query) { });
addb.ingredients('es').skip(10).take(25).loadSet(function(query) { });
```

#### Loading Specific Action

``` js
addb.ingredients().load('shake', function(shake) { });
```

#### Auto Suggest Search (on name)

``` js
addb.ingredients().quickSearch('some query', function(query) { });
```

## .NET Client Library
#### Listing Actions

``` csharp
var ingredients = ADDbClient.Ingredients().Skip(5).Take(20);
```

#### Loading Specific Action

``` csharp
var ingredient = ADDbClient.Ingredients().Load("lemon");
var ingredients = ADDbClient.Ingredients("es").Load(new [] { "absolut-vodka", "absolut-watkins" });
```

#### Auto Suggest (on name)

``` csharp
var ingredients = ADDbClient.Ingredients().QuickSearch("some query");
```
