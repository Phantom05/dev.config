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

  - DELETE FROM Customers WHERE CustomerName='Alfreds Futterkiste';

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



+ **LIKE** - Used to search for the specified pattern.
  - SELECT * FROM Products WHERE ProductName LIKE '%s'
  - SELECT * FROM Products WHERE ProductName LIKE '_h%'
  - SELECT * FROM Customers
    WHERE CustomerName LIKE '%Hungry%';
  - SELECT * FROM Customers
    WHERE CustomerName LIKE 'a__%'; (a로 시작하는 3글자)
  - SELECT * FROM Customers
    WHERE ContactName LIKE 'a%o';
  - SELECT * FROM Customers
    WHERE CustomerName NOT LIKE 'a%';
  - SELECT * FROM Customers WHERE ContactName LIKE 'a%' OR  ContactName LIKE 'b%'  OR  ContactName LIKE 'c%'
+ **IN** - Put multiple conditions in the where statement.
  - SELECT * FROM Customers
    WHERE Country IN ('Germany','UK');
  - SELECT * FROM Customers
    WHERE Country IN (SELECT Country FROM Suppliers LIMIT 3);
  - SELECT * FROM Customers
    WHERE Country IN (SELECT DISTINCT Country FROM Suppliers WHERE Country IN ('UK','USA'));

+ **LIMIT** - Test with null value
  + SELECT * FROM Customers LIMIT 3;
  + SELECT * FROM Customers
    WHERE Country='Germany'
    LIMIT 5;
+ **MIN & MAX** - Find the maximum and minimum value.
  - SELECT MIN(Price) AS SmallestPrice
    FROM Products; 
+ **AVG** - Find the average value.
  - SELECT AVG(Price) AS AveragePrice
    FROM Products;

+ **IS NULL** - Test with null value
  + SELECT * FROM Customers 
    WHERE Address IS NULL;
  + SELECT * FROM Customers 
    WHERE Address IS NOT NULL;