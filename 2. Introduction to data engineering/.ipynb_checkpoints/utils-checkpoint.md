### Inserting records in a database from a .sql file.

#### 1. Create the database using postgres commands.
```postgres
postgres=# CREATE DATABASE datacamp;
```


#### 2. Import the SQL file.
```bash
psql -h localhost -U postgres datacamp < inputs/datacamp_application.sql 
```

#### Change postgres password.
```postgres
ALTER USER user_name WITH PASSWORD 'new_password';
```