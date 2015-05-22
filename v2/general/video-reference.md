Video
================
An object used to describe where a video can be found.

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
            <td>video</td>
            <td>the identiyfier of the video. either a youtube id or a filename on the assets server</td>
            <td>string</td>
        </tr>
        <tr>
            <td>type</td>
            <td>where the video can be found, either "youtube" or "assets"</td>
            <td>string</td>
        </tr>
    </tbody>
</table>

####Example
An array of videos looking like this

	"videos": [
		{
			"video": "V9sgZX9V6wE",
			"type": "youtube"
		},
		{
			"video": "old-fashioned.mp4",
			"type": "assets"
		}
	]

refers to videos that can be found at

> http://www.youtube.com/watch?v=V9sgZX9V6wE

> http://assets.absolutdrinks.com/videos/old-fashioned.mp4