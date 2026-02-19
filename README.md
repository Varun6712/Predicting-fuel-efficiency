
# 🌾 Farm Goods Marketplace -- Streamlit Web Application

## 📌 Overview

Farm Goods Marketplace is a Python-based web application built using
Streamlit.\
It allows users to browse and order farm products online, while
administrators can manage products and monitor orders.

The application uses SQLite as the database and includes email
notifications for order confirmations.

------------------------------------------------------------------------

## 🚀 Features

### 👤 User Features

-   User Registration & Login
-   Browse available farm products
-   Place orders
-   Receive order confirmation via email

### 🛠 Admin Features

-   Admin login
-   Add new products
-   View all customer orders
-   Receive email notification for new orders

------------------------------------------------------------------------

## 🗄 Database Structure

The application automatically creates a SQLite database named:

farm_goods.db

### Tables:

### 1️⃣ Users

  Column     Type   Description
  ---------- ------ ---------------
  username   TEXT   Primary Key
  password   TEXT   User Password
  role       TEXT   Admin/User

### 2️⃣ Products

  Column            Type
  ----------------- --------------------
  product_name      TEXT (Primary Key)
  price             REAL
  available         INTEGER
  quality           TEXT
  date_of_produce   DATE
  shelf_life        INTEGER
  image             BLOB

### 3️⃣ Orders

  Column         Type
  -------------- --------------------------
  id             INTEGER (Auto Increment)
  username       TEXT
  product_name   TEXT
  quantity       INTEGER
  mobile         TEXT
  address        TEXT
  email          TEXT
  status         TEXT (Default: Pending)

------------------------------------------------------------------------

## 🛠 Technologies Used

-   Python
-   Streamlit
-   SQLite3
-   Pandas
-   SMTP (Email Sending)
-   MIMEText

------------------------------------------------------------------------

## ⚙ Installation Guide

### 1️⃣ Install Required Packages

pip install streamlit pandas

### 2️⃣ Configure Email Credentials

Inside the send_email() function, update:

from_email = "your_email@gmail.com"\
password = "your_password"

⚠ Use an App Password for Gmail instead of your real password.

### 3️⃣ Run the Application

streamlit run fuel efficiency.py

------------------------------------------------------------------------

## 🔐 Authentication System

-   Users must register before login.
-   Role-based access (Admin / User).
-   Session state maintains login status.
-   Unauthorized access is restricted.

------------------------------------------------------------------------

## 🔮 Future Improvements

-   Password encryption (bcrypt)
-   Product editing and deletion
-   Order status update feature
-   Payment gateway integration
-   Improved UI design
-   Deployment on cloud server

------------------------------------------------------------------------

## 📂 Project Structure

fuel efficiency.py\
farm_goods.db (auto-created)\
README.md

------------------------------------------------------------------------

## 👨‍💻 Author

Developed as a learning project using Python and Streamlit.
