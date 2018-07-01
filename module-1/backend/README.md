Week 1 Questions
List the five common HTTP verbs and what the purpose is of each verb.

Get - gets a url
Post - sends information to a url
Patch - updates a resource, partially
Put - updates a resource, completely
Delete - delete a resource

What is Sinatra?
Sinatra is a framework built off Rack that helps make writing server-side code easier.

What is MVC?
Model/View/Controller - a design pattern for server-side code organization.

Why do we follow conventions when creating our actions/path names in our Sinatra routes?
It allows our api to be predictable as a RESTful interface, and makes it more clear what each route does when looking at the code.

What types of variables are accessible in our view templates without explicitly passing them?
Instance variables.

Given the following block of code, how would I pass an instance variable count with a value of 1 to my index.erb template?
```ruby
get '/horses' do
  @count = 1
  erb :index
end
```

In the same code block, how would I pass a local variable name with a value of Mr. Ed to the view?
```ruby
get '/horses' do
  @count = 1
  mr_ed = "Mr. Ed"
  erb :index, :locals => {:mr_ed: mr_ed}
end
```

What's the purpose of ERB?
It renders views with dynamic content.

Why do I need a development AND test database?
The test database can use smaller amounts of data, and the development database is a bit closer to the actual production db implementation.

What is CRUD and why is it important?
Create, Read, Update and Delete.  It's important because these are the 4 operations that can be applied to a db record.

What does HTTP stand for?
Hypertext Transfer Protocol

What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
Using the <% some code... %> or the <%= some code... %>.  The first one executes code, while the second executes code and puts the result on the view.

What's an ORM? What does it do?
Object Relational Mapping, it communicates with the database and maps the information to a ruby object.

What's the most commonly used ORM in ruby (Sinatra & Rails)?
ActiveRecord

Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
```Ruby
get '/restaurants' do
   # this finds all restaurants in the db and returns them
end

get '/restaurant/:id' do
  # this finds a specific restaurant by id
end

get '/restaurants/new' do
  # this gets the form to add a new restaurant
end

post '/restaurants' do
  # this creates a new restaurant in the db
end

get '/restaurants/:id/edit' do
  # this gets the form to edit a restaurant
end

put '/restaurants/:id' do
  # this updates a specific restaurant by id
end

delete '/restaurants/:id'do
  # this deletes a specific restaurant by id
end
```

What's a migration?
A migration is a change in the db schema, which is run once (and edits or creates the schema).

When you create a migration, does it automatically modify your database?
No, you have to run the migration.

How does a model relate to a database?
It defines the class that creates a Ruby object with the data coming back from the db.

What is the difference between #new and #create?
New creates a new Ruby object, while create not only creates a new ruby object but also saves it in the db.

Review Questions:
Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
with a CSV method in the seeds file, which parses each row and inserts it into a db with headers.

Given the following hash:

activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}

How would I add 'granola bar' to things you should have when hiking?
```Ruby
  activities[:hiking][:supplies] << 'granola bar'
```

What are the 4 Principles of OOP? Give a one sentence explanation of each.
Encapsulation, which essentially hides as much data as possible, allowing for predictable ways to interact with data.
Abstraction, which basically hides away the inner workings of an object or class, so we can interact with it in specific ways.
Inheritance, which allows classes to inherit from parent classes or to have sub classes.
Polymorphism, which lets us overwrite methods in classes so we aren't stuck with inherited methods if we don't want them.

Self Assessment:
Choose One: (erase the others)
I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
I feel comfortable with the content presented this week
