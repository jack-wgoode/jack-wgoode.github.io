---
layout: post
title:      "Second Milestone Project - Sinatra"
date:       2020-09-22 09:01:13 -0400
permalink:  second_milestone_project_-_sinatra
---


We are all familiar with Ruby on Rails. Just where does Sinatra fit in? No, I am not talking about the iconic crooner
who made "My Way" a classic but that theme will apply. My project was a simple "PawPost" application  which simulated an Owner signing up their dogs for doggie daycare. In a nutshell, I needed a CRUD application with ]authetication. The models were Owner and Dog. The resource was dogs. By using ActiveRecord associations of has_many and belongs_to, I was able to tap into the methods to limit owners to their own dogs.

## Why Sinatra? 
Yes, Ruby on Rails is the powerful "Swiss Army Knife" and it is great for spinning up a web application with concise commands like 

```
$ rails new my_app --database=postgresql
```

In fact, without seeing what is going on under the hood, Rails can seem lot a bit of magic. One of the things I truly appreciate about the curriculum at Flatiron is that it does not allow you to jump into frameworks without progressively learning the layers beneath it. My Sinatra project allowed me to get hands on with a microframework that has been used by companies like Linkedin, BBC, and GitHub.

Sinatra provides a very lightweight framework with an intuitive DSL to quickly build web apps. Creating a get route would be as simple as this code in the controler: 

```
get "/dogs" do
    redirect_if_not_logged_in
    @dogs = current_owner.dogs
    erb  :"/dogs/index.html"
  end
```

This renders an Embedded Ruby(ERB) file in html. That view has access to the @dogs instance variable and can iterate through all the dogs that belong to the currently signed in owner. This code lives in the dogs_controller.rb and 
allows us to separate concerns with the Dog model, dogs_controller, and the associated views that follow REST. 

By having more control over what is included, Sinatra allows a developer to have just the right tool for the job instead of 
far more than is needed. Think tack hammer vs. sledge. Sinatra is built on Rack as a webserver, and in my case I used ActiveRecord with a SQLite development db. When errors arose as they often do in our world, I could know where to go quickly in the MVC to resolve them. IN a "Goldilocks" balance, I could still take advantage of the Corneal gem to generate models or scaffold selectively. Just enough but not too much.

One of the key requirements for my project was that the user only had access to create, edit, or delete their own records. I was able to use redirects in the controller, conditional logic against the session[:id], and ActiveRecord associations to accomplish this without much fuss. Sinatra's simpler structure made it clearer to see what was going on and debug issues.

This was an excellent learning process and I will definitely keep Sinatra in my toolbox.

https://github.com/jack-wgoode/paw_post.git

https://www.linkedin.com/in/jack-w-goode-10816812/






