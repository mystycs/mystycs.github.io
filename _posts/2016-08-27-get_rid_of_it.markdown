---
layout: post
title:  "Get Rid Of It"
date:   2016-08-27 05:01:46 +0000
---


This was my first sinatra project assessment, and I really enjoyed working on it. The concept was to create a classified listings website where users can sell goods they are looking to get rid of, hence the name Get Red Of It.

Users can sign up, login, post, edit, and delete their listings. This is using the standard concept of CRUD. Also known as create, read, update and delete.

![](http://i.imgur.com/6tH3zHr.png)

I decided to go with a bootstrap design, as it allows for simplistic readability and cross platform use. The app makes use of ActiveRecord. I implemented 3 controllers, 2 models and several migrations. User validation, and content validation is also implemented to ensure that bad data isn't created.

![](http://i.imgur.com/2OG3WH3.png)

The biggest hurdle was to make sure that we handled certain validations so that other users could not edit, or delete listings that were not assigned to their user_id. Some validation had to be implemented to make sure that the user with a current session was equal to that of the user whom had posted the listing.

![](http://i.imgur.com/WBv1LJK.png)

As seen above, we compare the current_user id to the user.id of the listing; if that returns as false, we output an error the user that he can not edit another listing. Bootstrap has some fancy css for error display which we used.

Overall the concept yet simple, required some time and effort to make it perfect. We want to make sure that we handle all possible scenarios and inputs.

So if you are ever looking to list something for sale, why not Get Rid Of It?
