# Project.Eroy

# Restaurant Mnanagement System

# What the database is all about? 

The Restaurant Management System  helps the restaurant manager to manage the restaurant more effectively and efficiently by computerizing meal ordering, billing and inventory control.Mission is to organized and manage data for restaurant.


# ERD (Entity Relationship Diagram)

![image(https://user-images.githubusercontent.com/73158407/103190738-7b3c3a80-488f-11eb-9fb4-48d198ddf5b3.png)


# Where did you get the database?

https://www.youtube.com/watch?v=YhkwUAVMrzg

# Table Description
Chefs are identified by name, chefid, salary, hire date. Restaurant also identified by name, address, phone number. Restaurant has waiter identified by waiter id, name, salary, hire date. Waiter serves food to customer. Customer also identified by customer id, name, phone number. Customer gives orders by waiter. Orders identified by cid, oid, mid, quantity, status, date.
Store a start data, an end data, and the text to the contact.

# Database Dependency Diagram (Image)

![image(https://user-images.githubusercontent.com/73158407/103190955-42e92c00-4890-11eb-9d9c-214397ee192f.png)

 
  # Query 1
  I. This query is shows you on how to add a table.
  II. It's important because it's easy to add records from a table.
  III. # INSERT      INSERT INTO `customer`(`cid`, `Name`, `phoneno`, `address`, `waiterid`) 
                     VALUES (' 4 ' , ' Yuri Lee ' , ' 5678597 ' , ' Brisbane ' , ' 2 ' );
  ![image(https://user-images.githubusercontent.com/73158407/103194735-c65d4a00-489d-11eb-80b9-493ec167f19c.png)

 # Query 2
 I. This query is shows you on how to remove rows from table.
 II. It's important because it's easy to remove records from a table.
 III. # DELETE     delete from 'order' where oid='1'
  ![image(https://user-images.githubusercontent.com/73158407/103192642-a6765800-4896-11eb-9aa0-5835a39d7b05.png)
  
  
  # Query 3
  I. This query is shows you on how to sort the result-set in ascending or descending order.
  II. It's important because it's easy to sort using ascending or descending order.
  III. # ORDER BY  SELECT name FROM 'meal' ORDER BY chefid ASC
     ![image(https://user-images.githubusercontent.com/73158407/103196167-e4787980-48a0-11eb-95b8-7d0f5d36a2fa.png)
     
     
  # Query 4
  I. This query is shows you on how to selects all the customer from the country "Brisbane", in the "Customer" table.
  II. It's important because it's easy to filter the records and fetching only the necessary records.
  III. # WHERE     SELECT * FROM Customer WHERE address='Gold Coast';
     ![image(https://user-images.githubusercontent.com/73158407/103198876-a9794480-48a6-11eb-88a2-c50b620d7196.png)



  
     
     

