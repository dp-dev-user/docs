(DEPRECATED) ﻿Tag
=========
Tags are the way to construct groups of [Drinks][] for any drinks that you find related to each other and that you have a use for in your app. Tags are applied to Drinks and each app manage their own tags. 

Example of use: All drinks on the articles of absolutdrinks.com are chosen and tagged together by the Absolut team. 

Look here for example: &lt;http://www.absolutdrinks.com/en/inspiration/know-one-collins-and-you-know-them-all/&gt;

## Resource Properties
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
            &lt;td&gt;name&lt;/td&gt;
            &lt;td&gt;the name of the tag&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;owner&lt;/td&gt;
            &lt;td&gt;the app that created this tag&lt;/td&gt;
            &lt;td&gt;string&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;count&lt;/td&gt;
            &lt;td&gt;how many drinks it's applied to&lt;/td&gt;
            &lt;td&gt;number&lt;/td&gt;
        &lt;/tr&gt;
    &lt;/tbody&gt;
&lt;/table&gt;

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