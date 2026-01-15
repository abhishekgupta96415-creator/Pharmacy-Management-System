CREATE DATABASE pharmacy;
USE pharmacy;

CREATE TABLE stock (
    med_no INT PRIMARY KEY,
    name VARCHAR(50),
    genere VARCHAR(30),
    manufacturer VARCHAR(50),
    doe DATE,
    dom DATE,
    rate INT,
    quantity INT,
    strength INT,
    category VARCHAR(30)
);

CREATE TABLE staff (
    staff_id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    gender CHAR(1),
    phone BIGINT,
    address VARCHAR(100)
);

CREATE TABLE customer (
    cust_no BIGINT PRIMARY KEY,
    name VARCHAR(50),
    address VARCHAR(100)
);

CREATE TABLE billing (
    bill_no INT PRIMARY KEY,
    cust_no BIGINT
);

CREATE TABLE billing_details (
    sale_id INT,
    med_no INT,
    bill_no INT,
    rate INT,
    quantity INT
);
