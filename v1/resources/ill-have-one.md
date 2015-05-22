I'll Have One
=============

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
            <td>the id of the I'll Have One</td>
            <td>number</td>
        </tr>
        <tr>
            <td>latitude</td>
            <td>the latitude of this I'll Have One was made from (if any)</td>
            <td>number</td>
        </tr>
        <tr>
            <td>longitude</td>
            <td>the latitude of this I'll Have One was made from (if any)</td>
            <td>number</td>
        </tr>
        <tr>
            <td>city</td>
            <td>the city this I'll Have One was made from</td>
            <td>string</td>
        </tr>
		<tr>
            <td>countryCode</td>
            <td>the country code this I'll Have One was made from</td>
            <td>string</td>
        </tr>
		<tr>
            <td>region</td>
            <td>the region this I'll Have One was made from</td>
            <td>string</td>
        </tr>
        <tr>
            <td>country</td>
            <td>the country this I'll Have One was made from</td>
            <td>string</td>
        </tr>
        <tr>
            <td>facebookId</td>
            <td>the facebook id of the person that made this I'll Have One*</td>
            <td>number</td>
        </tr>
        <tr>
            <td>timeStamp</td>
            <td>the date/time this I'll Have One was made</td>
            <td>json date</td>
        </tr>
        <tr>
            <td>drink</td>
            <td>the drink that was ordered</td>
            <td><a href="/drinks-api/docs/v1/general/entity-reference">entity reference</a> to <a href="/drinks-api/docs/v1/drinks">drink</a></td>
        </tr>
        <tr>
            <td>app</td>
            <td>the app that was used when the drink was ordered</td>
            <td>string</td>
        </tr>
		<tr>
            <td>version</td>
            <td>**the version??**</td>
            <td>string</td>
        </tr>
        <tr>
            <td>facebookAuthToken</td>
            <td>the facebook authentication token of the person that made this I'll Have One</td>
            <td>string</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
#### Listing I'll Have Ones

> /illhaveones/

#### Listing New I'll Have Ones
*Usable for polling, will only return newer than id provided*

> /illhaveones/?fromId=800000

## Filtering Queries
### By Location
#### By Country

> /illhaveones/incountry/*country*/

#### By City

> /illhaveones/incity/*city*/

#### By Latitude/Longitude (1000m)

> /illhaveones/near/*lat*,*lng*/

#### By Latitude/Longitude (Custom Radius)

> /illhaveones/near/*lat*,*lng*,*radius*/

### By Drink

> /illhaveones/fordrink/*drink_ids*/

### By Application Submitted

> /illhaveones/byedition/*edition_id*/

## JavaScript Client Library
#### Listing I'll Have Ones
*skip-parameter isn't allowed for ill have ones*

``` js
addb.illHaveOnes().loadSet(function(query) { });
addb.illHaveOnes().take(10).loadSet(function(query) { });
```

#### Listing new I'll Have Ones
*Usable for polling, will only return newer than id provided*

``` js
addb.illHaveOnes().fromId(800000).loadSet(function(query) { });
```


## .Net Client Library
#### Listing I'll Have Ones
``` csharp
var illhaveones = ADDbClient.IllHaveOnes();
```

#### Listing I'll Have Ones by country
``` csharp
var illhaveones = ADDbClient.IllHaveOnes().InCountry("Mexico");
```

#### Listing I'll Have Ones by city
``` csharp
var illhaveones = ADDbClient.IllHaveOnes().InCity("Tartu");
```

#### Listing I'll Have Ones by co-ordinates
``` csharp
var illhaveones = ADDbClient.IllHaveOnes().Near(58.359474182128906, 26.68110466003418, 90000);
```



