Updates
=========
Update is a service that can tell you which [Drinks][], [Ingredients][] etc that has changed.
## Resource Properties
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
            <td>updateId</td>
            <td>the updateId of the event.</td>
            <td>number</td>
        </tr>
        <tr>
            <td>TimeStamp</td>
            <td>When the change occurred</td>
            <td>The timestamp in UTC, on <a href="http://www.w3.org/TR/NOTE-datetime">ISO 8601</a> format</td>
        </tr>
        <tr>
            <td>Resource</td>
            <td>path to the resource.</td>
            <td>string</td>
        </tr>
        <tr>
            <td>ObjectType</td>
            <td>the type of object that changed.</td>
            <td>number</td>
        </tr>
        <tr>
            <td>objectId</td>
            <td>the id of the object changed.</td>
            <td>string</td>
        </tr>
        <tr>
            <td>typeOfChange</td>
            <td>the type of change. Either 'Updated' or 'Deleted'</td>
            <td>enum</td>
        </tr>
        <tr>
            <td>languageBranch</td>
            <td>the language the update affected.</td>
            <td>string</td>
        </tr>
    </tbody>
</table>

## HTTP(s) GET Operations

> /updates/*updateId*/

Will return up to 1000 updates, starting with updateId + 1

To get the very first update(s) do
> /updates/0/

 To get update's starting with updateId 101 do
> /updates/100/

[Drinks]: /drinks-api/docs/v2/drinks
[Ingredients]: /drinks-api/docs/v2/ingredients
