---
Title: "What is a Database Index?"
Subjects:
  - "Computer Science"
  - "Data Science"
Tags:
  - "Database"
  - "Queries"
  - "Primary Key"
  - "Foreign Key"
  - "Index"
Catalog Content:
  - "https://www.codecademy.com/learn/paths/design-databases-with-postgresql"
  - "https://www.codecademy.com/learn/paths/analyze-data-with-sql"
  - "https://www.codecademy.com/learn/paths/data-science"
---

A database index is a data structure that improves the speed of data retrieval in the database. 
Indexes on a table consist of one or more columns of ordered data with links back to specific rows in a table. 

By matching the values in the index, the database management system can quickly retrieve the corresponding row without having to search every row in the table.
Tables are indexed on their primary key columns, and many database systems require an index on a foreign key column as well.
During database design indexes are typically also placed on columns that will be most often queried on.

## Example

Index creation can vary from database to database, but in standard SQL it consists of the statement `CREATE INDEX` followed by a name for the index,
`ON` the table name, followed by a list of the columns to indexed.
So adding an index on the `region` field of a `sales` table looks like this:

```sql
CREATE INDEX sales_by_region
ON sales (region);
```