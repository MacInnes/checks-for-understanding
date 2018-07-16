## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
* rails new <app name>
2. What do Models generally inherit from in rails?
* ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
* ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources :horses, only: [:show] (show horse haha)
5. What rake task is useful when looking at routes, and what information does it give you?
* rake routes, gives you all paths available, the route explicitly, and the controller method responsible for that route
6. What is an example of a route helper? When would you use them?
* horse_path(horse), when I want a variable to represent the path, in case it changes later
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
* `_url` uses an absolute path, while `_path` uses a relative path
8. What are strong params and why are they necessary?
* they provide validations for the data needed to create an instance of a model, or a row in a db table
9. What role does `form_for` play in helping us create our forms?
* it allows us to create a dynamic form that (somehow) figures out if we're making a PUT or POST request, so it can be reused between the new and edit views.  It's basically magic imo
10. How does `form_for` know where to submit the user's input?
* based on the controller method that invoked the use of the form.
11. Create a form using a `form_for` helper to create a new `Horse`.
```Ruby
  <% form_for :horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.submit %>
```
12. Why do we want to validate our models?
* to ensure that they receive the data we expect, without any inconsistencies
13. What are the steps of the DNS lookup?
* Root server, Name server, Authoritative Name Server...?  


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
* horse.move.prance

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
* furniture.purchased vs furniture.table.height
16. What is inheritance?
* inheritance is where a class can inherit methods or state from a parent class

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel confident about the content presented this week
