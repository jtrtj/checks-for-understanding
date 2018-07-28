### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 5 Questions
1. How do we make flash messages display on a page?

  After an action in a controller you set the flash message to what you want to be displayed. Then somewhere in your views (generally application layout so it appears on all pages) you set up the flash to display its key's contents.

2. Where is cart information/temporary information usually stored?

  `session[:cart]`

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?

  Unless you want to store the items every user may have bought but didnt for analysis, you don't store the cart until it becomes an order to save space in your database.

4. What is the purpose of the asset pipeline?

  Concatinate, precompile, minify and fingerprint the assets to help out the browser

5. Why do we precompile our assets?

  To speed up loading of webpages on rails

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

  links a stylesheet tag, a javascript script and an image.
  These are the ERB helpers to link things instead of using the html elements. you can use path helpers with them.
7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

8. What are the top four accessibility issues that we as developers should be aware of?

  navigation, text, images, forms - these would be my guesses

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

  a callback. when you want to run some method before a row is saved in the database.

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```
  `if @user.active?`

11. What is the difference between a scope and a class method?

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  

    cart[:48] = 4
  12b. How would you increase the quantity of item 29?  
    cart[:29] += 1
  12c. How would you find out how many items your user is thinking about purchasing?   
    cart.keys.sum
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  


### Self Assessment:
Choose One:

* I was able to answer a few questions independently, but relied heavily on outside resources 

Choose One:

* I feel confident about the content presented this week

