(DEPRECATED) I'll Have One
=============

### Resource Properties
&lt;table&gt;
    &lt;thead&gt;
        &lt;tr&gt;
            &lt;th&gt;Name&lt;/th&gt;
            &lt;th&gt;Description&lt;/th&gt;
            &lt;th&gt;Returns&lt;/th&gt;
        &lt;/tr&gt;
    &lt;/thead&gt;
    &lt;tbody&gt;
        &lt;tr&gt;
            &lt;td&gt;id&lt;/td&gt;
            &lt;td&gt;the id of the I'll Have One&lt;/td&gt;
            &lt;td&gt;number&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;latitude&lt;/td&gt;
            &lt;td&gt;the latitude of this I'll Have One was made from (if any)&lt;/td&gt;
            &lt;td&gt;number&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;longitude&lt;/td&gt;
            &lt;td&gt;the latitude of this I'll Have One was made from (if any)&lt;/td&gt;
            &lt;td&gt;number&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;city&lt;/td&gt;
            &lt;td&gt;the city this I'll Have One was made from&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
		&lt;tr&gt;
            &lt;td&gt;countryCode&lt;/td&gt;
            &lt;td&gt;the country code this I'll Have One was made from&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
		&lt;tr&gt;
            &lt;td&gt;region&lt;/td&gt;
            &lt;td&gt;the region this I'll Have One was made from&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;country&lt;/td&gt;
            &lt;td&gt;the country this I'll Have One was made from&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;facebookId&lt;/td&gt;
            &lt;td&gt;the facebook id of the person that made this I'll Have One*&lt;/td&gt;
            &lt;td&gt;number&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;timeStamp&lt;/td&gt;
            &lt;td&gt;the date/time this I'll Have One was made&lt;/td&gt;
            &lt;td&gt;json date&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;drink&lt;/td&gt;
            &lt;td&gt;the drink that was ordered&lt;/td&gt;
            &lt;td&gt;&lt;a href="/drinks-api/docs/v2/general/entity-reference"&gt;entity reference&lt;/a&gt; to &lt;a href="/drinks-api/docs/v2/drinks"&gt;drink&lt;/a&gt;&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;app&lt;/td&gt;
            &lt;td&gt;the app that was used when the drink was ordered&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
		 &lt;tr&gt;
            &lt;td&gt;version&lt;/td&gt;
            &lt;td&gt;**the version??**&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
		version
        &lt;tr&gt;
            &lt;td&gt;facebookAuthToken&lt;/td&gt;
            &lt;td&gt;the facebook authentication token of the person that made this I'll Have One&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
    &lt;/tbody&gt;
&lt;/table&gt;

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
