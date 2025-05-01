# 📊 E-commerce Sales Data Analysis using MySQL & Python

This project demonstrates how to connect Jupyter Notebook to a MySQL database to analyze e-commerce sales data. It involves running SQL queries and visualizing the results using Python libraries such as Pandas and Matplotlib.

## Technologies Used

- **Python (Jupyter Notebook)**
- **MySQL**
- **SQLAlchemy & PyMySQL** (for database connection)
- **Pandas**
- **Matplotlib**

##  Database Information

Connected to a MySQL database named `ecommerce` with a table `sales_data` containing:

- `id`: Customer ID  
- `name`: Customer Name  
- `buydate`: Date of Purchase  
- `productname`: Product Category  
- `sales`: Sale Amount

---

##  Visualizations Included

1. **Sales Over Time**  
   - Line graph showing total sales on each date.
   
2. **Sales by Product Category**  
   - Bar chart representing total sales for each product type.
   
3. **Sales by Customer**  
   - Bar chart showing how much each customer spent.

# Interview Questions

# 📌 Interview Questions and Answers

# 1. How did you connect Python to a database?
 ➤ I used SQLAlchemy and PyMySQL to connect to a MySQL database.
 Example:
 from sqlalchemy import create_engine
 engine = create_engine("mysql+pymysql://username:password@localhost:3306/database")
 connection = engine.connect()

# 2. What SQL query did you run?
 ➤ I ran queries like:
 SELECT productname, SUM(sales) AS sales FROM sales_data GROUP BY productname;

# 3. What does GROUP BY do?
 ➤ GROUP BY groups rows with the same value in a column, allowing aggregate functions 
 like SUM() or COUNT() to be applied to each group.

# 4. How did you calculate revenue?
 ➤ I used the SUM() function on the 'sales' column.
 For example:
 SELECT SUM(sales) AS total_revenue FROM sales_data;

# 5. How did you visualize the result?
 ➤ I used Matplotlib to plot line and bar charts.
 Example:
 df.plot(kind='bar', x='productname', y='sales')

# 6. What does pandas do in your code?
 ➤ Pandas is used to execute SQL queries and convert the result into DataFrames 
 for analysis and visualization.

# 7. What’s the benefit of using SQL inside Python?
 ➤ It allows combining SQL's power for data extraction with Python’s processing, 
 automation, and visualization capabilities — useful for end-to-end analysis.

# 8. Could you run the same SQL query directly in DB Browser for SQLite?
 ➤ Yes, the core SQL query would work with small syntax changes. But the connection and 
 data handling are different. SQLite doesn't support all MySQL features, but basic 
 queries like SELECT, GROUP BY, and SUM will work fine.
