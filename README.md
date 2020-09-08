# shopify-data-intern 

Question 1 code and answers located in R markdown file. Refer to comments 

Question 2 SQL queries and numeric answers below: 

  2a. select count(OrderID) from Orders a, Shippers b where a.shipperID = b.shipperID and b.ShipperName = 'Speedy Express'
      Answer: 54 orders 
  
  2b. SELECT count(OrderID), b.lastname, a.EmployeeID from Orders a, Employees b where a.EmployeeID = b.EmployeeID group by a.EmployeeID Order by count(OrderID)         desc
      Answer: Peacock with 40 orders 
          (last name is Peacock) 
          
   2c. SELECT count(ord.OrderID), prod.productName FROM OrderDetails ordt, Orders ord, Products prod, Customers cust where prod.ProductID = ordt.ProductID and            ordt.OrderID = ord.OrderID and ord.customerID = cust.CustomerID and cust.Country = 'Germany' group by prod.productName order by count(ord.OrderID) desc
       Answer: 5 orders of Gorgonzola Telino


