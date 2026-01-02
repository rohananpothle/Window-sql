# Window-sql Questions

# SQL Window Functions

---

### Scenario 1: The VIP List (Ranking)
**Business Need:** The marketing team wants to send a "Thank You" gift to the **top 3 customers in each country** based on their total purchase amount.
**Task:** * Write a query that shows the Country, Customer Name, and Total Spent.
* Filter the results to show only the top 3 per country. 
* If two people have the same spend, they should receive the same rank.

### Scenario 2: Growth Metrics (Offset)
**Business Need:** The CFO needs to see if the company’s revenue is growing. They require a report showing total revenue for each month and the **percentage change** compared to the previous month.
**Task:** * Calculate the Monthly Revenue.
* Use a window function to retrieve the previous month’s revenue to calculate the MoM (Month-over-Month) growth rate.

### Scenario 3: Salary Benchmarking (Aggregates)
**Business Need:** HR wants to ensure fair pay across the organization. They need a list of all employees that includes their Name, Department, Salary, and the **Average Salary of their specific department** for comparison.
**Task:** * Create a result set where every employee row displays the average salary of their department.
* **Constraint:** Do not use a `GROUP BY` clause that collapses individual employee records.

### Scenario 4: Inventory Tracking (Running Totals)
**Business Need:** The warehouse manager needs to track stock levels. We have a table of "Stock In" (positive numbers) and "Stock Out" (negative numbers) events sorted by time.
**Task:** * Create a query that shows a **Running Total** of inventory over time. 
* Add a column to flag any row where the running total drops below zero (indicating a data error).

### Scenario 5: Customer Lifecycle (Extremes)
**Business Need:** To understand customer retention, we need to see the "Bookend" dates for every customer.
**Task:** * For every order in the database, include two additional columns:
    1. The date of that customer's **very first purchase**.
    2. The date of that customer's **most recent purchase**.
* Ensure these dates appear on every row associated with that customer.

