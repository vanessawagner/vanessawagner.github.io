---
published: true
---
## An Intro to Self in Ruby

Self can have very abstract uses so I am going to dive into the basic implementations before we go into the more obscure uses. 

### What is Self?

Self is always changing but is not always explicitly shown in the code. 


```
async function getMEME() {
        const response = await fetch(`https://api.imgflip.com/get_memes`);
        }
        
```

Complete data and grab the data in the body of the response. We need to read that data and store it in a format that we can work with (this can be in the form of text, image data, array, JSON or Javascript Object Notation). Finally, you will need to call that function to display the API array of data.  


```
async function getMEME() {
        const response = await fetch(`https://api.imgflip.com/get_memes`);
        const memedata = await response.json();
        }
getMEME()
```
<img src="https://i.imgflip.com/19ijp6.jpg" width="300">


### Check out the full code here:
https://github.com/vanessawagner/phase-1-final-project
