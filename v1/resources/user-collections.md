User Collection
===============

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
            <td>the id of the list</td>
            <td>string</td>
        </tr>
        <tr>
            <td>name</td>
            <td>the name of the list</td>
            <td>string</td>
        </tr>
        <tr>
            <td>facebookUserId</td>
            <td>the facebook id of the user who created this list</td>
            <td>number</td>
        </tr>
        <tr>
            <td>drinks</td>
            <td>the drinks in this list</td>
            <td>array of <a href="/drinks-api/docs/v1/general/entity-reference">entity reference</a> to <a href="/drinks-api/docs/v1/drinks">drinks</a></td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations
#### Listing User Collections
**NOTE**: You are only allowed to list your own lists. Therefore a facebook User Access Token must be provided.
*See [Facebook's Developer](https://developers.facebook.com/) site in order to find out how to get one.*

> /usercollections/?authtoken=*access_token*

#### Showing specific user collection

> /usercollections/*user_collection_id*/

#### Showing a user collections flip side
*What other drinks can be made with the ingredients from the drinks in this list*

> /usercollections/*user_collection_id*/flipside/


## JavaScript Client Library
**NOTE**:A facebook User Authentication Token must be provided.

#### Creating User Collections

``` js
addb.usercollections.create(name, callback,"whiskey-sour", "expresso-martini"); 
```

#### Updating User Collections

``` js
addb.usercollections.update(id, name, callback, "whiskey-sour", "expresso-martini"); 
```

#### Deleting User Collections 

``` js
addb.usercollections.deleteUserCollection(id, callback);
```

#### By User Collections flipside

``` js
addb.usercollections.flipside(id, callback);
```


## .Net Client Library
**NOTE**:A facebook User Authentication Token must be provided.

#### Creating User Collections  

``` csharp
var userCollections = ADDbClient.UserCollections().Create(facebookAuthToken, listName, "whiskey-sour", "expresso-martini");
```

#### Updating User Collections  

``` csharp
var userCollections = ADDbClient.UserCollections().Update(facebookAuthToken, listId, name, "whiskey-sour", "expresso-martini");
```

#### Deleting User Collections  

``` csharp
var userCollections = ADDbClient.UserCollections().Delete(facebookAuthToken, listId);
```

#### By facebook user

``` csharp
var userCollections = ADDbClient.UserCollections().ForFacebookUser(facebookAuthToken);
```
