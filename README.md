                           Library Management System – SQL Project
Project Description
A relational database system built using SQL to manage a library's core entities: authors, publishers, books, members, and loan records. This project demonstrates the use of SQL DDL, DML.
 Key Features
 Relational schema with 5 tables

 Foreign key relationships between books, authors, publishers, and members

 Insert, Update, Delete, and Select operations

 Data validation through constraints (e.g., UNIQUE, NOT NULL)
 

 Database Structure
 Authors
AuthorID (PK)
Name
Country

 Publishers
PublisherID (PK)
Name
Country

 Books
BookID (PK)
Title
Genre
ISBN (UNIQUE)
AuthorID (FK → Authors)
PublisherID (FK → Publishers)

 Members
MemberID (PK)
Name
JoinDate
Email (UNIQUE)

 Loans
LoanID (PK)
BookID (FK → Books)
MemberID (FK → Members)
IssueDate
ReturnDate (nullable)

 Usage Instructions
Create Database

CREATE DATABASE LibraryManagementSystem;
USE LibraryManagementSystem;
Create Tables (Authors, Publishers, Books, Members, Loans)

Insert Sample Data
INSERT INTO Authors (Name, Country) VALUES ('Dr.Charles', 'USA');

Run Queries

View all books:
SELECT * FROM Books;

Update a genre:
UPDATE Books SET Genre = 'Underwater creatures' WHERE Title = 'Sea Creatures';

Delete returned loans:
DELETE FROM Loans WHERE ReturnDate IS NOT NULL;

 Sample Data Summary
3 Authors: From USA, Africa, Japan

3 Publishers: Eagle, Collins, Bliss

3 Books: Assigned to different authors & publishers

2 Members: Jai and Vardha

2 Loans: One returned, one ongoing


