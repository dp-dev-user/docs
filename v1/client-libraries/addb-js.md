The addb.js - ADDb through JavaScript
=========================

## Including the addb.js
Start by including the addb.js by adding the following tag to your page. It can be placed either in 
your head-tag or anywhere in your body-tag.

Development Version (with comments)

``` html
<script src="http://assets.absolutdrinks.com/api/addb-0.5.2.js" type="text/javascript"></script>
```

Minified Production Version:

``` html
<script src="http://assets.absolutdrinks.com/api/addb-0.5.2.min.js" type="text/javascript"></script>
```

## Initializing
The first thing you need to do before anything else is initializing addb.js with 
**your** settings. The only mandatory setting is the **appId**.

``` js
addb.init({
    appId: 5
});
```

#### All available settings are
<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Type</th>
            <th>Default Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>appId</td>
            <td>the id of your app</td>
            <td>number</td>
            <td>undefined</td>
        </tr>
        <tr>
            <td>host</td>
            <td>the base host of all queries.</td>
            <td>string</td>
            <td>addb.absolutdrinks.com</td>
        </tr>
        <tr>
            <td>assetsHost</td>
            <td>the base host to all media assets</td>
            <td>string</td>
            <td>assets.absolutdrinks.com</td>
        </tr>
        <tr>
            <td>defaultPageSize</td>
            <td>the default page size of your queries result</td>
            <td>number</td>
            <td>25</td>
        </tr>
    </tbody>
</table>

The settings can be changed after initialization by using the following convention.

``` js
addb.configuration.defaultPageSize = 10;
```

## While Developing
ADDb uses the URL registered for your app to authorize your queries. While developing simply modify your "hosts" file.

## Using addb.js
For more information on how to use addb.js to query for resources, check each individual resource for code examples.