# ContactBookApp

A Java application to manage contacts with CRUD operations, using MySQL for data storage.

## Prerequisites
- Java 17 (OpenJDK 17.0.10)
- MySQL 8.0+
- MySQL Connector/J 9.3.0 (located at `K:\SumIship\folder2\lib\mysql-connector-j-9.3.0.jar`)

## Database Setup
1. Install and start MySQL.
2. Run the provided SQL script to create the database and table:
   ```bash
   mysql -u root -p < resources/database.sql
