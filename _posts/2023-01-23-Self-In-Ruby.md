---
published: true
---
## An Intro to Self in Ruby

Self can be very difficult to understand as a beginner using Ruby because it changes based on the context and it is not always explicitly shown in the code. A few high level things to note: 
SELFS
Truths can be used to specifically reference properties and methods of a class or object (instance). You can use it to solve class-level problems.
Falsies 
class methods and variables can reference individual objects. FALSE
Self does not change based on context. False - THEY DO!
Self is never implicitly called by ruby - FALSE

Before I dive into explaining self, I will explain class methods and variables. 

### What are class methods and variables?
Class methods and variables reference the entire class. A class is basically a template for all objects or instances of that class. This is otherwise known as what attributes do the class have (ie what does a child look like?) and what methods can I call on it to be able to manipulate it to a specific instance. 

TIP: It is important to note that you have to call a class method on a class. If you call a class method on an install of the class, it will throw an error (NoMethodError). When you get this error, look at what you are calling it on. This will only occur when you are calling a class method on an instance or an instance method on a class. 


### What is Self and how do you know what the context is?
Self is referring to the object of the context. If you are inside of an method, self is what it is called on. So, if it is an instance method, it was called on an instance. 

CHECK: Check what was this method called on? 

TIP: If the first line of the method starts with def… if it is self.(dot) it must be a class method. So if you are there, self is a class. If it does not have a self dot in front of the def it is an instance method, self must be an instance.

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
