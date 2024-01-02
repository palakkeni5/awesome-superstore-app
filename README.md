# Awesome Superstore App

This repository contains the web application, database and ETL components for a business use case to develop an e-commerce web application for Awesome Superstore Inc.

This project was developed as a part of the NYU Fall 2023 course ECE-GY 9953: Advanced Project 1 under Prof. Amit Patel
## Project Overview

This project involved designing and implementing a robust database backend to support the core business operations of Awesome Superstore - an online furniture and office supplies retailer.

The key components developed are:

- Online Transaction Processing (OLTP) database built with MySQL.
- Database-driven web application built with React, Node.js and Express.
- Data warehouse built with Oracle Database.
- ETL workflow scripts to store data from OLTP database to data warehouse using CDC process.
  
## Tech Stack

- React.js
- Node JS (Express.js)
- MySQL
- Oracle SQL

## Web Application

  ![web-app-architecture](https://github.com/palakkeni5/awesome-superstore-app/assets/42136520/b0f8804f-d2ef-4638-a617-a2a0cae47db8)


The React-based web application provides the following functionality:

- Product browsing
- Shopping cart
- Order management
- User profile and password management
- Add new Products

Kindly refer to the code inside the awesome-superstore-backend and awesome-superstore-frontend folder.

OLTP database code can be found inside the awesome_superstore_db/mysql folder
## ETL workflow

![ETL workflow](https://github.com/palakkeni5/awesome-superstore-app/assets/42136520/5773e687-a6e5-4213-a992-ddcbd12e685f)


- Initial full extract export from MySQL, apply transformations, load into warehouse (baseline)
- etl_extract_date table tracks full extract timestamps
- Then periodic incremental extracts from MySQL - only changed data since last extract
- Apply similar ETL process on extracts and merge into data warehouse tables
- Achieves ongoing synchronization of data warehouse with only incremental deltas


## Contributors

- [Palak Pramod Keni](https://github.com/palakkeni5)
- [Brian Catraguna](https://github.com/briancatraguna)
