# Payroll Management System

A payroll management system is a software application designed to automate and streamline the process of calculating employee salaries, taxes, and other related financial calculations. It ensures that employees are paid accurately and that all payroll-related legal and regulatory requirements are met.

The objective of our project is to design and develop a payroll management system that automates the payroll process and ensures accuracy and transparency. The system includes features such as employee information management, salary calculation, adding and deleting employees, tax deductions, and generating pay reports, among others. By implementing this payroll management system, we aim to eliminate the manual and time-consuming process of payroll management, reduce errors, and improve data security.

## Pre-requisites

- Install node, npm and nodemon
- Install PostgreSQL

### To set up PostgreSQL user, database and tables

```bash
psql
> CREATE ROLE me WITH LOGIN PASSWORD 'password';
> ALTER ROLE me CREATEDB;
> CREATE DATABASE api;
> GRANT ALL ON SCHEMA public TO me;
> \q
cd backend/commands
psql -h localhost -U me -d api -a -f DDL.sql
```

### To create an Admin

Send a post request to http://localhost:3003/api/adminSignup with json body containing "email", "password", "username". This can be done using postman or any other tools.

### To create an Organisation

Send a post request to http://localhost:3003/api/addOrganisation with json body containing org_name, email, location, contact_number, paid_leave_limit, encashed_leave_limit. This can be done using postman or any other tools.

## Running the application

### To start Frontend React Server
```bash
cd frontend
npm i
npm start
```

### To start Backend Server
```bash
cd backend
npm i
nodemon index.js
```

## Troubleshooting

When starting the frontend server, if you get an error with code 'ERR_OSSL_EVP_UNSUPPORTED', then run:
```bash
export NODE_OPTIONS=--openssl-legacy-provider
```

## Authors

- **Ahmad Amaan**
- **Dhriti Garg**
- **Kratik Agrawal**
- **Yash Gupta**
