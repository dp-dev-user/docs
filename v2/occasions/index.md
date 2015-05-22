Occasion
========

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
            <td>the identifier of the occasion</td>
            <td>string</td>
        </tr>
        <tr>
            <td>name</td>
            <td>the name of the occasion</td>
            <td>string</td>
        </tr>
        <tr>
            <td>description</td>
            <td>the description of the occasion</td>
            <td>string</td>
        </tr>
        <tr>
            <td>languageBranch</td>
            <td>the language of the texts in the occasion</td>
            <td>string</td>
        </tr>
        <tr>
            <td>start</td>
            <td>the discrete datetime this occasion starts</td>
            <td><a href="#discrete-datetime">discrete datetime</a></td>
        </tr>
        <tr>
            <td>end</td>
            <td>the discreete datetime this occasion ends</td>
            <td><a href="#discrete-datetime">discrete datetime</a></td>
        </tr>
    </tbody>
</table>

#### Discrete Datetime
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
            <td>month</td>
            <td>the month</td>
            <td>number</td>
        </tr>
        <tr>
            <td>day</td>
            <td>the day</td>
            <td>number</td>
        </tr>
        <tr>
            <td>weekDay</td>
            <td>the weekday</td>
            <td>number</td>
        </tr>
        <tr>
            <td>hour</td>
            <td>the hour</td>
            <td>number</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET operations
#### List Occasions

> /occasions/

#### List Active Occasion
Lists the occasions that is active at the provided date/time

> /occasions/?activeat=*time*

**time** should be formatted *yyyy-MM-dd!HHmm*

#### Show specific Occasion(s)

> /occasions/*occasion_id*/

> /occasions/*occasion_id1*,*occasion_id2*/

#### Search

> /occasions/search/*search query*/

## Connections
#### [Drinks By Occasion](/drinks-api/docs/v2/drinks)
> /drinks/for/*occasion_id*/

#### [Drinks By Active Occasion](/drinks-api/docs/v2/drinks)
> /drinks/for/*time*/

**time** should be formatted *yyyy-MM-dd!HHmm*

## JavaScript Client Library
#### Listing Occasions

``` js
addb.occasions().loadSet(function(query) { });
addb.occasions('es').skip(10).take(25).loadSet(function(query) { });
```

#### Loading Specific Occasion

``` js
addb.occasions().load('shake', function(shake) { });
```

#### Auto Suggest Search (on name)

``` js
addb.occasions().quickSearch('some query', function(query) { });
```

## .NET Client Library
#### Listing Occasions

``` csharp
var occasions = ADDbClient.Occasions().Skip(5).Take(20);
```

#### Loading Specific Occasion

``` csharp
var occasion = ADDbClient.Occasions().Load("afternoon");
var occasions = ADDbClient.Occasions("es").Load(new [] { "afternoon", "evening" });
```

#### Auto Suggest (on name)

``` csharp
var occasions = ADDbClient.Occasions().QuickSearch("some query");
```
