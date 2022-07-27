---
published: true
---
## How to Use Javascript to Use API Data

Today we will work through how to pull API Data into Javascript. In this example, I use the [public API from ImgFlip](https://api.imgflip.com/get_memes) which provides images for memes. 

### Fetching API Data

First, we use the fetch function with an argument identifying the path to the resource, our API. Next, we need to work with the response which is a stream of data that returns a promise. We can do these two steps simply by using `async` and `await`. Because `fetch` is an asynchronous, we need add `await` to wait on the fetch result to store it in our variable which I will call `data`. 

```
async function getMEME() {
        const response = await fetch(`https://api.imgflip.com/get_memes`);
        }
        
```

Complete data and grab the data in the body of the response. We need to read that data and store it in a format that we can work with (text, image data coming as a blob, array, JSON or Javascript Object Notation). 
Make an img as a url into the DOM Element with that data.

```
test code
```

![]({{site.baseurl}}/https://i.imgflip.com/19ijp6.jpg)
