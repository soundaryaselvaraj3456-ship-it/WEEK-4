# ** WEEK-4 Order Management System**

## **Project Overview**

The **Order Management System** is an e-commerce database project developed using MySQL. It helps manage customer orders, products, quantities, prices, inventory, and order status efficiently.

## **Objectives**

* Create and manage customer orders.
* Add multiple products to a single order.
* Store product quantities and prices.
* Calculate the total order amount.
* Update order status.
* Delete cancelled orders.
* View customer order history.
* Generate sales and purchase reports.

## **Tables Used**

### **1. Customer**

Stores customer information such as Customer ID, Name, Email, and Address.

### **2. Product**

Stores product information such as Product ID, Product Name, Price, and Category.

### **3. Orders**

Stores the main order information.

* Order_ID
* Customer_ID
* Order_Date
* Total_Amount
* Order_Status

### **4. Order_Details**

Stores the products included in each order.

* Order_Detail_ID
* Order_ID
* Product_ID
* Quantity
* Price

### **5. Inventory**

Stores product stock information and available quantities.

## **Relationships**

* **Customer → Orders:** One customer can place multiple orders.
* **Orders → Order_Details:** One order can contain multiple products.
* **Product → Order_Details:** One product can appear in multiple orders.
* **Product → Inventory:** Inventory tracks the available stock of products.

## **Constraints Used**

* **PRIMARY KEY:** Uniquely identifies each record.
* **FOREIGN KEY:** Establishes relationships between tables.
* **NOT NULL:** Prevents required columns from containing NULL values.
* **CHECK:** Ensures that values satisfy specified conditions.

### **Example Constraints**

```sql
CHECK (Quantity > 0);
CHECK (Total_Amount >= 0);
```

## **Main Operations**

### **1. INSERT**

Adds new customers, products, and orders to the database.

### **2. UPDATE**

Updates order status, product prices, and quantities when required.

### **3. DELETE**

Deletes cancelled orders while maintaining referential integrity.

### **4. SELECT**

Retrieves customer details, order information, and product records.

### **5. REPORTS**

Generates reports such as:

* Customer Order History
* Product-wise Order Report
* Total Sales Report
* Customer Purchase Analysis
* Inventory Stock Report

## **Example Order**

| Order ID | Customer | Product | Quantity |
| -------- | -------- | ------- | -------- |
| 5001     | Rahul    | Laptop  | 1        |
| 5001     | Rahul    | Mouse   | 2        |

## **Technologies Used**

* MySQL
* SQL
* MySQL Workbench
* GitHub

## **Advantages**

* Organizes customer and order information.
* Supports multiple products in a single order.
* Maintains product and inventory records.
* Reduces data duplication through relational tables.
* Simplifies order tracking and sales reporting.

## **Conclusion**

The **Order Management System** provides an efficient way to manage customer orders, products, inventory, quantities, prices, and order statuses. It demonstrates the practical use of SQL queries, relational database design, primary keys, foreign keys, and constraints in an e-commerce application.
