---
layout: post
title:  "Project Manager - My first full Ruby on Rails application"
date:   2016-09-06 06:56:27 +0000
---


For my Ruby on Rails application I decided to create a project manager. This rails app allows users to post projects under categories and create tasks and post comments.

![](http://i.imgur.com/BUVjp2x.jpg)

The front end framework I decided to use was Bootstrap. Bootstrap allows us to be flexible and is one of the most widely used today. It allowed me to quickly deploy something that looked clean and sleek without hassle. 

I decided to use devise for the authentication system and paired it with Facebook omniauth. This allows Facebook users to create accounts and login without the hassle of filling in the blanks themselves. Isn’t that just great? Sure is!

![](http://i.imgur.com/vLCUlEw.png)

As seen above we don’t take much from Facebook, just an email and name to get the user setup. The rest of that data is just behind the scenes that gets the ball rolling. 

Once the logged in the user can create categories, and then projects. Within the projects the user has abilities to create tasks and leave a comment if a discussion is necessary. 

![](http://i.imgur.com/SAwqhLN.jpg)

All validations are handled in the models and we make sure to prevent any duplicate projects from being created. 

![](http://i.imgur.com/t0P6IkG.jpg)

A simple project manager that is not cluttered can go a long way. Simply submit a project associated with the category of your choosing or create one. Post tasks, mark them completed and have a discussion if needed. That is what project manager allows us to do. Ruby on Rails gives us the foundation of tools needed to make this happen in the simplest of ways.



