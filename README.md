# 📚 MongoDB Fundamentals Assignment – PLP Bookstore

This project is part of the MongoDB Fundamentals Assignment. It demonstrates key MongoDB features including database setup, CRUD operations, advanced queries, aggregation pipelines, and indexing using a sample `plp_bookstore` database.

---

## 🚀 Objectives

- Set up a MongoDB database locally
- Insert sample book data using a provided script
- Perform CRUD operations
- Write advanced queries with filtering, projection, sorting, and pagination
- Build aggregation pipelines for data analysis
- Implement indexing to optimize query performance

---

## 🛠️ Setup Instructions

### ✅ Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- [MongoDB Community Edition](https://www.mongodb.com/try/download/community)
- MongoDB Shell (`mongosh`)
- VS Code or any text editor

---

### 📂 Installation & Data Setup

1. **Clone the Repository**  
   Clone your GitHub Classroom repository:

   ```bash
   git clone https://github.com/YOUR-CLASSROOM-REPO.git
   cd YOUR-CLASSROOM-REPO

2. Start MongoDB Server
Ensure your MongoDB server is running locally.

3. Run the Insert Script in MongoDB Shell
Open a terminal and enter the MongoDB Shell:
```mongosh```
Then load the insert script:
```load("insert_books.js")```

4. Verify the Data
```use plp_bookstore
db.books.find().pretty()```

📄 Files in This Project
File Name	Description
insert_books.js	Script to insert at least 10 book documents
queries.js	MongoDB queries (CRUD, advanced, aggregation, indexing)
README.md	Setup instructions and project description
screenshot.png	Image showing your MongoDB Compass or shell data

🧪 Example Queries
Here are a few sample queries you can test in mongosh:
```// Find all books in the Fantasy genre
db.books.find({ genre: "Fantasy" })

// Find books published after 2010
db.books.find({ published_year: { $gt: 2010 } })

// Aggregate: Average price per genre
db.books.aggregate([
  { $group: { _id: "$genre", avgPrice: { $avg: "$price" } } }
])```
For the full list, see the queries.js file.

📸 Screenshot
📷 Make sure to include a screenshot showing your plp_bookstore collection (either in MongoDB Compass or terminal) as screenshot.png.

✅ Submission Checklist
 insert_books.js added and working

 queries.js with all required operations

 Screenshot added

 README.md completed

 All files pushed to GitHub Classroom repo

📬 Submit
Push your work to GitHub:
git add .
git commit -m "Complete MongoDB Week 1 Assignment"
git push origin main

👨‍💻 Author
Lethabo Molemi
