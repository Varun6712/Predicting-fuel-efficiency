🌾 Farm Goods Marketplace – Streamlit Application
📌 Project Overview

Farm Goods Marketplace is a web-based application built using Python and Streamlit that allows users to buy farm products online. The system includes user authentication, product management, order processing, and email notifications.

The application uses SQLite as the backend database and provides separate interfaces for Admin and User roles.

🚀 Features
👤 User Features

User Registration & Login

Browse available farm products

Place orders

Receive email confirmation after order placement

🛠 Admin Features

Admin login

Add and manage products

View all orders

Receive email notifications for new orders

📦 Product Management

Add product name

Set price and available quantity

Define quality and shelf life

Store product image

Track date of produce

📧 Email Notification System

Admin receives email when a new order is placed

User receives order confirmation email

🗂 Database Structure

The application uses SQLite database (farm_goods.db) with the following tables:

1️⃣ Users Table
Column	Type
username	TEXT (Primary Key)
password	TEXT
role	TEXT (Admin/User)
2️⃣ Products Table
Column	Type
product_name	TEXT (Primary Key)
price	REAL
available	INTEGER
quality	TEXT
date_of_produce	DATE
shelf_life	INTEGER
image	BLOB
3️⃣ Orders Table
Column	Type
id	INTEGER (Auto Increment)
username	TEXT
product_name	TEXT
quantity	INTEGER
mobile	TEXT
address	TEXT
email	TEXT
status	TEXT (Default: Pending)
🛠 Technologies Used

Python

Streamlit

SQLite3

Pandas

SMTP (Email Service)

MIMEText (Email formatting)

⚙ Installation & Setup
Step 1: Install Required Packages
pip install streamlit pandas

Step 2: Configure Email Credentials

Inside the send_email() function, update:

from_email = "your_email@gmail.com"
password = "your_password"


Use:

A valid Gmail account

App password (recommended for security)

Step 3: Run the Application
streamlit run fuel efficiency.py

🔐 Authentication Flow

Users must register before logging in.

Role selection is required (Admin/User).

Session state maintains login status.

Unauthorized access is restricted.

📷 Application Interface

Sidebar navigation for:

Login

Register

Admin Interface

User Interface

Wide layout configuration for better UI experience.

📌 Future Enhancements

Password hashing for better security

Order status update functionality

Product editing & deletion

Payment gateway integration

Improved UI/UX design

Cloud database deployment

Role-based dashboard customization

⚠ Security Note

Currently:

Passwords are stored in plain text.

Email credentials are hardcoded.

For production deployment:

Use password hashing (bcrypt)

Store credentials using environment variables

Use secure database hosting

📄 Project Structure
fuel efficiency.py
farm_goods.db (auto-created)
README.md

👨‍💻 Developed With

Python & Streamlit for learning full-stack web application development.
