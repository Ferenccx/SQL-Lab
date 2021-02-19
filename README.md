# SQL-Lab

1. Select all the records from the "Customer" Table
SELECT * FROM Customers

2. Select distinct countries from the "Customer" Table

SELECT DISTINCT Country FROM Customers

3. Get all the records from the table Customers where the Customer’s ID starts with “BL”.
SELECT * FROM Customers
WHERE customer_id = 'BL';

4. Get the first 100 records of the orders table.

SELECT * FROM Customers
LIMIT 100;


5. Get all customers that live in the postal codes 1010, 3012, 12209, and 05023.
SELECT * FROM Customers
WHERE postal_code in ('1010', '3012', '12209', '05023');

6. Get all orders where the ShipRegion is not equal to NULL.
SELECT * FROM Customers
WHERE region <> null;


7. Get all customers ordered by the country, then by the city.
SELECT * FROM Customers
ORDER BY Country;

8. Add a new customer to the customers table. You can use whatever values/
INSERT INTO customers (customer) values ('VINNIE');


9. Update all ShipRegion to the value ‘EuroZone’ in the Orders table, where the

ShipCountry is equal to France.

10. Delete all orders from `order_details` that have a quantity of 1.
DELETE FROM  Customers
WHERE  quantity = '1';

11. Calculate the average, max, and min of the quantity at the `order details` table.

SELECT AVG(Quantity)
FROM Orders_Details;

12. Calculate the average, max, and min of the quantity at the `order details` table,
grouped by the orderid.

13. Find the CustomerID that placed order 10290 (orders table)

SELECT * FROM Orders WHERE Order_ID = 10290;

14. Do an inner join, left join, right join on orders and customers tables. (These are three
separate queries, one for each type of join.)

SELECT Orders
FROM Customers
INNER JOIN Customers ON Orders = Customers;


15. Use a join to get the ship city and ship country of all the orders which are associated
with an employee who is in London.

SELECT ship_name FROM orders
INNER JOIN 
	order_details 
	ON 
	orders.order_id = order_details.order_id
INNER JOIN
	products 
	ON 
	products.product_id = order_details.product_id
WHERE discontinued = 1;

16. Use a join to get the ship name of all orders that include a discontinued product. (See
orders, order_details, and products. 1 means discontinued.)

SELECT * FROM orders;
SELECT * FROM order_details;
SELECT * FROM products WHERE discontinued = 1;

17. Get first names of all employees who report to no one.

SELECT * FROM employees WHERE reports_to IS NULL;

18. Get first names of all employees who report to Andrew.
