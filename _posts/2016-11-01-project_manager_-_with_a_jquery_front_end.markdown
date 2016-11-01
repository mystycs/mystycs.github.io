---
layout: post
title:  "Project Manager - With a jQuery Front End"
date:   2016-11-01 18:28:33 -0400
---


Working off my last project, I added a jQuery front end. This rails app allows users to post projects under categories and create tasks and post comments.

The biggest change to the project manager was creating a JSON backend and using AJAX to render the data. Not only did we use an AJAX GET request to render the data but we also used AJAX POST requests to add data to our backend. 

![](http://i.imgur.com/AegBNhT.png)

For the comments section I used JavaScript  model objects with methods on their prototype to get the JSON data into JavaScript  before displaying the item by appending them to the DOM.


![](http://i.imgur.com/6001i8N.jpg)


Overall it was not difficult to implement a jQuery front end using AJAX to render the data, and definitely has its advantages.
