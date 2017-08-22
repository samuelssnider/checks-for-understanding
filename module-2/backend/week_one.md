## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

1. List the five common HTTP verbs and what the purpose is of each verb.
GET- Travels to the specified page and reads and renders the data on it
PUT- Updates
PATCH
DELETE
POST
2. What is Sinatra? A domain specific language and web software used for web applications. Alternative framework for Ruby- Ruby on Rails, Merb, Nitro, and Camping.
4. What is MVC?
Model-View-Controller. A template for constructing a web application with a 'pyramid' structure.
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
Because there are norms in the industry, and using them will make your code more readable and able to be developed by other team members in the workplace.
6. What types of variables are accessible in our view templates without explicitly passing them?
Instance variables
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
```ruby
get '/horses' do
  name = "Mr. Ed"
  erb :index
end
```
9. What's the purpose of ERB?
To display html, css, and javascript that is able to incorporate ruby code lines that are used to insert bits of logic we can't or don't want to use our 'base languages' for.
10. Why do I need a development AND test database?
We need both databases so that we can test all sorts of things to make sure our database and methods are functioning together- we don't want our client to have access to any of those things.   
11. What's responsive design?
Responsive web design- the design should respond to the user's client- screen size, platform, and orientation.
12. What is CRUD and why is it important?
Create, Read, Update, Delete. Essential for being able to view, edit, add, or delete items from our database. Also convention
13. What does HTTP stand for?
HyperText Transmission Protocol
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%= %> - used to pull in a method
<%  %> - used to preform ruby within html
15. What's an ORM?
Object-Relational Mapping- a programming technique for converting data between incompatible type systems using an object-oriented programming language
16. What's the most commonly used ORM in ruby (Sinatra & Rails)?
SQL
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
Get   /restaurants     - index
Get   /restaurants/:id  - show
Get   /restaurants/new - new
Post  /restaurants     - index
Get   /restaurants/:id/edit  - edit
Put   /restaurants/:id  -index
Delete /resutants/ -index
18. What's a migration? A feature of active record that allows you to evolve your database schema over time.
A migration is a way to evolve your database Schema over time. Use a Ruby DSL to describe changes to your tables rather than raw sequel
19. When you create a migration, does it automatically modify your database?
No, you need to seed it to alter your database.
20. How does a model relate to a database?
A model is what directly interacts with a database- turns the table into ruby objects to manipulate and organize.
21. What's the difference between agile workflow and waterfall method?
Working on Analysis, Planning, Coding and testing concurrently in small chunks- rather than doing each of them in one separate chunk.
22. What is the difference between `#new` and `#create`?
The #create 'method' makes and saves the object in the database- while ]the #new method just makes it.
