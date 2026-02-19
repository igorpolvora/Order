# 📦 Order Processing System 

## 📌 Project Overview

**Order** is a Java console application that simulates a simple order processing system.
The application allows users to:

* Register a client
* Create an order with multiple items
* Track order status
* Calculate total order value
* Display detailed order summary

This project reinforces core Java and Object-Oriented Programming concepts such as:

* Classes and objects
* Encapsulation
* Enum usage
* Composition
* Collections (`ArrayList`)
* Date and time handling
* Input and output formatting

---

## 🛠️ Technologies Used

* Java (JDK 8+)
* Standard libraries (`java.util`, `java.text`)
* No external dependencies or frameworks

---

## 📂 Project Structure

```
Order/
├── src/
│   ├── application/
│   │   └── Program.java
│   ├── entities/
│   │   ├── Client.java
│   │   ├── Order.java
│   │   ├── Product.java
│   │   └── OrderItem.java
│   └── entities/enums/
│       └── OrderStatus.java
├── .gitignore
├── README.md
```

---

## 🎯 Features

### 🧑‍💼 Client Registration

The user is prompted to enter:

* Client name
* Email
* Birth date

### 📦 Order Creation

The application allows:

* Order status selection (`PENDING_PAYMENT`, `PROCESSING`, `SHIPPED`, `DELIVERED`)
* Input of multiple items
* Each item includes:

  * Product name
  * Price
  * Quantity

### 💰 Total Price Calculation

The system calculates:

```
total = sum(quantity × productPrice)
```

for all order items.

### 📇 Order Summary

Generates a formatted summary of:

* Order moment (timestamp)
* Order status
* Client data
* List of Ordered Items
* Total price

---

## 🧠 Technical Concepts

### 📌 Enum Usage

```java
OrderStatus status;
```

Enums are used to define a predefined set of valid states for order status.

### 📌 Composition

* An order contains *order items*
* Each order item references a *product*
* A client is associated with an order

### 📌 Collections

`ArrayList<OrderItem>` is used to manage the dynamic list of ordered items.

---

## 📋 Example Input / Output

```
Enter client data:
Name: Alex Green
Email: alex@gmail.com
Birth date (DD/MM/YYYY): 15/03/1985

Enter order data:
Status: PROCESSING
How many items to this order? 2

Enter #1 item data:
Product name: TV
Product price: 1000.00
Quantity: 1

Enter #2 item data:
Product name: Mouse
Product price: 40.00
Quantity: 2
```

### Output:

```
ORDER SUMMARY:
Order moment: 20/04/2026 15:42:15
Order status: PROCESSING
Client: Alex Green (15/03/1985) – alex@gmail.com
Order items:
TV, $1000.00, Quantity: 1, Subtotal: $1000.00
Mouse, $40.00, Quantity: 2, Subtotal: $80.00
Total price: $1080.00
```

---

## 🧩 Calculation Rules

* Subtotal = price × quantity
* Total = sum of all item subtotals
* Order date/time is captured at runtime

---

## 🚀 Possible Enhancements

Future improvements may include:

* Adding input validation and error handling
* Storing orders in memory or a file
* Implementing a user interface (GUI/web)
* Adding discount/promotion mechanisms
* Persisting data using databases

---

## 📚 Educational Purpose

This project is intended for learning and practicing:

* Core Java programming
* Object-oriented design
* Use of enums and collections
* Modular project organization

---

## 👨‍💻 Author

Developed by **Igor Polvora** as part of Java learning and practice exercises.
