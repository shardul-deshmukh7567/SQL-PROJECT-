Project Overview..
This project involves analyzing data from a coffee shop to gain insights into clients membership , and product varities, product categories, product cost , worker names their salaries.
The dataset includes information on clients, products, shop , transaction , workers.

Database Design
The database consists of  5 tables:

1. clients: stores information about each client, including their name, email, phone no and city.
2.  shop :information about each branch, including address of that particular branch.
3. products: stores information about each product, including the product ID,, product type ,product name, and price.
4. transaction: stores information about transaction id's and transaction status.
5. workers : stores information about each worker name , phone no , their post and salary.


   ***CODE FOR THIS PROJECT IS GIVEN BELOW..


   ## coffee shop sales 
create database coffee;
use coffee;

show tables;

create table shop1 (
shop_id int(10),
shop_name char (20),
shop_address varchar (100),
city char (50));

show tables;
desc shop1;
 
insert into shop1 values ('1','cafe_blush','cannought garden ','chh sambhajinagar'); 
insert into shop1 values ('2','cafe_coffee','cannought garden ','chh sambhajinagar');
insert into shop1 values ('3','ccd','kranti chowk ','chh sambhajinagar');
insert into shop1 values ('4','cafe_rozas','bypass road ','chh sambhajinagar');
insert into shop1 values ('5','cafe_pocket','bypass road ','chh sambhajinagar');
insert into shop1 values ('6','cafe_woodies','usmanpura ','chh sambhajinagar');
insert into shop1 values ('7','salt n paper ','usmanpura ','chh sambhajinagar');
insert into shop1 values ('8','no meet naan ','cannought garden ','chh sambhajinagar');
insert into shop1 values ('9','UFO','cannought garden ','chh sambhajinagar');
insert into shop1 values ('10','ESS-PRESS-OH ','prozon mall ','chh sambhajinagar');
insert into shop1 values ('11','STARBUCKS ','cannought garden ','chh sambhajinagar');
insert into shop1 values ('12','urban bites ','cannought garden ','chh sambhajinagar');
insert into shop1 values ('13','rosewood ','cannought garden ','chh sambhajinagar');
insert into shop1 values ('14','CCC ','ulkanagri ','chh sambhajinagar');
insert into shop1 values ('15','chai_bite','MIT COLLEGE ','chh sambhajinagar');
insert into shop1 values ('16','blessings ','MIT COLLEGE ','chh sambhajinagar');
insert into shop1 values ('17','burger basket ','cannought garden ','chh sambhajinagar');
insert into shop1 values ('18','7th heaven  ','cannought garden ','chh sambhajinagar');
insert into shop1 values ('19','4ks cafe  ','cannought garden ','chh sambhajinagar');
insert into shop1 values ('20','frozen bottle','near MGM college ','chh sambhajinagar');


select * from shop1;

create table product (
product_id int (10),
product_category varchar (50),
product_type varchar (50),
product_cost int (255));

show tables ;
desc product ;

insert into product values ('1',' hot coffee','drip coffee','199');
insert into product values ('2','tea','herbal tea','59');
insert into product values ('3','hot chocolate','drip ','99');
insert into product values ('4','cold coffee','drip coffee','49');
insert into product values ('5','belgium coffee','drip coffee','199');
insert into product values ('6','Cappuccino','drip coffee','99');
insert into product values ('7','hazulnut coffee','drip coffee','129');
insert into product values ('8','vanilla coffee','drip coffee','149');
insert into product values ('9','chocolate coffee','drip coffee','79');
insert into product values ('10','Espresso','drip coffee','69');
insert into product values ('11','Cold brew','drip coffee','99');
insert into product values ('12','Latte','drip coffee','169');
insert into product values ('13','Americano','drip coffee','179');
insert into product values ('14','Turkish Coffee','drip coffee','195');
insert into product values ('15','coffee','black coffee','39');
insert into product values ('16','tea','green tea','35');
insert into product values ('17','hot chocolate ','drip coffee','100');
insert into product values ('18','tea','adrak tea','20');
insert into product values ('19','coffee','drip coffee','30');
insert into product values ('20','coffee','drip coffee','30');

select * from product;

create table clients (
    customer_Name VARCHAR(100),
    Email VARCHAR(100),
    Phone VARCHAR(15),
    city char (50),
    bill_status char (50));
    
show tables;
desc clients;

