## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?
A small piece of data sent to a user and stored on their client as to save any type of information about their 'session' as HTTP is stateless
* What’s the difference between a session and a cookie?
A session is stored on the server whereas a cookie is stored in the browser. This makes sessions much more (but still not totally) secure than cookies.
* What’s a flash and when do you want to use flashes?
Flash is a hash that stores messages to be displayed to the user depending on actions they take- conformation messages and failure messages.
* Why do people say “HTTP is stateless”?
HTTP is stateless because it does not store any information- this is what cookies and sessions are required for- to save any state information that belongs to users.
* What’s authentication? Explain.
Authentication is checking a users credentials from a login or other 'specific visit'. It confirms the user is who they say they are with some kind of check.
* What’s the difference between authentication and authorization?
Authentication is a one-time log in where authorization is something that persists and checks everytime a user tries to navigate around a website.
* What’s a before filter?
Before filter declares an action that must be taken before any action is taken in the MVC, it is useful for checking if a user is an admin or is logged in.
* How do we keep track of a user once they’ve logged in?
Using the session hash is the way we've accomplished this so far
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
When you want differing levels access to the same data- admin/items
* At a high level, what tools can you use to implement authorization? How would you use them?
BCrypt can encrypt your passwords so they are not legible. You can use the session hash to save the user after they have been authorized.
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
An Enum is a tool to map to integers in a database, so they can be identified by a different name. It gives you methods based on the names in it's array ex: admin!, admin? A Integer needs to be in your database to use an enum.

enum category: [:user, :admin, :super_admin]

* What are some strategies you can use to keep your views DRY?
Creating POROs and methods in the models to keep all of the repeat logic outside of the view.
