# Pizza Management System

### Developed by: Dijanira and Alfred
GitHub Repository: https://github.com/DijaniraMuachifi/PizzajavaSeminar.git 

---

## Table of Contents
1. [Introduction](#introduction)  
2. [Project Requirements](#project-requirements)  
3. [General Project Structure](#general-project-structure)  
   - [Technologies Used](#technologies-used)  
   - [Folder Structure](#folder-structure)  
4. [Database](#database)  
   - [Table Structures](#table-structures)  
   - [Table Relationships](#table-relationships)  
5. [Implemented Features](#implemented-features)  
   - [Home Page](#home-page)  
   - [Registration and Login](#registration-and-login)  
   - [User Roles](#user-roles)  
   - [Data Display](#data-display)  
   - [Contact Form](#contact-form)  
   - [Stored Messages](#stored-messages)  
6. [RESTful API](#restful-api)  
   - [Available Endpoints](#available-endpoints)  
   - [Testing with cURL and Postman](#testing-with-curl-and-postman)  
7. [GitHub Usage](#github-usage)  
   - [Commit Structure](#commit-structure)  
   - [Repository Organization](#repository-organization)  
8. [Screenshots](#screenshots)  
9. [Conclusion](#conclusion)  
10. [Future Improvements](#future-improvements)  

---

## 1. Introduction  
This project was developed to showcase skills in modern web application development, including user authentication, database integration, and RESTful API implementation. The system efficiently manages orders with defined roles for administrators, users, and visitors.

### Project Objectives  
- Build a functional and interactive order management system.  
- Demonstrate concepts like authentication, authorization, and data manipulation.  
- Use best practices for version control and documentation.  

---

## 2. Project Requirements  
### Necessary Features  
1. An attractive home page introducing the company.  
2. User registration and login with role-based access control.  
3. Display data stored in three different database tables.  
4. A functional contact form with server-side validation.  
5. Implement a RESTful API with full CRUD operations.  
6. Version control on GitHub with at least five meaningful commits.  
7. Detailed documentation with screenshots explaining each feature.  

---

## 3. General Project Structure  

### 3.1 Technologies Used  
- **Frontend:** HTML5, CSS3, Bootstrap  
- **Backend:** Java (Spring Boot), RESTful API  
- **Database:** MySQL  
- **Version Control:** GitHub  

### 3.2 Folder Structure  

---

## 4. Database  

### 4.1 Table Structures  
#### Users Table  
- **id** (PK, auto_increment): Unique identifier.  
- **name**: User's name.  
- **email** (UNIQUE): User's email address.  
- **password**: Encrypted password.  
- **role**: User role (Admin, User, Visitor).  
- **created_at**: Account creation timestamp.  

#### Order Table  
- **id** (PK): Unique identifier.  
- **pizzaname**: Name of the pizza.  
- **amount**: Ordered quantity.  
- **taken**: Status (prepared or not).  
- **dispatched**: Dispatch status.  

#### Pizza Table  
- **id** (PK): Unique identifier.  
- **pname**: Pizza name.  
- **categoryname**: Pizza category.  
- **vegetarian**: Indicates if the pizza is vegetarian (boolean).  

#### Category Table  
- **cname** (PK): Category name.  
- **price**: Average price of the category.  

### 4.2 Table Relationships  
- **Orders → Users:** A user can place multiple orders (1:N).  
- **Pizzas → Categories:** Each pizza belongs to one category (N:1).  

---

## 5. Implemented Features  

### 5.1 Home Page  
The home page introduces the system and includes navigation links for registration, login, and other key pages.  

### 5.2 Registration and Login  
- **Registration:** Allows new users to create an account.  
- **Login:** Grants access to the system with credential validation.  

### 5.3 User Roles  
- **Admin:** Full access, including user management.  
- **User:** Can place orders and view statuses.  
- **Visitor:** Limited access to public pages.  

### 5.4 Data Display  
Displays data from three database tables, such as orders, pizzas, and categories.  

### 5.5 Contact Form  
Includes a functional contact form with server-side validation.  

### 5.6 Stored Messages  
Displays contact form messages in reverse chronological order, showing the sender’s identity or “Guest” if not logged in.  

---

## 6. RESTful API  

### Available Endpoints  
#### Users  
- `GET /api/users` - Retrieves all users.  
- `POST /api/users` - Adds a new user.  

#### Orders  
- `GET /api/orders` - Retrieves all orders.  
- `POST /api/orders` - Creates a new order.  

### Testing with cURL and Postman  
#### cURL Examples  
```bash
curl -X GET http://localhost:8080/api/orders  
curl -X GET http://localhost:8080/api/pizzas  
curl -X GET http://localhost:8080/api/categories  
Postman Examples
List Categories
List Pizzas
List Orders
Create a New Category
7. GitHub Usage
Commit Structure
Each feature was implemented with meaningful commits and descriptive messages.

Repository Organization
The repository follows a structured layout, with separate folders for source code, database files, and documentation.

8. Screenshots
Home Page
Registration Form
Data Display
(Include actual image files in the screenshots/ folder and reference them here.)
9. Conclusion
This project demonstrates advanced skills in web development, showcasing modern practices in authentication, role management, and API design.

10. Future Improvements
Add detailed reporting features.
Integrate with external APIs for expanded functionality.
yaml
Copy code

---

---

### **Steps to Add This to GitHub**
1. Copy this into a `README.md` file.
2. Place the file in your project’s root directory.
3. Commit the file:
   ```bash
   git add README.md
   git commit -m "Add project documentation"
   git push
