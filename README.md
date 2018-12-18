# useful-sql
A collection of handy MySQL commands

### Table Information
##### Get the size of each table in a database, descending order
```
SELECT **table_name** AS "Table",
ROUND(((data_length + index_length) / 1024 / 1024), 2) AS "Size (MB)"
FROM information_schema.TABLES
WHERE table_schema = "**database_name**"
ORDER BY (data_length + index_length) DESC;
```
