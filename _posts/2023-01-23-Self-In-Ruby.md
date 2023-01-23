---
published: true
---
## An Intro to Self in Ruby

Self can be very difficult to understand as a beginner using Ruby because it changes based on the context and it is not always explicitly shown in the code. A few high level things to note: 

SELFS

Truths can be used to specifically reference properties and methods of a class or object (instance). You can use it to solve class-level problems.

Falsies 

- class methods and variables can reference individual objects. This is FALSE
- Self does not change based on context. This is False - THEY DO!
- Self is never implicitly called by ruby - This is FALSE

Before I dive into explaining self, let me back up and explain class methods and variables. 

### What are class methods and variables?
Class methods and variables reference the entire class. A class is basically a template for all objects or instances of that class. This is otherwise known as what attributes do the class have (ie what does a child look like?) and what methods can I call on it to be able to manipulate it to a specific instance. 

TIP: It is important to note that you have to call a class method on a class. If you call a class method on an install of the class, it will throw an error (NoMethodError). When you get this error, look at what you are calling it on. This will only occur when you are calling a class method on an instance or an instance method on a class.

An example of this error:

```
country = Country.new("Ecuador")
c country.self

NoMethodError: undefined method `self' for #<Country:0x001g1542658753 @name="Ecuador" @continent="South America"">
```




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
        
```
When you call this in pry, you will see a particular instance of the Country class. Country.new_from_hash is a class method that goes into your country.rb file and self.new creates a new instance and initailizes on that new instance. When you initialize the name, ecuador, it returns self. The output should look something like:

```
#<Country:0x001g1542658753 @name="Ecuador" @continent="South America">
```

Class variables are created using @@. You might have a bunch of countries that you want to store in a collector file using something like @@all = []. You can access the latest country you are currently initailizing using self. 

So, if you want to create a class method so you can use Country.all to get all the countries and use self to tell it that it is a class method. 

```
def self.all
    @@all
end
```
You are relying on the implicit return to force evaluation of the @@all which is the last line or Ruby and allows you to rely on that implicit return feature.

### Classes, Instances and Methods

The class is a blueprint for the actions and properties of a given instance. An instance is a unique object created from the class blueprint. A method, on the other hand, is a behavior.

Hopefully this was helpful in driving home the idea of self, class, and methods in Ruby! Remember, self in Ruby allows you to access the current object. When you call a method without explicitly receiving an object, the method is implicitly called on self. 

If you have more examples of when you might use self, feel free to leave a comment.


<img src="https://media.tenor.com/0ZfvvMFHDasAAAAC/beyourself-be.gif" width="300">
