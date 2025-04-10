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
   
