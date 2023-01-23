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

An example of class method:
```
class Country
    def self.class_method
        puts "This is a class method."
    end
end

Country.class_method #This prints "This is a class method."
        
```

An example of instance method:
```
require 'pry'
ecuador = Country.new_from_hash({name: "Ecuador", continent: "South America"})
binding.pry

#when you call this in pry, you will see a particular instance of the Country class. Country.new_from_hash is a class method that goes into your country.rb file and self.new creates a new instance and initailizes on that new instance. When you initialize the name, ecuador, it returns self.
        
```

### Classes, Instances and Methods

The class is a blueprint for the actions and properties of a given instance. An instance is a unique object created from the class blueprint. A method is a behavior.

Hopefully this was helpful in driving home the idea of self, class, and methods in Ruby! 


<img src="https://media.tenor.com/0ZfvvMFHDasAAAAC/beyourself-be.gif" width="300">
