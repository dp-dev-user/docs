Where Am I
==========
The **Where Am I** resource lets applications query for positioning information. 

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
            <td>latitude</td>
            <td>the latitude of the position</td>
            <td>number</td>
        </tr>
        <tr>
            <td>longitude</td>
            <td>the longitude of the position</td>
            <td>number</td>
        </tr>
        <tr>
            <td>city</td>
            <td>the identified city name</td>
            <td>string</td>
        </tr>
        <tr>
            <td>country</td>
            <td>the identified country name</td>
            <td>string</td>
        </tr>
        <tr>
            <td>countryCode</td>
            <td>the identified country code</td>
            <td>string</td>
        </tr>
        <tr>
            <td>region</td>
            <td>the identified region</td>
            <td>string</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
### Getting location by IP

> /whereami/

### Getting location by providing an IP

> /whereami/?ip=*ip_address*

*ADDb will try to get a position based on the IP-address of the client*

### Getting location by providing latitude and longitude

> /whereami/*location*

*Location should be provided in comma separated format ex. 59.336429,18.057808*

## .NET Client Library

``` csharp
var location = ADDbClient.WhereAmI(48.123, -75.456);
var other = ADDbClient.WhereAmI("An ip-address");
```