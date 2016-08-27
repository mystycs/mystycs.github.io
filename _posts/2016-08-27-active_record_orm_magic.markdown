---
layout: post
title:  "Active Record ORM Magic"
date:   2016-08-27 01:05:32 -0400
---


When developing software, it should always be taken into consideration to use an ORM framework. An ORM (Object-Relational Mapping) lets you query and handle data from a database using an object-oriented language. 

There are many advantages of using an ORM. It allows us to map the table columns to the matching object attributes. Some of these include eliminating the use for repetitive code (the lazy dream), reduce development time, deliver in-built query caching, validations, associations and more. 

One ORM application Ruby developers are familiar with is Active Record. You can think of Active Record as the M in an MVC model. Active Record allows us to achieve CRUD tasks in a more efficient and simple way. Active Record is super simple to setup and use once added to the application; in fact it is already setup with a default rails install.

When using Active Record in an application the first step will be to create a migration. A migration allows us write/alter a schema over time via running commands rather than write pure SQL which can become a daunting task. In rails its as simple as running the `rails generate` command. With a migration you can also create the associated model with your migration by running `rails g model`.

Below is an example of the creation of a Model and Migration in rails.

![](http://i.imgur.com/Dub9asa.jpg)

The first file created is your migration file, the second being your Ruby class. You can also create migrations from scratch without models. Every migration is a class itself. Below is an example of the migration file, which in turn once executed running `rake:db migrate` renders our schema and the actual SQL required to run the app. Active Record can work with other database technologies as well. In development we use sqlite with Ruby.

![](http://i.imgur.com/qeCO7bb.png)

Models in Active Record allow us to create helpers to interact with the database objects. Some key features are basic validations, ability to encrypt passwords using the bcrypt gem and more. Validations let us ensure we save proper data into the database. For example we can make sure that users provide their age when creating an account by simply adding `validates :age, presence: true` to our model. 

![](http://i.imgur.com/Z4Sz0oO.png)

Accessing data is also a breeze in Active Record. If we wished to access all the people in our model, its as simple as running `people = Person.all`. We can even search for a person with the name Tony with a simple line of code `tony = Person.find_by(first_name: 'Tony')`,  which is equivalent to running the SQL query `SELECT * FROM Person WHERE (Person.first_name = 'Tony') LIMIT 1`. These simple methods will run the associated queries in SQL needed to access our data. 

Overall using an ORM gives us major benefits when it comes to accessing and manipulating our data with breeze. It removes strenuous repetition of SQL queries in code, and allows us to create advanced methods to manipulate our data. It allows us to concentrate on the model rather than the structure of an SQL database itself. Every developer should consider using an ORM framework. 
