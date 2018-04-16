(DEPRECATED) I'll Have One
=============

### Resource Properties
Name|Description|Returns
--- | --- | ---
id|the id of the I'll Have One|number
latitude|the latitude of this I'll Have One was made from (if any)|number
longitude|the latitude of this I'll Have One was made from (if any)|number
city|the city this I'll Have One was made from|string
countryCode|the country code this I'll Have One was made from|string
region|the region this I'll Have One was made from|string
country|the country this I'll Have One was made from|string
facebookId|the facebook id of the person that made this I'll Have One*|number
timeStamp|the date/time this I'll Have One was made|json date
drink|the drink that was ordered|entity reference to drink
app|the app that was used when the drink was ordered|string
version|the version??|string
facebookAuthToken|the facebook authentication token of the person that made this I'll Have One|string

## HTTP(s) GET Operations
#### Listing I'll Have Ones

&gt; /illhaveones/

#### Listing New I'll Have Ones
*Usable for polling, will only return newer than id provided*

&gt; /illhaveones/?fromId=800000

## Filtering Queries
### By Location
#### By Country

&gt; /illhaveones/incountry/*country*/

#### By City

&gt; /illhaveones/incity/*city*/

#### By Latitude/Longitude (1000m)

&gt; /illhaveones/near/*lat*,*lng*/

#### By Latitude/Longitude (Custom Radius)

&gt; /illhaveones/near/*lat*,*lng*,*radius*/

### By Drink

&gt; /illhaveones/fordrink/*drink_ids*/

### By Application Submitted

&gt; /illhaveones/byedition/*edition_id*/

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
