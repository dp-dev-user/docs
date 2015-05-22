Tag
=========
Tags are the way to construct groups of [Drinks][] for any drinks that you find related to each other and that you have a use for in your app. Tags are applied to Drinks and each app manage their own tags. 

Example of use: All drinks on the articles of absolutdrinks.com are chosen and tagged together by the Absolut team. 

Look here for example: <http://www.absolutdrinks.com/en/inspiration/know-one-collins-and-you-know-them-all/>

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
            <td>name</td>
            <td>the name of the tag</td>
            <td>string</td>
        </tr>
        <tr>
            <td>owner</td>
            <td>the app that created this tag</td>
            <td>string</td>
        </tr>
        <tr>
            <td>count</td>
            <td>how many drinks it's applied to</td>
            <td>number</td>
        </tr>
    </tbody>
</table>

## Managing tags
To create a tag as an app owner you need to log into the [App Admin][].

## HTTP(s) GET Operations
### List tags

> /tags/

## Connections
#### [Drinks By Tag][Drinks]

> /drinks/tagged/*tag_name*/

[Drinks]: /drinks-api/docs/v1/drinks
[App Admin]: /app/login