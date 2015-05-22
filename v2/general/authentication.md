Authentication
==============
We currently 

##HTTP(S) GET Authentication
To authenticate with a regular HTTP(S) GET you need to provide your APiKey, either as a regular parameter or 
a header.

For an example

> http://addb.absolutdrinks.com/en/drinks?apiKey=bef8ba384df943bd9238e599becba9ff

##JSONP Authentication
To authenticate with JSONP (used for JavaScript implementations) you need to provide the ID of your App.

For an example
> http://addb.absolutdrinks.com/en/drinks?appId=125

We will then validate that the call is made from the URL that was specified for your application

*Under development just edit your host file to point at localhost*