# Task 18 - MongoDB Library Management System

## Objective
The goal of this project is to create a Library Management System using MongoDB to manage a collection of books, authors, and patrons. This involves creating a database, inserting documents into collections, and performing CRUD operations, advanced queries, and updates via the MongoDB shell (Mongosh).

---

## Project Overview

- **Database Name**: `LibraryDB`
- **Collections**:
  - `Books`
  - `Authors`
  - `Patrons`
- **Operations**:
  - Insert data using `insertMany`.
  - Perform CRUD operations.
  - Execute advanced queries with operators.

---

## Prerequisites

1. **MongoDB**: Ensure MongoDB is installed and the server is running.  
   [Download MongoDB](https://www.mongodb.com/try/download/community)
2. **MongoDB Shell (Mongosh)**: Included with MongoDB or can be downloaded separately.
3. **Visual Studio Code**: Install [VS Code](https://code.visualstudio.com/).
4. **Git**: Ensure Git is installed to push your repository to GitHub.

---

## Setup Instructions

### 1. Start MongoDB Server
Start the MongoDB server in a terminal:
```bash
mongod



READ:
##Find All Books:

javascript
Copy code
db.Books.find().pretty()
Find a Book by Title:

javascript
Copy code
db.Books.find({ title: "To Kill a Mockingbird" })
Find All Books by an Author:

javascript
Copy code
db.Books.find({ author_id: 5 })
Find All Available Books:

javascript
Copy code
db.Books.find({ available: true })
UPDATE:
Mark a Book as Borrowed:

javascript
Copy code
db.Books.updateOne({ _id: 3 }, { $set: { available: false } })
Add a Genre:

javascript
Copy code
db.Books.updateOne({ _id: 8 }, { $addToSet: { genres: "Epic" } })
DELETE:
Delete a Book:
javascript
Copy code
db.Books.deleteOne({ title: "Brave New World" })
Advanced Queries
Example: Find Books Published After 1950:

javascript
Copy code
db.Books.find({ published_year: { $gt: 1950 } })