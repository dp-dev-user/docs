ADDb-CSHARP - ADDB for .NET
===============================

## Installing
#### Downloading Binary Files
The binary files can be downloaded from the assets server at

> http://assets.absolutdrinks.com/api/addb-csharp.1.2.1.0.zip

## Configuration
The first thing you need to do is configuring your settings before using the library. 
The code can be placed anywhere need to run before you start querying. `Application_Start` in your Global.asax is 
recommended for web applications.
    
``` csharp
    using Absolut.ADDb.Client;

    public void Application_Start() 
    {
        ADDbClient.Configuration = new ADDbConfiguration 
        {
            ApiKey = "your_api_key",
            ApiSecret = "your_api_secret"
        };
    }
```

## Conventions
ADDb-Csharp allows usage of a fluent code style to easily make queries against the ADDb. It's also meant 
to reseamble to LinQ. The real query against ADDb gets executed when the result is enumerated, just like in 
regular LinQ.

### Quick Example
Here we query the ADDb for "The first 30 Drinks that contains 'lemon-juice' or 'orange-juice' that should be 
served in a 'cocktail-glass'"

``` csharp
    var drinks = ADDbClient.Drinks()
        .With("lemon-juice").Or("orange-juice")
        .ServedIn("cocktail-glass")
        .Take(30)
        .ToList();
```

## Using addb-csharp
For more information on how to use addb-csharp to query for resources, check each individual resource for code examples.

[Nuget]: http://nuget.org