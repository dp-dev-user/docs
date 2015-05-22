Entity Reference
================
A entity reference is used to refer from one resource to another resource in the ADDb.

###Entity Reference Properties
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
            <td>the id of the entity that is refered</td>
            <td>string</td>
        </tr>
        <tr>
            <td>text</td>
            <td>a text that can be used when creating links to the item</td>
            <td>string</td>
        </tr>
    </tbody>
</table>

####Example
An entity reference to an [action](/drinks-api/docs/v2/actions) looking like this

    {
      id: 'muddle',
      text: 'Muddle'
    }

refers to the action that can be found at

> http://addb.absolutdrinks.com/actions/muddle