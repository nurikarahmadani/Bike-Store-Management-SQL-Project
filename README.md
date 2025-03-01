# Bike-Store-Management-SQL-Project

## Membangun Database
```sql
CREATE DATABASE bike_store

 DROP TABLE IF EXISTS customer;
 CREATE TABLE customer
 (
   cst_id VARCHAR(20) PRIMARY KEY,
   cst_key VARCHAR(20),
   first_name VARCHAR(50),
   last_name VARCHAR(50),
   marital_status VARCHAR(2),
   gender VARCHAR(2),
   create_date DATE 
 );

DROP TABLE IF EXISTS product;
   CREATE TABLE product
   (
     product_id VARCHAR(20) PRIMARY KEY,
     product_key VARCHAR(20),
     product_name VARCHAR(50),
     cost INT,
     product_line VARCHAR(2),
     product_start_date DATE,
     product_end_date DATE 
   );


   DROP TABLE IF EXISTS sales;
   CREATE TABLE sales
   (
     order_number VARCHAR(20) PRIMARY KEY,
     product_key VARCHAR(20),
     sls_cust_id VARCHAR(20),
     order_date DATE,
     ship_date DATE,
     due_date DATE,
     sales INT,
     quantity INT,
     price INT
     FOREIGN KEY (sls_cust_id) REFERENCES customer(cst_id)
   );
   
```
