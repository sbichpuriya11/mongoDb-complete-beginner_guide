# MongoDB Setup and Useful Tricks

This guide provides instructions for downloading and installing MongoDB, along with some useful tricks and commands for working with MongoDB.

## Installation Steps

- Download and install MongoDB Community Edition from [here](https://www.mongodb.com/try/download/community).
- Install MongoDB Shell from [here](https://www.mongodb.com/try/download/shell).
- Download MongoDB Database command-line tool from [here](https://www.mongodb.com/try/download/database-tools).

## Useful Tricks

1. **Monitoring MongoDB Service**:
   - MongoDB is registered as a service during installation. In the Windows search bar, search for "services" to check MongoDB's running status.

2. **Start and Stop MongoDB Service**:
   - In CMD (opened in admin mode), use the following commands:
     ```shell
     net stop MongoDB
     ```
     ```shell
     net start MongoDB
     ```

3. **Connecting to MongoDB Database**:
   - Use this connection string in mongoShell:
     ```
     mongodb://localhost:27017
     ```

4. **Flexible Schema**:
   - MongoDB allows adding different structured documents/records in the same collection. However, maintain one level of schema from the end user/developer's perspective.

5. **Atomicity**:
   - MongoDB provides atomicity in transactions, ensuring that either the complete document will be inserted/updated/deleted, or none at all. Atomicity applies to each record, not the complete transaction.

6. **Working with JSON Files**:
   - To work with JSON files from the command line, download the MongoDB command-line tool and add its bin directory to the Environment_variables path. Then, use the following command:
     ```shell
     mongoimport "D:\Courses\mongoDb\order_dummy.json" -d ecommerece -c orders --jsonArray --drop
     ```
     Response:
     ```
     2024-04-27T18:48:28.430+0530    connected to: mongodb://localhost/
     2024-04-27T18:48:28.431+0530    dropping: ecommerece.orders
     2024-04-27T18:48:28.460+0530    15 document(s) imported successfully. 0 document(s) failed to import.
     ```

---

Feel free to explore more MongoDB documentation and resources for advanced usage and optimization.
