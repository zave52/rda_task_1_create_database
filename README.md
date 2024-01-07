# Database for online shop

It's time to build a database for an online shop! 

## Task
#### Prerequisites
- Install and confiture a MySQL database server on a Virtual Machine, connect to it with the MySQL client
- Fork this repository

#### Requirements
Edit the file "task.sql" to create a SQL script, for online shop database creation. The script should complete the following actions on the database server: 

1. Create a database (schema), called "ShopDB"
2. In the "ShopDB" database, create the following tables: 
    - "Products", which has the following columns: ID, Name, Description, Price, WarehouseAmount. 
    - "Customers", which has the following columns: ID, FirstName, LastName, Email, Address. 
    - "Orders", which has the following columtns: ID, CustomerID, Date
    - "OrderItems", which has the following columns: ID, OrderID, ProductID
    When creating the tables, take the folloiwing into account: 
    - Use approproate data type for each column. You will need to use one of the following data types for this task: INT, DATE, VARCHAR(50),VARCHAR(100)
    - Use autoincrement for the primary keys 
    - Use construction "FOREIGN KEY (<column-name>) REFERENCES <rederenced-table-name>(<referenced-column-name>) ON DELETE SET NULL" to connect related tables. The following tables are related with each other: Orders and Customers, OrderItems and Orders, OrderItems and Products.

#### How test yourself 
Just in case you want to test your script on your own DB before submitting a PR, you can do it by performing the following actions: 
1. Run the script you wrote in the "task.sql" against your database server 
2. Make sure all tables in the database it created are empty 
3. Run script "test.sql" against your database. If the sctip execution finished without errors - you are ready to submit a PR. 
