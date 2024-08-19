#### Basics about MongoDB
- NoSQL database (i.e not relational, not made out of rows and columns)
- MongoDB uses collections and documents
- Collecions store a specific type  of data record e.g users, authors, books
- In a collection are documents
- documents have JSON format, but actually they are stored as bison
- It can be used to store nested documents

#### MongoDB-Compass Vs. MongoDB Atlas
- MongoDB-Compass: the local version
- MongoDB-Atlas: the online version. Use to make and host a cluster online. It an be connected to MongoDB Compass through a connection string.

#### Installing MongoDB Compass
-  https://www.mongodb.com/try/download/community
-  Make sure install mongoDB as a service is checked
-  install mongoDB shell from https://www.mongodb.com/try/download/shell
-  open terminal and type mongosh
-  show dbs
-  use database_name
-  inserting data from shell to mongodb:
-    - db database_name.collection_name e.g database_name is bookstore, collection_name is books
     - db.books.insertOne({title: "The Color of the Wind", author"Terry Henry", pages: 450, rating: 7, genres: ["fantasy", "magic"]}) --> inserting one document
     - db.books.inserMany({title: "The Color of the Wind", author"Terry Henry", pages: 450, rating: 7, genres: ["fantasy", "magic"]}, {title: "Va Va Voom", author"Mickey Mouse", pages: 234, rating: 9, genres: ["children", "magic"]}) ---> inserting many 
