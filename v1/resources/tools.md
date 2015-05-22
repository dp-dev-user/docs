Tools
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
            <td>the identifier of the tool</td>
            <td>string</td>
        </tr>
        <tr>
            <td>name</td>
            <td>the name of the tool</td>
            <td>string</td>
        </tr>
        <tr>
            <td>languageBranch</td>
            <td>the language of the texts in the tool</td>
            <td>string</td>
        </tr>
        <tr>
            <td>description</td>
            <td>a general text that describes the tool</td>
            <td>string</td>
        </tr>
        <tr>
            <td>videos</td>
            <td>any videos of this action</td>
            <td>array of <a href="/drinks-api/docs/v1/general/video-reference">video reference</a>s</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
#### Listing Tools

> /tools/

#### Showing Specific Tool(s)

> /tools/*tool_id*/

> /tools/*tool_id1*,*tool_id2*/

## Connections
#### [Drinks By Tool](/drinks-api/docs/v1/drinks)

> /drinks/madewith/*tool_id*/

#### [Images](/drinks-api/docs/v1/assets#images)

> http://assets.absolutdrinks.com/tools/*tool_id.format*

## JavaScript Client Library
#### Listing Tools

``` js
addb.tools().loadSet(function(query) { });
addb.tools('es').skip(10).take(25).loadSet(function(query) { });
```

#### Loading Specific Tool

``` js
addb.tools().load('boston-shaker', function(shake) { });
```

#### Auto Suggest Search (on name)

``` js
addb.tools().quickSearch('some query', function(query) { });
```

## .NET Client Library
#### Listing Tools

``` js
var tools = ADDbClient.Tools().Skip(5).Take(20);
```

#### Loading Specific Tool(s)

``` js
var tool = ADDbClient.Tools().Load("boston-shaker");
var tools = ADDbClient.Tools("es").Load(new [] { "boston-shaker", "strainer" });
```

#### Auto Suggest (on name)

``` js
var tools = ADDbClient.Tools().QuickSearch("some query");
```