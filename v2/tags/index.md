(DEPRECATED) ﻿Tag
=========
Tags are the way to construct groups of [Drinks][] for any drinks that you find related to each other and that you have a use for in your app. Tags are applied to Drinks and each app manage their own tags. 

Example of use: All drinks on the articles of absolutdrinks.com are chosen and tagged together by the Absolut team. 

Look here for example: &lt;http://www.absolutdrinks.com/en/inspiration/know-one-collins-and-you-know-them-all/&gt;

## Resource Properties
Name|Description|Returns
--- | --- | ---
name|the name of the tag|string
owner|the app that created this tag|string
count|how many drinks it's applied to|number

## Managing tags
To create a tag as an app owner you need to log into the [App Admin][].

## HTTP(s) GET Operations
### List tags

&gt; /tags/

## Connections
#### [Drinks By Tag][Drinks]

&gt; /drinks/tagged/*tag_name*/

[Drinks]: /drinks-api/docs/v2/drinks
[App Admin]: /app/login