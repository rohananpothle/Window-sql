# Window-sql

# SQL Window Functions – RAD (Role Activity Document)

## Role
**Data Analyst**

## Activity
Understanding and using **SQL Window Functions** for real-time analytical use cases without losing row-level data.

---

## 1. What is a Window Function?

A **Window Function** performs calculations across a set of rows related to the current row **without collapsing the result set**.

### Key Difference

| GROUP BY | Window Function |
|--------|----------------|
| Collapses rows | Keeps all rows |
| Summary only | Summary + detail |
| Limited analytics | Advanced analytics |

---

## 2. Sample Dataset

### Table Structure

```sql
CREATE TABLE sales (
    order_id INT,
    emp_name VARCHAR(20),
    department VARCHAR(20),
    order_date DATE,
    sales_amount INT
);

