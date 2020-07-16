---
layout: post
title:      "Welcome to class"
date:       2020-07-16 23:56:18 +0000
permalink:  welcome_to_class
---

You mave have heard that "everything in Ruby is an object." but exactly what does that mean? For my purposes, we will not take a journey into the deep inner workings of Ruby or any other programming languages.What we will do is help you gain a clearer understanding of what classes and objects represent in object oriented programming. 

Take a moment to think about how you interact with the things around you in real life. If you are reading this, you have either a touch screen or a keyboard. You are reading this on a screen that you expect to display my words. These things have what we will call attributes. They can be described with things like size and color. You expect them to behave in certain ways. You understand what will happen when you move the cursor or press the backspace button. I will take a chance here but I am guessing that you do not know exactly what happens in your PC or MAC to cause it to happen.
The more important thing is that you do not *have *to know.

Got that? If not, don't worry. Your lightbulb will come on shortly. If we want to create applications, we have a wonderful way to represent a model of what things are and how they behave. Let's start by creating a class definition. We will keep it simple.

```
def Dog

   def initialize('name')
	    @name = name
	 end
	 
	 def breed
	    @breed 
	 end
	 
	 def breed=(breed)
	    @breed = breed
	 end		
	 
	 def bark
	    puts 'Woof!'
	 end		
	 
end
```

A class definition lets us define a model for an object. In this case, a dog. With this Dog class we can create a dog object that has a name and a breed. We don't have to stop there. With a few more lines of code, we could also define attributes like size,color, or anything that would describe a dog. If we are building a model that represents a real dog, we also want to define what it can do. Almost all dogs can bark, so we have defined a method that outputs 'Woof' to the  screen.

Now we have created an object, right? Not yet. You have created a powerful factory for creating dog objects.
Each of them can have their own breed and be unique just like a real dog. If you forget their name, you can ask with
a "getter" method and your dog will tell you. If you want to make it a bassett hound, you can set its breed with a "setter" method. If you tell your dog to bark, they will say "Woof". It has attributes and it has methods. 

Being able to model the real world is what allows developers to create applications that you use everday. The player in your favorite game or your "desktop" on your PC let you interact in predictable ways. How do we create an actual object and use its attributes and methods?  In our next exciting blog post, we will dive into the power of objects. In the meantime, keep it "classy". 

Comments, Corrections, and feedback are always welcome. 



The content of your blog post goes here.
