### Basics about MongoDB

* MongoDB is a **NoSQL database** — it’s not relational and doesn’t use rows and columns like traditional databases.
* It organizes data using **collections** and **documents**.
* A **collection** holds records of the same type (e.g., users, authors, books).
* Each **collection** contains multiple **documents**.
* Documents are stored in **JSON-like format** (actually BSON, a binary version of JSON).
* MongoDB supports **nested documents**, so you can store complex data structures easily.

---

### MongoDB Compass vs. MongoDB Atlas

* **MongoDB Compass** is the local GUI application to interact with your MongoDB database on your computer.
* **MongoDB Atlas** is the cloud-hosted version where you can create and manage MongoDB clusters online.
* You can connect **Atlas** to **Compass** using a connection string for easy management.

---

### Installing MongoDB Compass

1. Download MongoDB Community Server:
   [https://www.mongodb.com/try/download/community](https://www.mongodb.com/try/download/community)

   * Make sure **“Install MongoDB as a service”** is checked during setup.

2. Download MongoDB Shell (mongosh):
   [https://www.mongodb.com/try/download/shell](https://www.mongodb.com/try/download/shell)

3. Open your terminal and start the shell by typing:

   ```
   mongosh
   ```

4. Common commands:

   * Show databases:

     ```
     show dbs
     ```
   * Use a specific database:

     ```
     use database_name
     ```

5. Insert data into a collection from the shell:

   * Insert one document:

     ```
     db.books.insertOne({ title: "The Color of the Wind", author: "Terry Henry", pages: 450, rating: 7, genres: ["fantasy", "magic"] })
     ```
   * Insert multiple documents:

     ```
     db.books.insertMany([
       { title: "The Color of the Wind", author: "Terry Henry", pages: 450, rating: 7, genres: ["fantasy", "magic"] },
       { title: "Va Va Voom", author: "Mickey Mouse", pages: 234, rating: 9, genres: ["children", "magic"] }
     ])
     ```

6. Query data:

   * Find all documents:

     ```
     db.books.find()
     ```
   * Find documents with filter:

     ```
     db.books.find({ author: "Mickey Mouse" })
     ```
   * Find documents with multiple filters:

     ```
     db.books.find({ author: "Mickey Mouse", rating: 7 })
     ```


