# SQL-Project

# 📚 Online Bookstore – SQL Project (PostgreSQL)

Welcome to the **Online Bookstore SQL Project**!

This project simulates a simple online bookstore using **PostgreSQL**. It covers everything from creating the database and tables to importing data and writing a variety of SQL queries—both basic and advanced.

The goal was to build a hands-on project to practice real-world SQL skills and explore how SQL can be used to analyze book sales, customer behavior, and inventory.

---

## 🚀 About the Project

This project focuses on applying core SQL concepts like:

- Database schema design
- Data import using the `COPY` command
- Writing queries with `WHERE`, `GROUP BY`, `HAVING`, and `ORDER BY`
- Using `JOIN` operations across tables
- Real-world business logic (e.g., stock management, top customers, sales revenue)

Whether you're a beginner or brushing up on your SQL, this project offers a solid playground to explore relational database design and querying.

---

## 🧱 Database Structure

The database is called `OnlineBookstore` and has three main tables:

### 🗃️ `Books`
Stores information about each book in the store.

| Column        | Type          | Description             |
|---------------|---------------|-------------------------|
| Book_ID       | SERIAL (PK)   | Unique ID for each book |
| Title         | VARCHAR(100)  | Title of the book       |
| Author        | VARCHAR(100)  | Book's author           |
| Genre         | VARCHAR(50)   | Genre (e.g., Fiction)   |
| Published_Year| INT           | Year of publication     |
| Price         | NUMERIC(10,2) | Price of the book       |
| Stock         | INT           | Number of books in stock|

---

### 🧑‍🤝‍🧑 `Customers`
Contains details about customers who’ve placed orders.

| Column      | Type         | Description              |
|-------------|--------------|--------------------------|
| Customer_ID | SERIAL (PK)  | Unique customer ID       |
| Name        | VARCHAR(100) | Full name                |
| Email       | VARCHAR(100) | Contact email            |
| Phone       | VARCHAR(15)  | Phone number             |
| City        | VARCHAR(50)  | City                     |
| Country     | VARCHAR(150) | Country                  |

---

### 🧾 `Orders`
Tracks book purchases made by customers.

| Column       | Type          | Description               |
|--------------|---------------|---------------------------|
| Order_ID     | SERIAL (PK)   | Unique order ID           |
| Customer_ID  | INT (FK)      | References `Customers`    |
| Book_ID      | INT (FK)      | References `Books`        |
| Order_Date   | DATE          | Date the order was placed |
| Quantity     | INT           | Number of books ordered   |
| Total_Amount | NUMERIC(10,2) | Total price for the order |

---

## 📥 Data Import

The data is imported from three CSV files using PostgreSQL's `COPY` command.

You’ll need to adjust the file paths in the SQL script to match where your `.csv` files are located. Example:
```sql
COPY Books(Book_ID, Title, Author, Genre, Published_Year, Price, Stock) 
FROM 'D:\\Path\\To\\Books.csv' CSV HEADER;


🎯 What You’ll Learn
How to structure a real relational database

Writing optimized queries using PostgreSQL syntax

Analyzing sales, customer behavior, and stock levels

Building query logic that reflects business scenarios

Using SQL for simple reporting and insights

🛠️ How to Run the Project
Create a new PostgreSQL database: OnlineBookstore

Run the provided SQL script in a PostgreSQL client like pgAdmin or DBeaver.

Modify file paths in COPY statements to match your machine.

Start running and modifying queries!

📁 Files Included
SQL Project Solutions.sql – Full SQL script with schema + queries

(Dummy Data) You can use dummy data 

🔮 Future Ideas
Add views and stored procedures for reuse

Generate reports using tools like Power BI or Tableau

Visualize customer and sales analytics

Write unit tests for each SQL logic block

🙋‍♂️ Final Note
This project was created to blend learning with something realistic and practical. If you're getting into SQL or PostgreSQL, feel free to fork it, experiment with the queries, or even turn it into a mini-app.
