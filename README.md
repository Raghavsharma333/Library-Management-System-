# Library-Management-System
A simple Java Swing-based Library Catalog System that allows users to add books to a MySQL database and view the catalog using a GUI.

# Features:

Add Books: Enter book details (Title, Author, Year, ISBN) and save them in a database.
View Catalog: Display the stored books in a GUI table.
MySQL Integration: Uses JDBC to interact with a MySQL database.

# Technologies Used

Java (Swing for GUI, JDBC for database connectivity)
MySQL (Database for storing book information)

# Installation & Setup

1. Prerequisites
Ensure you have the following installed:
Java Development Kit (JDK 8+)
MySQL Server
MySQL JDBC Driver (Download from MySQL Connector/J)

2. Database Setup
Start MySQL Server.
Create a database named library (or use the included Java program to create it automatically).
Run the following SQL script to create the books table manually (if needed):
CREATE DATABASE IF NOT EXISTS library;
USE library;
CREATE TABLE IF NOT EXISTS books (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    author VARCHAR(255),
    publication_year INT,
    isbn VARCHAR(13)
);

3. Configure Database Credentials

Update the following lines in LibraryCatalogSystem.java with your MySQL username and password:
private static final String DB_USER = "your_username";
private static final String DB_PASSWORD = "your_password";

4. Run the Application

Compile and execute the Java program:
javac LibraryCatalogSystem.java
java LibraryCatalogSystem

Usage

Launch the application.
Add a book by entering its details and clicking the Add Book button.
Click View Catalog to see the list of books stored in the database.

# Enhancements (Future Features)

Edit and Delete Books
Search Functionality
Export Catalog to CSV/PDF

# Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss your ideas.

# License

This project is licensed under the MIT License. Feel free to use and modify it.



