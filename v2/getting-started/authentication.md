Authentication
=================
All queries against the ADDb must be authenticated with an App. To get an app send an request to <interactive@absolut.com>

## Server to ADDb
To authenticate a request server to ADDb you need to provide your app's api key as 
a parameter in the request.

Example.

> /drinks/?apiKey=bef8ba384df943bd9238e599becba9ff

## Client to ADDb (JavaScript)
To authenticate a request directly from a client your app's id needs to be provided
as a parameter in the request.

Example.

> /?appId=125&callback=myCallback

The referer of the request will then be matched with the host registered with your app.

*While developing modify your "hosts"-file*

Having finished reading the **Getting Started** section you can now continue reading about the different resources available in ADDb by clicking on it in the menu to the left.