## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?
Node is a JavaScript runtime environment that can be used server or client side. 
2. What is Express? Why is Express similar to in the Ruby world?
Express is a Node.js framework that provides features for web applications. There are many frameworks 'build on top' of express. Rails is similar to express in the ruby world
3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.
```
var express = require('express');
var app = express();
app.get("/api/v1/foods", food.getFoods);
```
4. What do we use Knex for?
Knex.js helps us build Postgresql (and other database) queries in javascript
5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?
We could keep each model, view and controller separate in their organization similar to how we did in rails.
6. How do you execute raw SQL in node?
I'm not 100% sure how to without KNEX, but with it we use the
```
const database = require('knex')(configuration);  
return database.raw(`<your raw sql here>`)
```
7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
There are two places that things can go wrong, sometimes its not super easy to tell which one.

#### Review  

8. Describe DNS.
When a client sends a request to find a domain, it sends the request to a domain name server which sees if it has that domain name in its caches, if it does it sends that domain name the request, if it does not it sends the request to another domain name server.
9. What does writing clean code mean to you?
Writing clean code means writing code that does not need any refactoring.
10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?
