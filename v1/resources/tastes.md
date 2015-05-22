Taste
=====

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
            <td>the identifier of the taste</td>
            <td>string</td>
        </tr>
        <tr>
            <td>name</td>
            <td>the name of the taste</td>
            <td>string</td>
        </tr>
        <tr>
            <td>languageBranch</td>
            <td>the language of the texts in the taste</td>
            <td>string</td>
        </tr>
        <tr>
            <td>description</td>
            <td>a general text that describes the taste</td>
            <td>string</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
#### Listing Tastes

> /tastes/

#### Showing Specific Taste(s)

> /tastes/*taste_id*/

> /tastes/*taste_id1*,*taste_id2*/

#### Auto Suggest (on name)

> /quickSearch/tastes/*search query*/

## Connections
#### [Drinks By Taste](/drinks-api/docs/v1/drinks)

> /drinks/tasting/*taste_id*/

#### [Images](/drinks-api/docs/v1/assets#images)

> http://assets.absolutdrinks.com/tastes/*taste_id.format*

## JavaScript Client Library
#### Listing Tastes

``` js
addb.actions().loadSet(function(query) { });
addb.actions('es').skip(10).take(25).loadSet(function(query) { });
```

#### Loading Specific Taste

``` js
addb.tastes().load('sweet', function(shake) { });
```

#### Auto Suggest Search (on name)

``` js
addb.tastes().quickSearch('some query', function(query) { });
```

## .NET Client Library
#### Listing Tastes

``` csharp
var tastes = ADDbClient.Tastes().Skip(5).Take(20);
```

#### Loading Specific Taste(s)

``` csharp
var taste = ADDbClient.Tastes().Load("sweet");
var tastes = ADDbClient.Tastes("es").Load(new [] { "sweet", "sour" });
```

#### Auto Suggest (on name)

``` csharp
var tastes = ADDbClient.Tastes().QuickSearch("some query");
```