# SQL Data Mismatch Investigation

## Summary
A user reported that the API returned incorrect account information for a record.

## Issue
The application displayed data that did not match the expected customer record.

## Investigation Goal
Determine whether the issue came from:
- incorrect data stored in the database
- incorrect filtering/query logic
- mismatched IDs between systems

## Example Query Used
```sql
SELECT id, name, email, status
FROM customers
WHERE id = 101;

##Follow-up Query
SELECT id, customer_id, order_total, created_at
FROM orders
WHERE customer_id = 101;

##Findings
Customer record existed
Related order data was associated with the correct customer_id
The mismatch suggested the application may have been referencing the wrong field or mapping the wrong response data

##Root Cause
Potential data mapping issue between the application layer and the underlying database query results.

##Resolution
Escalated for engineering review, documenting expected vs. actual output and the SQL checks performed.

