<h1 align="center"> 🛍️ Shopping Application</h1>

## 📌 Overview
The purpose of shopping application is to provide an online platform where user can easily browse the products, add them to cart and place the orders. It simplifies the shopping process for users and allows them to manage their profile and orders efficiently.
For admin, The application offers a powerful backend system to manage products, categories, orders and users. It helps in handling all the store related operations in one place. 

### 🛠️ Tech Stack
- **Backend:** 🖥️ Java, Spring boot, Spring MVC, Spring Data JPA  
- **Frontend:** 🎨 HTML, CSS, Bootstrap, Javascript
- **Database:** 🗄️ MySQL  
- **Build Tool:** 🛠️ Spring Tool Suite 

## 🚀 Features

### 👤 User Features
- 🔑 **User Registration & Login:** Secure authentication with password reset via email & mobile.
- 🛒 **Product Browsing & Search:** Explore products by category and latest arrivals.
- 🛍️ **Shopping Cart & Orders:** Add products to cart, checkout, and track orders.
- 👤 **Profile Management:** View and update user details.

### 🛠️ Admin Features
- 📊 **Admin Dashboard:** A centralized panel to manage the application.
- 📦 **Product Management:** Add, edit, delete, and view products.
- 📂 **Category Management:** Manage product categories efficiently.
- 👥 **User Management:** View, update, and remove users.
- 🛡️ **Admin Management:** Add, view, edit, and remove admin users.
- 📦 **Order Management:** Track and update order statuses.

## 📐 Application Structure
- 📂 **Model Layer:** Defines entity classes representing database tables.
- 📂 **Repository Layer:** Handles database operations using Spring Data JPA.
- 📂 **Service Layer:** Implements business logic.
- 📂 **Controller Layer:** Manages HTTP requests and responses.
- 🎨 **Frontend:** Built using HTML, CSS, Bootstrap.

## 🛠️ How the Project Works
1. **Users** register and log in securely.
2. They can **browse products**, search by category, and view product details.
3. Users **add products to their cart**, update quantities, and proceed to checkout.
4. Orders are **stored in the database**, and users can track order history.
5. The **Admin Panel** allows administrators to **manage products, categories, users, and orders** efficiently.

## 🛠️ Setup & Installation

### 📋 Prerequisites
- ☕ **Java Development Kit (JDK) 8+**
- ⚙️ **Spring Boot Framework**
- 🗄️ **MySQL Database**
- 🛠️ **Maven**
- 💻 **Spring Tool Suite (STS)**

### ⚙️ Steps to Run the Application

#### 1️⃣ Clone the Repository
```sh
git clone https://github.com/your-username/shopping-application.git
cd shopping-application
```

#### 2️⃣ Configure Database (MySQL)
- Create a database in MySQL:
  ```sql
  CREATE DATABASE shopping_app;
  ```
- Update `application.properties` with MySQL credentials:
  ```properties
  spring.datasource.url=jdbc:mysql://localhost:3306/shopping_app
  spring.datasource.username=root
  spring.datasource.password=yourpassword
  spring.jpa.hibernate.ddl-auto=update
  ```

#### 3️⃣ Build the Project Using Maven
```sh
mvn clean install
```

#### 4️⃣ Run the Spring Boot Application
```sh
mvn spring-boot:run
```

#### 5️⃣ Access the Application
- **User Panel:** `http://localhost:8080/`
- **Admin Panel:** `http://localhost:8080/admin`


<h3 align="center">🎉 Happy Shopping! 🚀</h3> 
<p align="center">Thank you for checking out this project! If you found it helpful, <b>give it a star ⭐ on GitHub! </b> 😊</p>
