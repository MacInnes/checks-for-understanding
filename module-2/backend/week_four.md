## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
A cookie is a small piece of data stored on the client's browser.
2. What’s the difference between a session and a cookie?
A session is stored on the server, while a cookie is stored on the client.
3. What’s a flash and when do you want to use flashes?
A flash is a message sent from the server that populates a specific field, usually in the layout view.
4. Why do people say “HTTP is stateless”?
Because it does not maintain state between requests.
5. What’s authentication? Explain.
Authentication is verifying a users' credentials.
6. What’s the difference between authentication and authorization?
Authorization is checking whether a user is authorized to view certain pages or edit/create data.
7. What’s a before filter?
A before filter allows only authorized users to reach certain routes or controller methods.
8. How do we keep track of a user once they’ve logged in?
Setting a session[:user_id]
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
You want to namespace a resource when you want to control authorization to that resource, while you want to nest a resource when two resources are related.
10. At a high level, what tools can you use to implement authorization? How would you use them?
You can create methods that verify a user's role to allow access to certain controllers or routes.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
An enum is a collection of different values (my only experience is strings, though I suppose others could be used), allowing you to store data in the database as an integer.  The enum is declared in the model.
12. What are some strategies you can use to keep your views DRY?
Using an \_form (underscore form, in case you couldn't see it with weird formatting) to reuse for edit/new is one example.  Using partials and pushing any common html to the application view (such as nav).

### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
# declared this as a variable...
holidays = [
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
```ruby
holidays.sort_by do |each|
  each[:holiday][:name]
end
```
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
Normally I'd simply call .to_i, but I'm not sure how to deal with the $


### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel comfortable with the content presented this week
