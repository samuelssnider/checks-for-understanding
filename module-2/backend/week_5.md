1. How do we make flash messages display on a page?
Using the flash hash (ex: flash[:success]) before an action in the controller- this can be accomplished by calling all flash messages in the application.scss file.

2. Where is cart information/temporary information usually stored?
Each item id in the cart as well as a quantity for it.

3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?

We would want to have it persist in our database- the user logging back into our site wouldn't want to see her cart destroyed. This does take up space in our database however- data that would have to be cleaned every so often to prevent the permanent storage of older carts.

4. What is the purpose of the asset pipeline?

The asset pipeline is a way to store all the assets of a webpage in a compressed, condensed way so as to make as few requests to the server as possible.

5. Why do we precompile our assets?
So the browser/client doesn't have to make a request for each one as it browses our webpage.

6. What do each of the following tags do?


```ruby 
<%= stylesheet_link_tag "application" %>
ruby helper to indicate the stylesheet to be used in rendering our website.
<%= javascript_include_tag "application" %>
ruby helper to indicate where the javascript for our site lives.
<%= image_tag "rails.png" %>
ruby helper to create an image tag - saves us from writing our own image tag.
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

Great readme's help the user incorporate our gem/ use our project seemlessly, helping them through all the version control and setup problems they might have. Gives the user a step by step guide how to start up and use out application.

8. What are the top four accessibility issues that we as developers should be aware of?

Vision, Dexterity, Sight, Cognitive Ability


9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
This is a callback, we would use this to execute something at a certain point during the controller action/s

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```

class User < ActiveRecord::Base
	scope :now, -> {where(status: active)}
end

11. What is the difference between a scope and a class method?

Their place in the controller; Scopes are easier to 'chain' together. Scopes look cleaner if they are small, where they get very messy if they are large.
