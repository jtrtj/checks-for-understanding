## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?

  `rails new your_app_name`
2. What do Models generally inherit from in rails?

  `ApplicationRecord`
3. What do Controllers generally inherit from in a rails project?

  `ApplicationController`
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

  `resources :horse, only [:show]`
5. What rake task is useful when looking at routes, and what information does it give you?

  `rails routes` shows you all of the routes for your models that are availible.
6. What is an example of a route helper? When would you use them?

  `new_horse_path(horse)` - if you wanted to make a link to the new horse action in the horse controller
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

  path is relative and url is absolute
8. What are strong params and why are they necessary?

  params that only allow the fields for a specific model in the app. set up so that tricksters can't mess with your app and try to get server or database info from errors.
9. What role does `form_for` play in helping us create our forms?

  You pass it an ActiveRecord object and it knows what path to use to create or edit that object. It can also autofill fields with the objects existing attributes when doing and edit.
10. How does `form_for` know where to submit the user's input?

  You give it an ActiveRecord object: `<%= form_for @horse do |f| %>`
11. Create a form using a `form_for` helper to create a new `Horse`. 

  ```ruby
  <%= form_for @horse do |f| %>
    <% f.label :name %>
    <% f.text_field :name %>
    <% f.label :age %>
    <% f.text_field :age %>
    <% f.label :breed %>
    <% f.text_field :breed %>
    <% f.submit %>
  <% end %>
  ```
12. Why do we want to validate our models?

  So that if someone tries to make an instance of that model with fields that can't be blank or with a non unique attribute, the database will reject the entry.
13. What are the steps of the DNS lookup?
  
  User enters a URL. Browser asks OS if URL is in cache. If it's not it asks the DNS, the DNS then asks a heirarchy of URL servers if they know what the IP address is for that URL. Once it gets it's answer, it returns the IP address back to the OS which gives it to the Browser and the browser makes a request to the server with that IP address.

### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?

  `Horse.move(prance())`

  ```ruby
  def move
    prance
  end
  ```
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  

  `furniture[:table][:height] vs furniture[:purchased]`
16. What is inheritance?

  When a ruby class gets methods from an externally established class that has methods you would use on any class. Such as a Rails model inheritting from ApplicationRecord.

### Self Assessment:
Choose One:

* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel comfortable with the content presented this week

