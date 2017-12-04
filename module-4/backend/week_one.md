## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's the most useful thing you learned from completing the intermission week work?
Basic syntax of javascript, and how logic looks basically the same in ruby and js. I also had a personal assignment using AJAX, similar to the module 3 lesson we had on AJAX. This helped me solidify some of the js/jQuery basics as well.
2. What are some tools to help debug JavaScript code?
Debugger, Console.log, and the many tools that the google chrome developer tools employ.
3. What are some tools you need in order to unit test your JavaScript?
Mocha is what we used in the prework and the week one assignments, but I know there are more options. Unit testing in the professional JS is prevalent where feature and model are not as much.
4. What is the syntax for invoking a function?
Parenthesis (empty or containing arguments) after a function name are required to invoke it, otherwise just the function itself is returned.
5. What is CORS?
Cross-Origin Resource Sharing. A mechanism that uses additional HTTP headers to let a user agent gain permission to access selected resources from a server on a different origin than the site currently in use. Basically a user agent makes a cross-origin HTTP request when it requests a resource from a different domain, protocol, or port that the one which the current document originated
6. How do we enable CORS?
A 'Access-Control-Allow-Origin' header will allow us on our project will override the default CORS protocol, and allow us to access different resources without changing the page.
7. What's `this` in JavaScript?
This is a complexity in js, but it basically comes down to a variable that changes based on the current scope. It is by default the window, but if its inside a function, it is that function itself. Using #.bind() will help us change the scope of this inside of a function. With arrow functions, this retains the value of the enclosing lexical context's this. In other words, the variable 'arrowed' to this will retain this's current scope.
8. What is Webpack and why is it useful?
Webpack is a gem that helps us organize our required js, css, and sass files into just being referenced in one index.js file. It is a 'module bundler' that takes modules with dependencies and generates static assets representing those modules
9. When/why do you want to use event delegation?
Event delegation allows us to avoid adding listener events to specific nodes; we just need the event listener on the parent node. That event listener can tell from the bubbling of the event which child element was 'evented' on.
10. What is a callback function?
A 'higher-order' function that is passed another function as a parameter. It might sound complicated, but it's really as simple as: 
$("#button").click(function() {
  alert("the button was Clicked");
});
11. What's `npm` and what do we use it for?
A typical application has dependencies on tens of packages. npm is a way to organize these packages and dependencies. It also gives us access to some command-line commands (as well as the ability for us to set up custom versions of these).
Three distinct parts: website, registry, and CLI.

#### Review  
12. What's the MVC design pattern? Describe each part of MVC.
Model-View-Controller. The design pattern is organized in a top down configuration from the controller. Separating these elements and having them organized so, allows us to avoid some of the pitfalls of having these elements organized amongst themselves. Separate internal representations of the information from the ways information is presented to, and accepted from, the user.
13. What are a few ways to optimize a Rails application?
We can use caching to save large requests we are making so they only have to be loaded once. We can use asynchronous tools like background workers to load certain parts of our pages separately if one is particularly slow.
14. What's a background worker? When would we want to use a background worker?
A background worker is a tool we can use to operate on some function that we want to execute without causing the page we are on to only load when that function is complete.
