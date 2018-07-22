## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?

  a small piece of data that the browser stores to give state to stateless http
2. What’s the difference between a session and a cookie?

  session has more to do with authentication 
3. What’s a flash and when do you want to use flashes?

  A short message displayed on the page to inform the user that an action they triggered has occured
4. Why do people say “HTTP is stateless”?
5. What’s authentication? Explain.

  Proving a user is who they say they are. Generally it cross checks a user_name with a password. The password is stored in an encrypted hash that knows what it's plain text version looks like. So the app can ask 'Does this username go with the password for this user?'.
6. What’s the difference between authentication and authorization?

  Authentication is 'Who are you?' and Authorization is 'What are you allowed to do/view?'. After you have been authenticated that app is programmed to only alllow you to do certain things and access certain directories through namespacing and ruby conditional statements.
7. What’s a before filter?

  A piece of code that goes in controllers that tells the controller to run some functions before each or specific actions.
8. How do we keep track of a user once they’ve logged in?

  Logging in creates a new session which can tell the app at any point who the current user is according to the database.
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

  Namespacing is when you want certain pages to be availible through seperate controllers with different before action functions than the standard actions for their corresponding model.

  Nesting resources is good for when you want to edit or create a model including the id of another model that it belongs_to
10. At a high level, what tools can you use to implement authorization? How would you use them?

  A method that checks if a current user is present/a session has a user id. A method that checks if the current user has the role of admin.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

  Enums are declared on the model to tell your app what an integer value in a column could stand for. For example if the users table has a role column that is 0 or 1, the enum tells the model what that 0 or 1 stands for. You tell the enum what column and in order what the integers stand for - `enum role: [default, admin]` 0 would mean default and 1 would mean admin.
12. What are some strategies you can use to keep your views DRY?

  conditionals that render partials for default users vs admin users, Putting a nav partial in the application.html.erb so that the app automatically puts it on every page. 


### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

  ```ruby
  example.sort_by do |holiday, holiday[:name]|
    holiday[:name]
  end.join
  ```
  something like that
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300? 

  I do not know

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

