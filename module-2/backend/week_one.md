## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.

  GET, POST, PUT, PATCH, DESTROY

2. What is Sinatra?

  Sinatra is a framework that allows us to build ruby apps that use databases and .erb front facing views

3. What is MVC?

  Models, Views, Controllers.
  
  it's an app design pattern

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

  To created RESTful web apps

5. What types of variables are accessible in our view templates without explicitly passing them?

  params

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
  @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```ruby
  get '/horses' do
  @count = 1
  @name = 'Mr. Ed'
    erb :index
  end
  ```

8. What's the purpose of ERB?

  Gives us the ability to use ruby code to fill out HTML content

9. Why do I need a development AND test database?

  So that you can clear the database after a test fills it in without affecting the database that is actually storing things (development)

10. What is CRUD and why is it important?

  C.reate, R.ead, U.pdate, D.elete

  it's a standard protocol to give state to **stateless** HTTP actions

11. What does HTTP stand for? 

  Hyper Text Transfer Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

  <%= `ruby`%>
    
    Render the result of the included ruby statement to the html string
    
  <% `ruby`%>
   
    do the ruby code but do not show us the result

13. What's an ORM? What does it do?

  Object Relational Mapper - Gives us the ability to treat rows in a database table like OOP objects and create associations between them

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?

  ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

  post '/restaurants' - **Create** this would be the route to create a new object and save it to our database

  get '/restaurants' - **Read** this would display an index of all restraunts

  get'/restaurants/new' - **Read** this would display the form to **Create** a new restaurant

  get '/restaurants/id' - **Read** this route would show the information for a single restaurant

  get '/restaurants/id/edit - **Read** this route would show the edit form to **Update** a restaurant

  put '/resaturans' - **Update** - this route would **Update** a restauarant in our table of restaurants

  delete '/restaurants/id/' - **Destroy** - this route would **Destroy** a row in our table


16. What's a migration? 

  as far as I can understand, it sets ups the attributes the schema looks for when creating a new object in a given table.

17. When you create a migration, does it automatically modify your database?

  no, but it does automatically change the schema

18. How does a model relate to a database?

  a model controls associations and methods for each row in the table

19. What is the difference between `#new` and `#create`?

  `#new` - creates a new object but does not save it as a row

  `#create` - creates a new object and saves it as a row in its table

### Review Questions:  
20. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

  put code that looks like this in the `seeds.rb` file.

  ```ruby
  CSV.foreach('films.csv', headers: true, header_converters: :symbol) do |film|
  Merchant.create(
                  id:         film[:id],
                  title:       film[:title],
                  description:       film[:description]
                )
  end
  ```

21. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?

```ruby
activities[:hiking][:supplies].push('granola bar')
```

22. What are the 4 Principles of OOP? Give a one sentence explanation of each.

  abstraction - creation of classes and objects

  encapsulation - hiding of implementation

  inheritance - objects can relate to eachother with either a “has a”, “uses a” or an “is a” relationship.

  polymorphism - an object can have many methods that manipulate it in different ways

### Self Assessment:
Choose One: (erase the others)

* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel comfortable with the content presented this week - 85%
* I feel overwhelmed by the content presented this week - 15%

