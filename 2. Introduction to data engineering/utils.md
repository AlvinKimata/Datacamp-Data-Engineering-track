### Inserting records in a database from a .sql file.

#### 1. Create the database using postgres commands.
```bash
postgres=# CREATE DATABASE datacamp;
```


#### 2. Import the SQL file.
```bash
psql -h localhost -U postgres datacamp < inputs/datacamp_application.sql 
```