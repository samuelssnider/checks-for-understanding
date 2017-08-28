## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
Helper ORM to facilitate the creation and use of objects in a database

2. Assume you have the following model:


```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

Team.all, Team.count- Inheriting from the Base class in Active Record gives us these methods

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
Team.find(4)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
Team.find_by(owner_id: 4)
Owner.find_by(team_id: 4)

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
Students: has_many :teachers
Teachers: has_many :students
6. Define foreign key, primary key, and schema.
Foreign key- any key (use of id) that is not a tables primary key- used to link data in tables together based on relationships
Primary key- the id for a table, usually set up using an auto-increment
Schema- A 'roadmap' for what characteristics all the classes in the database will have.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
A foreign key will link a table to another table, and which objects are related to which other object.
8. What are the parts of an HTTP response?
Status line
Headers
Body



### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
