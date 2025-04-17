# Apply Filters to SQL Queries – Portfolio Activity

## Project Description
In this project, I used SQL to examine login activity and employee records for a simulated cybersecurity scenario. Using logical and pattern-matching operators like `AND`, `OR`, `NOT`, and `LIKE`, I retrieved relevant data from relational tables. These queries demonstrate how SQL supports threat investigation, anomaly detection, and system auditing within an enterprise environment.

---

## Retrieve After Hours Failed Login Attempts

**Query:**
```sql
SELECT count(*) FROM log_in_attempts WHERE login_time > '18:00:00' AND success = 0;
```

**Explanation:**  
This query filters login attempts that occurred after 6:00 PM (`login_time > '18:00:00'`) and were unsuccessful (`success = 0`). It helps identify potentially suspicious activity after business hours.

**Result:**  
```
count(*)
19
```

---

## Retrieve Login Attempts on Specific Dates

**Query:**
```sql
SELECT count(*) FROM log_in_attempts WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```

**Explanation:**  
This query retrieves all login attempts on May 8 and May 9, 2022. The `OR` operator allows the inclusion of both dates.

**Result:**  
```
count(*)
75
```

---

## Retrieve Login Attempts Outside of Mexico

**Query:**
```sql
SELECT count(*) FROM log_in_attempts WHERE country NOT LIKE 'MEX%';
```

**Explanation:**  
This query excludes any login attempts originating from entries beginning with "MEX", such as MEX or MEXICO, using the `NOT LIKE` operator and wildcard `%`.

**Result:**  
```
count(*)
144
```

---

## Retrieve Employees in Marketing

**Query:**
```sql
SELECT * FROM employees WHERE department LIKE 'Marketing' AND office LIKE 'E%';
```

**Explanation:**  
This query returns all employees in the `Marketing` department who work in office locations that begin with "E" (e.g., East-170). The query uses `LIKE 'E%'` to match any East office, useful for location-specific updates.

**Result:**

| employee_id | device_id      | username | department | office   |
|-------------|----------------|----------|------------|----------|
| 1000        | a320b137c219   | elarson  | Marketing  | East-170 |
| 1052        | a192b174c940   | jdarosa  | Marketing  | East-195 |
| 1075        | x573y883z772   | fbautist | Marketing  | East-267 |
| 1088        | k865l965m233   | rgosh    | Marketing  | East-157 |
| 1103        | NULL           | randerss | Marketing  | East-460 |
| 1156        | a184b775c707   | dellery  | Marketing  | East-417 |
| 1163        | h679i515j539   | cwilliam | Marketing  | East-216 |

---

## Retrieve Employees in Finance or Sales

**Query:**
```sql
SELECT * FROM employees WHERE department LIKE 'Finance' OR department LIKE 'Sales' LIMIT 4;
```

**Explanation:**  
This query returns the first four employees who are in either the `Finance` or `Sales` department using the `OR` operator. Useful for department-specific device patching or analysis.

**Result:**

| employee_id | device_id      | username | department | office    |
|-------------|----------------|----------|------------|-----------|
| 1003        | d394e816f943   | sgilmore | Finance    | South-153 |
| 1007        | h174i497j413   | wjaffrey | Finance    | North-406 |
| 1008        | i858j583k571   | abernard | Finance    | South-170 |
| 1009        | NULL           | lrodriqu | Sales      | South-134 |

---

## Retrieve All Employees Not in IT

**Query:**
```sql
SELECT count(*) FROM employees WHERE department NOT LIKE 'Information Technology';
```

**Explanation:**  
This query returns a count of all employees whose departments are not labeled as `Information Technology`, using the `NOT LIKE` operator. This supports exclusion-based updates for departments that have not yet received them.

**Result:**  
```
count(*)
161
```

---

## Summary

In this activity, I used SQL to extract and analyze security-related data across employee and login datasets. I applied logical operators (`AND`, `OR`, `NOT`) and pattern-matching techniques (`LIKE`, `%`) to retrieve data under various business constraints. This experience showcases my ability to filter large datasets and perform targeted queries, skills essential to cybersecurity data analysis and auditing.

---

## SQL Techniques Demonstrated

- `LIKE` with wildcard (`%`) to match partial patterns (e.g., office or country codes).
- Date and time filtering using `login_date` and `login_time`.
- Logical operators `AND`, `OR`, `NOT` for multi-condition filtering.
- Query exclusions using `NOT LIKE`.
