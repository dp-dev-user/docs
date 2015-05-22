Response Formats
==============
The APi currently supports the following formats

- [JSON][]
- [JSONP][]

For JSONP just supply a "callback" parameter in each request

## Example Response
The following JSON object is an example of how the response would look when requesting 
**http://addb.absolutdrinks.com/drinks/absolut-cosmopolitan/** with a valid APiKey (excluded from example)

``` json
{
	"description": "[Fill|Action|fill] a [shaker|Tool|boston-shaker] with [ice cubes|Ingredient|ice-cubes]. [Add|Action|add] all ingredients. [Shake|Action|shake] and [strain|Action|strain] into a chilled [cocktail glass|Glass|cocktail-glass]. [Garnish|Action|garnish] with orange.",
	"story": "A pink drink served in a Martini glass and called The Cosmopolitan is said to have originated in San Francisco in the 1980s, but it wasn't\r\nuntil 1988--the year Absolut Citron was launched--that the\r\nCosmopolitan as it is known today was created. Bartender Toby Cecchini\r\nadapted the original recipe, using fresh juice, orange liqueur, a\r\nsplash of cranberry, and the first citrus-flavored vodka. The rest is history!",
	"color": "Pink",
	"rating": 87,
	"skill": {
		"id": "beginner",
		"name": "Beginner",
		"value": 1
	},
	"videos": [
		{
			"video": "absolut-cosmopolitan.mp4",
			"type": "assets"
		},
		{
			"video": "pggWEFyT1Ds",
			"type": "youtube"
		}
	],
	"isAlcoholic": true,
	"isCarbonated": false,
	"isHot": false,
	"tags": [
		{
			"Owner": "apps/225",
			"Name": "Coll_Citron"
		},
		{
			"Owner": "apps/225",
			"Name": "Coll_Classic1"
		},
		{
			"Owner": "apps/225",
			"Name": "Coll_Vodka"
		},
		{
			"Owner": "apps/225",
			"Name": "drinkspiration"
		}
	],
	"servedIn": {
		"id": "cocktail-glass",
		"text": "Cocktail Glass"
	},
	"ingredients": [
		{
			"type": "ice",
			"id": "ice-cubes",
			"text": "[Ice Cubes]",
			"textPlain": "Ice Cubes"
		},
		{
			"type": "vodka",
			"id": "absolut-citron",
			"text": "2 Parts [ABSOLUT CITRON]",
			"textPlain": "2 Parts Absolut Citron"
		},
		{
			"type": "spirits-other",
			"id": "orange-liqueur",
			"text": "½ Part [Orange Liqueur]",
			"textPlain": "1 Part Orange Liqueur"
		},
		{
			"type": "mixers",
			"id": "cranberry-juice",
			"text": "½ Part [Cranberry Juice]",
			"textPlain": "½ Part Cranberry Juice"
		},
		{
			"type": "mixers",
			"id": "lime-juice",
			"text": "¼ Part [Lime Juice]",
			"textPlain": "1 Part Lime Juice"
		},
		{
			"type": "fruits",
			"id": "orange",
			"text": "1 Twist [Orange]",
			"textPlain": "1 Twist Orange"
		}
	],
	"tastes": [
		{
			"id": "sweet",
			"text": "Sweet"
		},
		{
			"id": "fresh",
			"text": "Fresh"
		},
		{
			"id": "fruity",
			"text": "Fruity"
		}
	],
	"occasions": [
		{
			"id": "afternoon",
			"text": "Afternoon Drinks"
		},
		{
			"id": "evening",
			"text": "Evening Drinks"
		},
		{
			"id": "pre-dinner",
			"text": "Pre-Dinner Drinks"
		}
	],
	"tools": [
	{
		"id": "citrus-press",
		"text": "Citrus press"
	},
	{
		"id": "freezer",
		"text": "Freezer"
	},
	{
		"id": "jigger",
		"text": "Jigger"
	},
	{
		"id": "strainer",
		"text": "Strainer"
	},
	{
		"id": "twist-knife",
		"text": "Twist Knife"
	},
	{
		"id": "boston-shaker",
		"text": "Boston Shaker"
	}
	],
	"drinkTypes": [],
	"actions": [
		{
			"id": "shake",
			"text": "Shake"
		},
		{
			"id": "strain",
			"text": "Strain"
		}
	],
	"brands": [ "absolut" ],
	"languageBranch": "en",
	"id": "absolut-cosmopolitan",
	"name": "ABSOLUT Cosmopolitan",
	"descriptionPlain": "Fill a shaker with ice cubes. Add all ingredients. Shake and strain into a chilled cocktail glass. Garnish with orange."
}
```

A pipe (**|**) separated list enclosed by square brackets (**[ ]**) indicates a string that can be
parsed in order to produce a link to that resource. For example **[shaker|Tool|boston-shaker]**

* The first part [**shaker**|Tool|boston-shaker] contains the translated word to be displayed as part
of the text.
* The second part [shaker|**Tool**|boston-shaker] contains the type of the item. Add an **s** to the 
end of the word and you have the first part of the url to link to: http://addb.absolutdrinks.com/Tool**s**/
* The third part [shaker|Tool|**boston-shaker**] contains the ID of the item. Append the ID to the above
URL to produce the entire URL (**NOTE**: This example does not contain the API-key): http://addb.absolutdrinks.com/Tools/**boston-shaker**/



## Errors
If an error occurs, when for an example an non existing resource is requested, ADDb will respond with an error. The error, as every
other responses in ADDb, is a JSON-object.

``` json
{
    "error": "Description of the error"
}
```

Next, read how [Internationalization][i18n] works in ADDb

[JSON]: http://en.wikipedia.org/wiki/Json
[JSONP]: http://en.wikipedia.org/wiki/JSONP
[i18n]: /drinks-api/docs/v1/getting-started/i18n


