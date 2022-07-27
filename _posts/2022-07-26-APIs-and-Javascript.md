---
published: true
---
## How to Use Javascript to Use API Data

Today we will work through how to pull API Data into Javascript. In this example, I use the [public API from ImgFlip](https://api.imgflip.com/get_memes) which provides images for memes. 

### Fetching API Data

First, we use the fetch function with an argument identifying the path to the resource, our API. Next, we need to work with the response which is a stream of data that returns a promise. We can do these two steps simply by using `async` and `await`. Because `fetch` is an asynchronous, we need add `await` to wait on the fetch result to store it in our variable which I will call `response`. 

```
async function getMEME() {
        const response = await fetch(`https://api.imgflip.com/get_memes`);
        }
        
```

Complete data and grab the data in the body of the response. We need to read that data and store it in a format that we can work with (text, image data coming as a blob, array, JSON or Javascript Object Notation). Finally, you will need to call that function to display the API array of data.  


```
async function getMEME() {
        const response = await fetch(`https://api.imgflip.com/get_memes`);
        const data = await response.json();
        }
getMEME()
```
<img src="https://i.imgflip.com/19ijp6.jpg" width="100">

You'll notice in the array from the ImgFlip API has a drill-down of data -> memes -> an array of objects. Within each object, we have the `object keys`: id, name, url, width, and height. 
![Meme Array from API]({{site.baseurl}}/_posts/Meme Array Snip.PNG)

### Connecting URL Data to HTML

We are interested in using the url and displaying an image in the DOM Element with that data. To do this, we need to connect our html to the javascript.

```
HTML:
<img src="" id="image" width="300px">

Javascript:
var i = 0;
memeCurrent = data.data.memes[i]
image.src = memeCurrent.url
```




