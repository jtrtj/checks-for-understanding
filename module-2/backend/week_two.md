## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

  ActiveRecord is a plug in for ruby that adds methods for your application to interact with SQL databases. It is agnostic as to what database program you are using as long as it is SQL.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

  `all`,`where()`,`find()`,`select`,`group`,`order`

  they are methods inherited from ActiveRecord that translate ruby like language of objects/classes to SQL commands to find and organize rows/columns in tables.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
    
    ```owner_id = team.owner_id
      Owner.find(owner_id).name```
4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

  `find(4).owner`

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

  students have many teachers and teachers have many students so it would be a many to many relationship

  ![school_teachers](/Users/jtr/turing/checks-for-understanding/module-2/backend/diagrams/Screen Shot 2018-07-06 at 7.42.23 PM.png)
6. Define foreign key, primary key, and schema.

  -foreign key is a number in a table's column that corresponds to the primary key of another table.

  -primary key is the indexed key each row of a table is assigned when it is created

  -schema is a file that instructs our database as to what each table should have in it's rows and what relationships it may have to other tables
7. Describe the relationship between a foreign key on one table and a primary key on another table.

  The foreign key gives acces to another table's rows as primary keys
8. What are the parts of an HTTP response?

  a response code, headers (i think params are in here) and message body


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.

  average() - gets the average of the column provided as an argument

  sum() - sum the data in the argument

  find() - finds the row with the given ID

  where() - similar to find_all or find_by in ruby, it can return things matching circumstances you provide

  order() - orders rows according to the column you provide
2. Name your three favorite ActiveRecord rake tasks and describe what they do.

  drop - deletes the entire database

  create - creates the database

  migrate - builds your table blueprints in the schema file.
3. What two columns does `t.timestamps null: false` create in our database?

  created_at and updated_at
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?

  A School has_many teachers
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

  ![school_teachers](/Users/jtr/turing/checks-for-understanding/module-2/backend/diagrams/Screen Shot 2018-07-06 at 7.29.31 PM.png)
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.

  doctors have many patients and patients have many doctors (many to many)
8. Describe and diagram the relationship between museums and original_paintings.

  Original paintings have many museums through exhibitions
  
  ![painting_exhibitions](/Users/jtr/turing/checks-for-understanding/module-2/backend/diagrams/Screen Shot 2018-07-06 at 7.37.26 PM.png)
9. What could you see in your code that would make you think you might want to create a partial?

  Forms and Nav Bars

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel overwhelmed by the content presented this week

