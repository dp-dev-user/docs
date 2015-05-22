Glass Methods
=============
A *Glass* represents a serving glass in which drinks are served.

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
            <td>description</td>
            <td>The description of the glass</td>
            <td>string</td>
        </tr>
        <tr>
            <td>languageBranch</td>
            <td>the language branch of the texts in the glass</td>
            <td>string</td>
        </tr>
        <tr>
            <td>videos</td>
            <td>a list of videos</td>
            <td>array of <a href="/drinks-api/docs/v2/general/video-reference">video reference</a>s</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
#### Listing Glasses

> /glasses/

#### Showing Specific Glass

> /glasses/*glass_id*/

#### Searching

> /glasses/search/*search query*/

### Connections
#### [Drinks By Glass](/drinks-api/docs/v2/drinks)

> /drinks/servedin/*glass_id*/

#### [Images](/drinks-api/docs/v2/assets#images)

> http://assets.absolutdrinks.com/glasses/*glass_id*.*format*

## JavaScript Client Library
#### Listing Glasses

``` js
addb.glasses().loadSet(function(query) { });
addb.glasses('es').skip(5).take(10).loadSet(function(query) { });
```

#### Loading Specific Glass

``` js
addb.glasses().load('cocktail-glass', function(glass) { });
```

#### Auto Suggest (on name)

``` js
addb.glasses().quickSearch('some query', function(query) { });
```

## .NET Client Library
#### Listing Glasses

``` csharp
var glasses = ADDbClient.Glasses();
var nextGlasses = ADDbClient.Glasses().Skip(5).Take(10);
```

#### Loading Specific Glass(es)

``` csharp
var glass = ADDbClient.Glasses().Load("cocktail-glass");
var glasses = ADDbClient.Glasses("de").Load(new [] { "cocktail-glass", "wine-glass" });
```

#### Auto Suggest (on name)

``` csharp
var glasses = ADDbClient.Glasses().QuickSearch("some query");
```