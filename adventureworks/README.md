# Introduction to Adventure Works OLTP DB
AdventureWorks Database is a Microsoft product sample for an online transaction processing (OLTP) database. The AdventureWorks Database supports a fictitious, multinational manufacturing company called Adventure Works Cycles.
You can view the database ER Diagram [here](https://cursos.virtual.uniandes.edu.co/isis3301/wp-content/uploads/sites/208/2019/08/adventureworks.pdf), or look through this interactive [schema](https://dataedo.com/samples/html/AdventureWorks/doc/AdventureWorks_2/tables.html)

## Scenario
Adventure Works Cycles, the fictitious company on which the AdventureWorks sample databases are based, is a large, multinational manufacturing company. The company manufactures and sells metal and composite bicycles to North American, European and Asian commercial markets. While its base operation is located in Bothell, Washington with 290 employees, several regional sales teams are located throughout their market base.

In 2000, Adventure Works Cycles bought a small manufacturing plant, Importadores Neptuno, located in Mexico. Importadores Neptuno manufactures several critical subcomponents for the Adventure Works Cycles product line. These subcomponents are shipped to the Bothell location for final product assembly. In 2001, Importadores Neptuno, became the sole manufacturer and distributor of the touring bicycle product group.

Coming off a successful fiscal year, Adventure Works Cycles is looking to broaden its market share by targeting their sales to their best customers, extending their product availability through an external Web site, and reducing their cost of sales through lower production costs.

# Practice Questions
1.  Write a SELECT statement that lists the customers along with their ID numbers. Include the last names, first names, and company names. 
2.  Write a SELECT statement that lists the name, product number, and color of each product. 
3.  Write a SELECT statement that lists the customer ID numbers and sales order ID numbers from the Sales.SalesOrderHeader table.

# Filtering Data 
1. Write a query using a WHERE clause that displays all the employees listed in the
HumanResources.Employee table who have the job title Research and Development Engineer.
Display the business entity ID number, the login ID, and the title for each one. 

2. Write a query using a WHERE clause that displays all the names in Person.Person with the middle
name J. Display the first, last, and middle names along with the ID numbers. 

#  Sorting Data 
1. Write a query that returns the business entity ID and name columns from the Person.Person
table. Sort the results by LastName, FirstName, and MiddleName. 

2. Write a query that displays all the rows from the Person.Person table where the rows were
modified after December 29, 2000. Display the business entity ID number, the name columns,
and the modified date. 

3. Write a query displaying the order ID, order date, and total due from the Sales.SalesOrderHeader
table. Retrieve only those rows where the order was placed during the month of September 2001
and the total due exceeded $1,000.

# Working With NULLs
1.  Write a query displaying the ProductID, Name, and Color columns from rows in the
Production.Product table. Display only those rows where no color has been assigned. 

2. Write a query displaying the ProductID, Name, and Color columns from rows in the
Production.Product table. Display only those rows in which the color is not blue. 

3. Write a query displaying ProductID, Name, Style, Size, and Color from the Production.Product
table. Include only those rows where at least one of the Style, Size, or Color columns contains
a value.  

# Using Mathematical Operators 
1. Write a query using the Sales.SpecialOffer table. Display the difference between the MinQty and
MaxQty columns along with the SpecialOfferID and Description columns. 

2. Write a query using the Sales.SpecialOffer table. Multiply the MinQty column by the DiscountPct
column. Include the SpecialOfferID and Description columns in the results. 

3. Write a query using the Sales.SpecialOffer table that multiplies the MaxQty column by the
DiscountPCT column. If the MaxQty value is null, replace it with the value 10. Include the
SpecialOfferID and Description columns in the results. 

# Using String Functions 
1. Write a query displaying the first name and last name from the Person.Person table all in
uppercase. 

# Using Date Functions 
2. Write a query that displays the year of each order date and the numeric month of each order date
in separate columns in the results. Include the SalesOrderID and OrderDate columns. 

3. Write a query that calculates the number of days between the date an order was placed and the
date that it was shipped using the Sales.SalesOrderHeader table. Include the SalesOrderID,
OrderDate, and ShipDate columns. 

4. Write a query that displays only the date, not the time, for the order date and ship date in the
Sales.SalesOrderHeader table. 

5.  Write a query that adds six months to each order date in the Sales.SalesOrderHeader table.
Include the SalesOrderID and OrderDate columns. 


# Joins
## Inner Joins
1. The HumanResources.Employee table does not contain the employee names. Join that table to the
Person.Person table on the BusinessEntityID column. Display the job title, birth date, first name,
and last name.

2. The customer names also appear in the Person.Person table. Join the Sales.Customer table to the
Person.Person table. The BusinessEntityID column in the Person.Person table matches the
PersonID column in the Sales.Customer table. Display the CustomerID, StoreID, and TerritoryID
columns along with the name columns. 

4. Write a query that joins the Sales.SalesOrderHeader table to the Sales.
SalesPerson table. Join the BusinessEntityID column from the Sales.SalesPerson table to the
SalesPersonID column in the Sales.SalesOrderHeader table. Display the SalesOrderID along with
the SalesQuota and Bonus. 

5. The catalog description for each product is stored in the Production.ProductModel table. Display
the columns that describe the product from the Production.Product table, such as the color and
size along with the catalog description for each product. 

6. Write a query that displays the names of the customers along with the product names that they
have purchased. Hint - Five tables will be required to write this query! 


## Outer Joins
1. Write a query that displays all the products along with the SalesOrderID even if an order has never
been placed for that product. Join to the Sales.SalesOrderDetail table using the ProductID
column. 

2. Change the query written in question 1 so that only products that have not been ordered show up
in the query. 

3.  Write a query that returns all the rows from the Sales.SalesPerson table joined to the
Sales.SalesOrderHeader table along with the SalesOrderID column even if no orders match.
Include the SalesPersonID and SalesYTD columns in the results. 

4. Change the query written in question 3 so that the salesperson’s name also displays from the
Person.Person table.

5.  The Sales.SalesOrderHeader table contains foreign keys to the Sales.CurrencyRate and
Purchasing.ShipMethod tables. Write a query joining all three tables, making sure it contains all
rows from Sales.SalesOrderHeader. Include the CurrencyRateID, AverageRate, SalesOrderID, and
ShipBase columns. 

# Summarizing Data 
Aggregating Data:
1.  Write a query to determine the price of the most expensive product ordered. Use the UnitPrice
column of the Sales.SalesOrderDetail table. 

2.  Write a query to determine the average freight amount in the Sales.SalesOrderHeader table. 

3. Write a query using the Production.Product table that lists a count of the products in each
product line. 

4. Write a query that displays the count of orders placed by year for each customer using the
Sales.SalesOrderHeader table.

5.  Write a query joining the Person.Person, Sales.Customer, and Sales.SalesOrderHeader tables to
return a list of the customer names along with a count of the orders placed

6. Write a query using the Sales.SalesOrderHeader, Sales.SalesOrderDetail, and
Production.Product tables to display the total sum of products by ProductID and OrderDate. 


# Having Clause
1.   Write a query that creates a sum of the LineTotal in the Sales.SalesOrderDetail table grouped by
the SalesOrderID. Include only those rows where the sum exceeds 1,000. 

2. Write a query that groups the products by ProductModelID along with a count. Display the rows
that have a count that equals 1. 


# Subqueries
1.  Using a subquery, display the product names and product ID numbers from the
Production.Product table that have been ordered. 

2. Write a query that displays the colors used in the Production.Product table that are not listed in
the Production.ProductColor table using a subquery. Use the keyword DISTINCT before the
column name to return each color only once. 


# Derived Tables and Common Table Expressions
1.  Using a derived table, join the Sales.SalesOrderHeader table to the Sales.SalesOrderDetail table.
Display the SalesOrderID, OrderDate, and ProductID columns in the results. The
Sales.SalesOrderDetail table should be inside the derived table query. 

2. Rewrite the query in question 1 with a common table expression. 

3. Write a query that displays all customers along with the orders placed in 2001. Use a common
table expression to write the query and include the CustomerID, SalesOrderID, and OrderDate
columns in the results. 


### Question Bank: 
- [pdf solutions](https://link.springer.com/content/pdf/bbm%3A978-1-4302-2462-4%2F1.pdf)
- unused right now but available [questions](https://www.sqlcourse.com/select.html)
