
![X](https://raw.githubusercontent.com/gabbersdev/x-scrapper/main/xlogo.png)

**X** is a multi-scrapper of the platforms:
- Twitter / X
- TikTok

### Installing
```bash
npm install x-scrapper
```
###  Example

 Twitter: 
 ```js
const twitter = require("x-scrapper").Twitter
	
twitter.getVideoInfo("https://twitter.com/memesbreakcore/status/1684331516825042944") // returns a Promise
.then((res) => {
	console.log(res) // Video info.
	console.log(res.media.formats[0].url) // Get the video .mp4 url (you can download it.)
})
```
Tiktok:
```js
const tiktok = require("x-scrapper").Tiktok

tiktok.getVideoInfo("https://www.tiktok.com/@oldtimehawkey/video/7259942195296210218") // returns a Promise
.then((res) => {
	console.log(res) // Video info.
	res.downloadVideo() // Return the tiktok video without watermark as a buffer. (You can't get the direct .mp4 url, you need to download it.)
	.then((buffer) => {
		console.log(buffer)
	})
})
```
