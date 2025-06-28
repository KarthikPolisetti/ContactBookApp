ContactBookApp
A Java application for managing contacts (name, phone, email) using a MySQL database.
Database Setup

Install MySQL: Ensure MySQL is installed and running.
Create Database and Table:
Run the SQL script located at resources/database.sql:mysql -u your_username -p < resources\database.sql

Replace your_username with your MySQL username and enter your password when prompted.


Configure Database Connection:
Update the database credentials in src/dao/ContactDAO.java (or the relevant file handling database connections):private static final String URL = "jdbc:mysql://localhost:3306/contactbookdb";
private static final String USER = "your_username";
private static final String PASSWORD = "your_password";





Running the Application

Prerequisites:
Java Development Kit (JDK) 8 or higher.
MySQL Connector/J (JDBC driver) in the classpath.
If using Maven, add to pom.xml (if applicable):<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.33</version>
</dependency>






Compile and Run (in PowerShell):
Navigate to the project directory:cd K:\SumIship\NdvTechSys\Internships\internships\ContactBookApp


Compile the Java files:javac -cp ".;path\to\mysql-connector-java.jar" src\main\*.java src\dao\*.java src\model\*.java

Replace path\to\mysql-connector-java.jar with the path to your MySQL JDBC driver.
Run the application:java -cp ".;path\to\mysql-connector-java.jar" main.ContactBook


If using Maven:mvn clean package
java -jar target\ContactBookApp-1.0-SNAPSHOT.jar




Usage:
Follow the console menu to add, view, update, or delete contacts.



Project Structure
ContactBookApp/
├── src/
│   ├── main/
│   │   ├── ContactBook.java
│   ├── dao/
│   │   ├── ContactDAO.java
│   ├── model/
│   │   ├── Contact.java
├── resources/
│   ├── database.sql
├── .gitignore
├── README.md
├── pom.xml (if using Maven)
