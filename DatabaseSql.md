## SQL

- **SELECT** - extracts data from a database
  
  - SELECT * FROM Customers;
  - SELECT Address, Country FROM Customers;
  - SELECT DISTINCT Country FROM Customers;
  - SELECT COUNT(DISTINCT Country) FROM Customers;
  - SELECT * FROM Customers
    WHERE Country='Mexico' AND CustomerID <= 20; 
  - SELECT CustomerID, Country, City FROM Customers
    WHERE Country='Germany' OR City='Berlin';
  - SELECT CustomerID, Country, City FROM Customers
    WHERE NOT Country='Germany'
  - SELECT CustomerID, Country, City FROM Customers
    WHERE Country='Germany' AND (City='Berlin' OR City='München') AND NOT CustomerID=1;
  - SELECT * FROM Customers 
    ORDER BY City DESC(있으면 내림차순 없으면 오름차순)
  - SELECT * FROM Customers 
    ORDER BY Country ASC, City DESC 
  
- **UPDATE** - updates data in a database

  - UPDATE Customers SET ContactName='Alfred Schmidt', City='Frankfurt'
    WHERE CustomerID=1;
  - UPDATE Customers SET City = "Korea" 
    WHERE CustomerID <= 10;

  > *Be careful when updating records. If you omit the WHERE clause, all records are updated!*

- **DELETE** - deletes data from a database

- **INSERT INTO** - inserts new data into a database

  - INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
    VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');

- **CREATE DATABASE** - creates a new database

- **ALTER DATABASE** - modifies a database

- **CREATE TABLE** - creates a new table

- **ALTER TABLE** - modifies a table

- **DROP TABLE** - deletes a table

- **CREATE INDEX** - creates an index (search key)

- **DROP INDEX** - deletes an index





+ **IS NULL** - Test with null value
  + SELECT * FROM Customers 
    WHERE Address IS NULL;
  + SELECT * FROM Customers 
    WHERE Address IS NOT NULL;