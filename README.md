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
  III.         
   INSERT INTO `customer`(`cid`, `Name`, `phoneno`, `address`, `waiterid`)                                                                             
   VALUES (' 4 ' , ' Yuri Lee ' , ' 5678597 ' , ' Brisbane ' , ' 2 ' );                                                                          
  ![image(https://user-images.githubusercontent.com/73158407/103194735-c65d4a00-489d-11eb-80b9-493ec167f19c.png)

 # Query 2   
 I. This query is shows you on how to remove rows from table.                                                                                                           
 II. It's important because it's help to remove records from a table.                                                                                                
 III.        
  delete from 'order' where oid='1'                                                            
 ![image(https://user-images.githubusercontent.com/73158407/103192642-a6765800-4896-11eb-9aa0-5835a39d7b05.png)
  
  
  # Query 3                              
 I. This query is shows you on how to sort the result-set in ascending or descending order.                                                                                
 II. It's important because it's help to sort using ascending or descending order.                                                                            
 III.         
  SELECT name FROM 'meal' ORDER BY chefid ASC                                                                         
 ![image(https://user-images.githubusercontent.com/73158407/103196167-e4787980-48a0-11eb-95b8-7d0f5d36a2fa.png)
     
     
  # Query 4
  I. This query is shows you on how to selects all the customer from the country "Brisbane", in the "Customer" table.                            
  II. It's important because it's easy and help to filter the records and fetching only the necessary records.                                       
  III. WHERE         
   SELECT * FROM Customer WHERE address='Gold Coast';                                                                         
 ![image(https://user-images.githubusercontent.com/73158407/103198876-a9794480-48a6-11eb-88a2-c50b620d7196.png)
     
     

# Query 5
  I. This query is shows you on how will select all customers, and any orders they might have.                                                     
  II. It's important because it helps keyword returns all records from the left table (Customers),even if there are no matches in the 
  right table (Orders).                      
  III.  
   (SELECT Customer.Name, orders.oid                                                                            
   FROM Customer                                                                                                       
   LEFT JOIN orders                                                                                                  
   ON Customer.cid=orders.cid                                                                                            
   ORDER BY Customer.Name;                                                                                             
 ![image(https://user-images.githubusercontent.com/73158407/103202604-16450c80-48b0-11eb-8eae-6e45a3ac9cd1.png)
 
 
 # Query 6
  I. This query is shows you on how to combine rows from different tables if the join condition is true.                                                                         
  II. It's important because it's help to combine all rows from differebt table.                                                    
  III.                                                                                                  
   SELECT orders.oid, customer.Name                                                                                           
   FROM orders                                                                                                                              
   INNER JOIN customer ON orders.cid = customer.cid;                                                                                    
  ![image(https://user-images.githubusercontent.com/73158407/103203931-5bb70900-48b3-11eb-828f-8a7c8840da07.png)


 # Query 7
  I. This query is shows you on how to returns all records from the right table (Customer), even if there are no matches in the left table (orders).          
  II. It's important because it's help to  return all Customer, and any orders they might have placed.                                          
  III.                                                                                                                        
   SELECT orders.oid, customer.Name, customer.address                                                                                                          
   FROM orders                                                                                                                                                     
   RIGHT JOIN customer ON orders.cid = customer.cid                                                                                                        
   ORDER BY orders.oid;                                                                                                                                            
  ![image(https://user-images.githubusercontent.com/73158407/103204945-aafe3900-48b5-11eb-9627-fde6127d5a43.png)
  

# Query 8
  I. This query is shows you on how to get 3 Highest salaries records from chef table.                                                    
  II.It's important because it's help to rank the highest salaries.                                                                         
  III.
   select distinct salary from chef a where 3 >= (select count(distinct salary) from chef b where a.salary <= b.salary) order by a.salary desc
  ![image(https://user-images.githubusercontent.com/73158407/103211915-b4dc6800-48c6-11eb-9fe5-6a25fc708180.png)

# Query 9
 I.This query is shows you on how to count mid from meal table.                                                                       
 II. It's important because it's help to count from table.                                                                                     
 III.
  SELECT COUNT(mid) FROM meal                                                                             
 ![image(https://user-images.githubusercontent.com/73158407/103213541-3b934400-48cb-11eb-9589-ed1907d9ad08.png)
  
  
 # Query 10
 I.This query is shows you on how to find the smallest price from meal.                                                                         
 II.It's important because it's help to finds the price of the cheapest meal.                                                              
 III.
  SELECT MIN(Price) AS SmallestPrice FROM meal                                                                  
  ![image(https://user-images.githubusercontent.com/73158407/103213915-56b28380-48cc-11eb-909f-b0728580ef84.png)
  
  
 # Query 11
 I.This query is shows you on how to find average price from meal.                                                                                                         
 II.It's important because it's help to finds the average price of all meal.                                                                                       
 III.
   SELECT AVG(Price) FROM meal                              
   ![image(https://user-images.githubusercontent.com/73158407/103214365-71392c80-48cd-11eb-8089-bb0b708b663b.png)
      
 
  # Query 12
 I. This query is shows you on how to find the highest salary from waiter.                                                       
 II.It's important because it's help to finds the  highest salary from waiter.                                                                         
 III.
  SELECT MAX(salary) AS HighestSalary FROM waiter                                                                     
    ![image(https://user-images.githubusercontent.com/73158407/103215503-c460ae80-48d0-11eb-8b36-ed89460070d5.png)
  
  
 # Query 13
I.This query is shows you on how to find lists the number of customers in each address.                                   
II. It's important because it's help to identify the number of customers in each address.                               
III.                                
 SELECT COUNT(cid), address FROM customer GROUP BY address                                                  
![image(https://user-images.githubusercontent.com/73158407/103216109-7482e700-48d2-11eb-8252-81c39cece469.png)


 # Query 14
 I.This query is shows you on how to select all customers that are located in (Melbourne, Perth, Gold Coast).                                                           
 II.It's important because it's help to identify all customers in there places that mention from table.                                                                      
 III.
 SELECT * FROM customer WHERE address IN ('Melbourne', 'Perth','Gold Coast' )                                                                             
 ![image(https://user-images.githubusercontent.com/73158407/103251274-69ad6e00-4935-11eb-931c-a4c8dfd9fa07.png)
 
  
 # Query 15
 I.This query is shows you on how to select all customers that are not located in (Melbourne, Perth, Gold Coast).                    
 II. identify all customers are not belong in there places that mention from table.                                         
 III.
 SELECT * FROM customer WHERE address NOT IN ('Melbourne', 'Perth','Gold Coast' )                                  
 ![image(https://user-images.githubusercontent.com/73158407/103251542-4fc05b00-4936-11eb-831b-32c0c07e5b1c.png)



 # Query 16
 I.This query is shows you on how to matches customers that are from the same address.                                        
 II.It's important because it's help to find gmmatches customers address from table.                                                          
 III.
 SELECT A.Name AS name1, B.name AS name2, A.address FROM customer A, customer B WHERE A.cid <> B.cid AND A.address = B.address ORDER BY A.address
 ![image(https://user-images.githubusercontent.com/73158407/103252141-b9d9ff80-4938-11eb-841a-a94b087f9edd.png)
 
 
  # Query 17
 I.This query is shows you on how to use the SQL EXISTS operator to test for the existence of rows returned by a subquery.         
 II.It's important because it's help to query returns all rows in the  customer table.                                        
 III.
 SELECT cid, Name FROM customer WHERE EXISTS( SELECT NULL) ORDER BY name                                               
 ![image(https://user-images.githubusercontent.com/73158407/103257943-71c6d700-4950-11eb-95ce-cb90ed03cea5.png)
 
 
  # Query 18
 I.This query is shows you on how to remove duplicate salary from waiter table                                 
 II.It's important because it's help to remove duplicates salary data.                                      
 III.
  SELECT DISTINCT salary FROM waiter ORDER BY salary DESC                                                           
  ![image(https://user-images.githubusercontent.com/73158407/103258170-51e3e300-4951-11eb-885a-0d73222a4d5c.png)
   
   As you see we have duplicate salary data e.g., 400 because two or more employees have the same salary.                   
   To remove the duplicate, you add the DISTINCT operator to the SELECT clause as follows:
                             
   
   
 ![image(https://user-images.githubusercontent.com/73158407/103258232-9b343280-4951-11eb-90c0-776617372493.png)
   
   Now all duplicates are removed from the result set.                            
 
 
 
  # Query 19
 I.
 II.
 III.
 
 
 
  # Query 20
 I.
 II.
 III.

























