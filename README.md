# CMSProject

An online delivery system designed to streamline the process of ordering and delivering products.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Architecture](#architecture)
5. [Installation](#installation)
6. [Usage](#usage)
7. [API Endpoints](#api-endpoints)
8. [Database Schema](#database-schema)
9. [Contact](#contact)

## Project Overview

CMSProject is an online delivery platform that connects customers with local vendors, facilitating seamless product ordering and timely deliveries. The system aims to enhance user convenience and expand vendor reach by providing an intuitive interface and efficient order management.

## Features

- User Registration and Authentication: Secure sign-up and login functionalities for customers and vendors.
- Product Browsing: Allows customers to explore available products easily.
- Order Management: Enables real-time tracking of orders from placement to delivery.
- Payment Integration: Supports multiple payment gateways for seamless transactions.
- Vendor Dashboard: Provides vendors with tools to manage inventory, view orders, and analyze sales.
- Admin Panel: Manage users, vendors, products, and transactions.

## Technologies Used

- Frontend:
  - HTML5, CSS3, JavaScript
  - React.js for dynamic user interfaces
- Backend:
  - Java with Spring Boot framework
  - Maven for project management and build automation
- Database:
  - MongoDB for database management
- Payment Processing:
  - Integration with Stripe and PayPal APIs
- Deployment:
  - Hosted on AWS with CI/CD pipelines using Jenkins

## Architecture

The project follows a Microservices Architecture with the following services:

- User Service: Handles user registration, authentication, and profile management.
- Product Service: Manages product catalog and inventory.
- Order Service: Manages order placement, tracking, and delivery.
- Payment Service: Processes payments and handles refunds.
- Notification Service: Sends order and delivery notifications to users.

## Installation

To set up the project locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/BhagyaRapolu/RLLproject.git

2. Navigate to the CMSProject directory:
    ```bash
    cd RLLproject/CMSProject
3. Install backend dependencies:
    ```bash
    mvn install
4. Set up environment variables:
    Create a .env file in the CMSProject directory with the following:
    ```ini
    DATABASE_URL=your_database_url
   JWT_SECRET=your_jwt_secret
   STRIPE_SECRET_KEY=your_stripe_secret_key
5. Start the application:
    ```bash
    mvn spring-boot:run

## Usage
1. Access the application:
  Open your browser and navigate to http://localhost:8080.
2. Explore as a customer:
  Register or log in.
  Browse products, add items to the cart, and proceed to checkout.
3. Explore as a vendor:
  Register or log in.
  Access the vendor dashboard to manage products and view orders.
4. Admin Access:
  Manage users, vendors, and products through the admin panel.
## API Endpoints
  User Registration: /api/register
  User Login: /api/login
  Product Listing: /api/products
  Order Placement: /api/orders
  Payment Processing: /api/pay
  Order Tracking: /api/track/{orderId}
## Database Schema
  ```paintext
+-----------------+--------------+--------------------------------+
|      Field       |     Type     |          Description            |
+-----------------+--------------+--------------------------------+
| userId           | String       | Unique identifier for the user  |
| username         | String       | User's name                     |
| password         | String       | Hashed password                 |
| role             | String       | User role (customer/vendor)     |
+-----------------+--------------+--------------------------------+

+-----------------+--------------+--------------------------------+
|      Field       |     Type     |          Description            |
+-----------------+--------------+--------------------------------+
| productId        | String       | Unique identifier for the product|
| name             | String       | Product name                    |
| price            | Double       | Product price                   |
| category         | String       | Product category                |
+-----------------+--------------+--------------------------------+

+-----------------+--------------+--------------------------------+
|      Field       |     Type     |          Description            |
+-----------------+--------------+--------------------------------+
| orderId          | String       | Unique order ID                 |
| userId           | String       | ID of the customer who placed it |
| items            | Array        | List of product IDs             |
| total            | Double       | Total amount                    |
| status           | String       | Current status of the order      |
+-----------------+--------------+--------------------------------+
```
## Contact
  For questions or feedback:
  Project Maintainer: Bhagya Rapolu
  Email: rapolubhagyalakshmi9@gmail.com
  
    Let me know if you need further customization or adjustments!


