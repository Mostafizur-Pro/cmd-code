# Create PostgreSQL Database on Linux using Command Line

## Step 1: Login to PostgreSQL

```bash
sudo psql -U postgres
```

## Step 2: Create a new database

```bash
CREATE DATABASE new_database_name;

```

```bash
\conninfo
```

<img src="images/01.png" alt="PostgreSQL Databases" />

Verify the database

```bash
\l
```

<img src="images/02.png" alt="PostgreSQL Exit" />

Exit PostgreSQL

```bash
\q
```

[BACK](db-import-export.md)
