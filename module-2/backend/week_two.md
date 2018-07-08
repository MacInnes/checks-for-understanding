## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

* ActiveRecord is an ORM which allows us to write database calls in ActiveRecord so they can be easily translated to postgresql, mysql, or another database language.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
* Find, create, select, where, pluck, etc...  We have access to these methods because we inherit them from ActiveRecord::Base.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

```ruby
Team.find(4)
```

```ruby
Team.find(4).joins(:owners)
# not very confident in this one...
```

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

```ruby
Team.find(4).owner
```

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
* Many to Many
6. Define foreign key, primary key, and schema.
* Primary key is the unique identifier of each row in a table, foreign key is a reference to the primary key of a different table, and schema defines the columns of a table.
7. Describe the relationship between a foreign key on one table and a primary key on another table.
* The foreign key of one table references the primary key of another table.  Primary keys must be unique identifiers, while foreign keys do not have to be unique.
8. What are the parts of an HTTP response?
* Essentially a header and a body.  The header includes the response code, the body includes the content the server responds with.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
* where seems most useful, but I recently found pluck and I'm becoming a big fan.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
* rake db:migrate (which runs the migration), rake db:create (creates the db), and rake db:seed (which seeds the db with data)
3. What two columns does `t.timestamps null: false` create in our database?
* created_at and updated_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
* Many to many
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
* create a StudentsTeachers table.  a cool way I recently found to create this is to run 'rails g migration CreateJoinTableStudentsTeachers students teachers'
6. Give an example of when you might want to store information besides ids on a join table.
* I can't think of one...  I thought Ian said that a join (join or joins?) table should only include ids.
7. Describe and diagram the relationship between patients and doctors.
* I mean, a patient could have multiple doctors, but I picture it as a one-to-many relationship where one doctor has many patients.
8. Describe and diagram the relationship between museums and original_paintings.
* One-to-many as well, each original_painting can only be in one museum at a time.
9. What could you see in your code that would make you think you might want to create a partial?
* Repeated content in a view, like a nav bar, title, even the head of the html page

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel overwhelmed by the content presented this week
