+ w3c sql보기
+ erp 그려보기

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
  - SELECT * FROM Customers ORDER BY City DESC(있으면 내림차순 없으면 오름차순)
  - SELECT * FROM Customers ORDER BY Country ASC, City DESC 테이블마다 각각 다르게 할수 있음
- **UPDATE** - updates data in a database
- **DELETE** - deletes data from a database
- **INSERT INTO** - inserts new data into a database
- **CREATE DATABASE** - creates a new database
- **ALTER DATABASE** - modifies a database
- **CREATE TABLE** - creates a new table
- **ALTER TABLE** - modifies a table
- **DROP TABLE** - deletes a table
- **CREATE INDEX** - creates an index (search key)
- **DROP INDEX** - deletes an index