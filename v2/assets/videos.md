Videos
============
Entities with <a href="/drinks-api/docs/v2/general/video-reference">videos</a> have a property called *videos* containing an array of video objects representing the identifier of a video and the type. Depending on type these can either be found on youtube or our assets server. 

<h2 id="asset-server">Youtube</h2>
A video with type "youtube" can be found youtube: 

> http://www.youtube.com/watch?v=*video*

For an example the video "V9sgZX9V6wE" is located at:

> http://www.youtube.com/watch?v=V9sgZX9V6wE

<h2 id="asset-server">Asset Server</h2>
A video with type "assets" can be found on our assets server: 

> http://assets.absolutdrinks.com/videos/*video*

For an example the video "blend.mp4" is located at:

> http://assets.absolutdrinks.com/videos/blend.mp4

Drink tutorial videos are found in a similar way using http://assets.absolutdrinks.com/videos/drink-id.mp4. 

For example, the video for absolut cosmopolitan is found here:

> http://assets.absolutdrinks.com/videos/absolut-cosmopolitan.mp4

If you want to filter addb for drinks with videos you use the following filter:

> http://addb.absolutdrinks.com/drinks/hasvideo/


