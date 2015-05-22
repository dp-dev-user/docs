Action
======
An *Action* represents something you do in the process of making a [Drink][], 
for an example **Blending**.

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
            <td>the identifier of the object</td>
            <td>string</td>
        </tr>
        <tr>
            <td>name</td>
            <td>the name of the object</td>
            <td>string</td>
        </tr>
        <tr>
            <td>languageBranch</td>
            <td>the language of the texts in the object</td>
            <td>string</td>
        </tr>
        <tr>
            <td>description</td>
            <td>a general text that describes the object</td>
            <td>string</td>
        </tr>
        <tr>
            <td>tool</td>
            <td>a referens to the tool that is used</td>
            <td><a href="./general/entity-reference">entity reference</a> to <a href="./tools">tool</a></td>
        </tr>
        <tr>
            <td>videos</td>
            <td>any videos of this action</td>
            <td>array of <a href="/drinks-api/docs/v1/general/video-reference">video reference</a>s</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
#### Listing Actions

> /actions/

#### Showing specific Action(s)

> /actions/*action_id*/

> /actions/*action_id1*,*action_id2*,*action_id3*/

#### Auto Suggest Search (on name)

> /quickSearch/actions/*search_query*/

### Connections
#### [Drinks By Action](/drinks-api/docs/v1/drinks)

> /drinks/doing/*action_id*/

#### [Images](/drinks-api/docs/v1/assets#images)

> /actions/*action_id*.*format*

## JavaScript Client Library
#### Listing Actions

``` js
addb.actions().loadSet(function(query) { });
addb.actions('es').skip(10).take(25).loadSet(function(query) { });
```

#### Loading Specific Action

``` js
addb.actions().load('shake', function(shake) { });
```

#### Auto Suggest Search (on name)

``` js
addb.actions().quickSearch('some query', function(query) { });
```

## .NET Client Library
#### Listing Actions

```csharp
var actions = ADDbClient.Actions().Skip(5).Take(20);
```

#### Loading Specific Action

```csharp
var action = ADDbClient.Actions().Load("shake");
var actions = ADDbClient.Actions("es").Load(new [] { "shake", "strain" });
```

#### Auto Suggest (on name)

```csharp
var actions = ADDbClient.Actions().QuickSearch("some query");
```

[Drink]: /drinks-api/docs/v1/drink