insert into clients values ('siddhi','sk8765@gmail.com','1234567890','pune','paid');
insert into clients values ('shardul','sd1234@gmail.com','1267567890','pune','paid');
insert into clients values ('sonu','sonu5@gmail.com','1234566790','ambad','pending');
insert into clients values ('ved','ved5@gmail.com','1234567234','chh sambhajinagar','pending');
insert into clients values ('sarth','sarth22@gmail.com','9876567890','chh sambhajinagar','paid');
insert into clients values ('parth','parthkothode1@gmail.com','9874567890','mumbai','cancelled');
insert into clients values ('shrutika','shrutika234@gmail.com','6234567890','pune','paid');
insert into clients values ('pradyumn','pradyumn654@gmail.com','17234567890','pune','cancelled');
insert into clients values ('vedant','vedant5454@gmail.com','18234567890','benglore','paid');
insert into clients values ('abhishek','abhi6789@gmail.com','19234567890','pune','cancelled');
insert into clients values ('sakshi','sakshi890@gmail.com','4234567890','ambad','paid');
insert into clients values ('rajvi','raajvi01@gmail.com','9234567890','pune','pending');
insert into clients values ('arun','arun9090@gmail.com','0234567890','mumbai','paid');
insert into clients values ('ritesh','ritech45455@gmail.com','5434567890','pimpri','pending');
insert into clients values ('aditi','aadi2323@gmail.com','7234567890','yeola ','paid');

select * from clients;

create table workers (
 worker_name char (100),
    phone  VARCHAR(100),
    post varchar (50),
    Salary decimal );
    
    show tables;
    desc workers;
    
    insert into workers values ('sanjeev ','3456789870','owner','45000');
	insert into workers values ('rajiv ','8856789870','Barista','5000');
    insert into workers values ('manish ','3567789870','coffee Artisan','4000');
    insert into workers values ('sunny ','9456789870','Server r','7000');
    insert into workers values ('vikas ','8456789870','Server ','5000');
    insert into workers values ('madhur ','7456789870','owner','45000');
    insert into workers values ('raju ','356789870','cashier','15000');
    insert into workers values ('varun ','56789870','owner','45000');
    insert into workers values ('vicky ','45656789870','Server r','6000');
    insert into workers values ('virat ','9996789870','barista','5000');

select * from workers ;

show tables;

create table transactions (
product_id int(10),
transaction_id varchar (100),
transaction_status varchar (50));

show tables;
desc transactions ;

insert into transactions values ('1','23456','completed');
insert into transactions values ('2','22456','processing');
insert into transactions values ('3','4567','pending ');
insert into transactions values ('4','11456','completed');
insert into transactions values ('5','45456','completed');
insert into transactions values ('6','13456','processing');

select * from transactions ;

rename table transactions to payments;
show tables ;


## queries realted to this 

## 1) display the barista of coffee shop 
select * from workers 
where post ='barista';

## 2) find a clients  who have premium membership 
select * from clients 
where membership = 'premium';

## 3) retrieve all the clients name ,city ,email ,phone 
select clients.customer_name,city,email,phone from clients ;

## 4) retrieve the information of clients who lives in pune
select * from clients 
where city = 'pune';

## 5)  retrieve the product information coffee 
select * from product 
where product_category = 'coffee';

## 6) display the information of all shops 

select * from shop1;

## 7) display the information of shop having id 1 
select * from shop1 
where shop_id = '1';

## 8) Find all clients with pending bills
SELECT customer_Name, Phone, Email
FROM clients
WHERE bill_status = 'Pending';

## 9) List all products with a cost above 99
SELECT product_id, product_type, product_cost
FROM product
WHERE product_cost > 99;

## 10) Retrieve all shops located in a specific city
SELECT shop_name, shop_address
FROM shop1
WHERE city = 'chh sambhajinagar';

## 11) List all products under a specific category
SELECT product_id, product_type, product_cost
FROM product
WHERE product_category = 'hot chocolate';

## 12) Combine all products with all shops.
SELECT product.product_id, product.product_type, shop1.shop_name, shop1.city
FROM product JOIN shop1;

## 13)Retrieve workers earning above the average salary.
SELECT worker_name, Salary
FROM workers WHERE Salary > (SELECT AVG(Salary) FROM workers);

## 14)Find  the Minimum and Maximum Product Costs
SELECT MIN(product_cost) AS min_cost, MAX(product_cost) AS max_cost
FROM product;

## 15) Find the Lowest and Highest Salaries:
SELECT MIN(Salary) AS min_salary, MAX(Salary) AS max_salary
FROM workers;

## 16) Find  Minimum and Maximum Product Costs by Category
SELECT product_category, MIN(product_cost) AS min_cost, MAX(product_cost) AS max_cost
FROM product GROUP BY product_category;

## 17) Find the  Minimum and Maximum Salaries by Position
SELECT post, MIN(Salary) AS min_salary, MAX(Salary) AS max_salary
FROM workers GROUP BY post;

## 18) List the customers along with the city they belong to and their bill status
SELECT customer_Name, city, bill_status FROM clients;

## 19) Show the total number of products in each category.
SELECT product_category, COUNT(*) AS total_products
FROM product GROUP BY product_category;

## 20) Count the total number of workers in each post.
SELECT post, COUNT(*) AS total_workers FROM workers GROUP BY post;

## 21) Get the total cost of all products in the store
SELECT SUM(product_cost) AS total_product_cost FROM product;

## 22) Display all cities where clients and shops exist
SELECT city FROM clients
UNION
SELECT city FROM shop1;

## 23) Show the list of workers who have a salary greater than 30000
SELECT worker_name, Salary FROM workers WHERE Salary > 30000;
   
