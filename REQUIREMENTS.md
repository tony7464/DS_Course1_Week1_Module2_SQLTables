# Requirements Checklist: 44953 Lab: SQL Table Relations

Source: Canvas description + rubric (latest_assignments.json), plus the starter notebook/repo instructions.

Deliverable: `SQLJoinsSubQueriesLab.ipynb`

| # | Requirement (explicit or implied) | Rubric criterion | How it's met | Status |
|---|---|---|---|---|
| 1 | Step 1: Boston employees first/last/jobTitle (JOIN + WHERE) | Join and Filter | `df_boston` (2 rows) | ✅ |
| 2 | Step 2: offices with zero employees (LEFT JOIN + HAVING) | Join and Filter (HAVING, aggregate) | `df_zero_emp` -> empty, i.e. no ghost offices | ✅ |
| 3 | Step 3: all employees + office city/state, ordered first then last name (LEFT JOIN) | Type of Join | `df_employee` | ✅ |
| 4 | Step 4: customers with no orders, contact first/last/phone/salesRep, sorted by contact last name (24 rows) | Type of Join | `df_contacts` LEFT JOIN ... IS NULL, 24 rows | ✅ |
| 5 | Step 5: contacts + payment amount/date sorted by amount DESC, CAST amount | Built-in Function (CAST) | `df_payment` ORDER BY CAST(amount AS REAL) DESC | ✅ |
| 6 | Step 6: 4 reps with avg customer credit > 90k, sorted by num customers | Joining and Grouping (HAVING, ORDER BY) | `df_credit` 4 rows | ✅ |
| 7 | Step 7: productName, numorders, totalunits sorted by totalunits | Joining and Grouping | `df_product_sold` | ✅ |
| 8 | Step 8: productName, productCode, numpurchasers (DISTINCT, 3 tables) | Multiple Joins | `df_total_customers` | ✅ |
| 9 | Step 9: n_customers per office with officeCode, city | Multiple Joins | `df_customers` | ✅ |
| 10 | Step 10: employees who sold products bought by <20 customers, subquery on productCode in WHERE, sorted by lastName | Subquery | `df_under_20` (15 employees) | ✅ |
| 11 | Executes top to bottom | AutoTests | nbconvert --execute passed | ✅ |
