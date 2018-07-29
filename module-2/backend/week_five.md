### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
* By using ```flash[:notice] = "some message"``` in the controller, then iterating over flash messages in the layout view.

2. Where is cart information/temporary information usually stored?
* In our session, under session[:cart]

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
* We don't need a record of each cart to persist permanently, it takes up space for data we won't use.  I could see a reason to persist that data, if I logged out and logged back in, I would expect my cart data to still be there.

4. What is the purpose of the asset pipeline?
* The asset pipeline makes the data of those assets smaller so the page loads faster.

5. Why do we precompile our assets?
* It's less work for our client's computer to do.

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

* It creates the appropriate link, script, or image tags in html with their associated data.

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

* A great readme explains why the project exists (what problem does it solve?), how to interact with the site (if you have an API), and how to set up the project on your local machine.

8. What are the top four accessibility issues that we as developers should be aware of?
* Visibility (size of text/images, color choices), being able to navigate the site without using a mouse, making the site intuitive to use (simplicity)...  (that's all I can think of, I don't remember this coming up in class)

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
* It's an example of a callback.  It would exist in a controller.

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
```ruby
scope :active, User.where(active: true)
```


11. What is the difference between a scope and a class method?
A scope filters objects automatically, while a method must be called to take effect.


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
  * I'll assume cart exists in the session object, so `session[:cart]["48"] = 4`
  12b. How would you increase the quantity of item 29?  
  * `session[:cart]["29"] += 2`
  12c. How would you find out how many items your user is thinking about purchasing?   
  * `session[:cart].values.sum`
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
* Polymorphism allows classes to override methods inherited from their parent class.  It's related to duck-typing, since any classes that share a method can be called with duck-typing.
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
* I don't remember being taught this, but I would assume something like number_to_phone(variable)


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
