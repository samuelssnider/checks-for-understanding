## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
rails new name -options
2. What do Models generally inherit from in rails?
ActiveRecord::Base
3. What do Controllers generally inherit from in a rails project?
ActionController::Base
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources :horses, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you?
rake routes- give you all the routes your website supports, along with their link prefix, verb, uri pattern, and controller action.
6. What is an example of a route helper? When would you use them?
Given by rails as the 'prefix' in rake routes. helps you write in links in your database using convienient syntax.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
_url is needed for redirect_to because the HTTP specification mandates that the Location.
where _path can be used in views because the page is implicit
8. What are strong params and why are the necessary?
Strong params allow us to create a new object from information inherited in params- like that given to us from a form.
9. What role does `form_for` play in helping us create our forms?
takes us away from having to name the forms method, can overlap edit and new functionalities, and makes input fields and such easier to create and standardize
10. How does `form_for` know where to submit the user's input?
based on the argument
11. Create a form using a `form_for` helper to create a new `Horse`.

<%= form_for(Horse.new) |f| do %>
<%= f.label :name %>
<%= f.text_area :name %>
<%= f.label :breed %>
<%= f.text_area :breed %>
<%= f.submit %>
<% end %>


12. Why do we want to validate our models?

So we don't have repeats, or missing data points that we need
