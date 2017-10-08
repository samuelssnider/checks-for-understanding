## Week One - Module 3

Some of these questions are from this week, some are from previous weeks, and some are new concepts. Try answering without research first. If you are not sure, take a guess but acknowledge that it's a guess (faking an answer in an interview without acknowledging it as a guess is a bad idea). Follow up with the necessary research to understand these concepts. These tend to be common themes during the job hunt and are worth having a solid understanding of.

1. What is `json`, what does it stand for, and why is it important?
JavaScript Object Notation- Is a format for storing data; it is important to have a universal format for organizing data in online API's so that the dozens of different languages, browsers, and frameworks all a standardized data format to work with. XML was used before JSON, and is still used today; the nested tags in XML can greatly reduce legibility (at least for humans) vs JSON.
1. What kind of object is JSON in Ruby? How do we know it's JSON?
A Hash, JSON has a very particular format, using double quotes, curly braces, and colons to indicate either and object or a collection of objects.
1. What's an API?
Application Programming Interface. In the most simple terms, an API is a way for two pieces of software to communicate with each-other. Web- HTML, REST using HTTP, Local - OS or midlleware, Program- remote procedure call.
1. What's a RESTful API? How does that look in Rails?
Uniform Interface
Stateless
Cacheable
Client-Server
Layered System
Code on Demand
Based on Representational state transfer
GET, PUT, POST, DELETE


1. What is an ORM, what does it stand for, and why is it helpful?
Object Relational Mapping, a format for storing data, like a CSV, or using a programming language's objects to store data so it can be used or manipulated.
1. How do you create a record in the following table in SQL? In Active Record?   
   (Users table with columns first_name, last_name, email, and age)
   SQL: INSERT INTO users (first_name, last_name, email, age) VALUES ('sam', 'snider', 'sam@sam.com', 26)
   Active Record. User.create(first_name: 'sam', last_name: 'snider', email: 'sam@sam.com', age: 26)
1. How would you refactor this method?

```
def people_with_brown_hair
  people_with_brown_hair = []

  people.each do |person|
    if person.hair_color == "brown"
      people_with_brown_hair << person
    end
  end

  people_with_brown_hair
end
```
```
def people_with_brown_hair
  people.find_all |person| do
    person.hair_color == "brown"
  end
end
```
1. Given an array numbers = [1,2,3,4,5], find the sum of the doubles of all the numbers. 

numbers.reduce(:+) {|number| number * 2 }

#### Self Assessment  
Rate yourself on the following scale.  
4  I know and understand all these concepts and did not have to look anything up  
3  I know and understand most of these concepts but had to look something up  
2  I am uncertain about some of these concepts and had to look some things up ^^  
1  I am feeling lost about with these concepts and had to look many things up ^^  

2.5

I feel pretty comfortable with these concepts, but find myself having to look up the exact wording and explanation of REST and RESTful routes
