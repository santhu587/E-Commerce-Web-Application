This is a full-stack e-commerce application built using Spring Boot, Spring Data JPA, MySQL, and Thymeleaf. 
It supports basic e-commerce functionalities like product listing,
user registration, shopping cart management, and order processing.
Installation
Prerequisites
JDK 8 or later
Maven
MySQL server
IDE (STS, IntelliJ, or Eclipse)
Configure the Database:

Create a MySQL database named ecommerce_db.
Update the application.properties file with your MySQL username and password:
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
Build and Run the Application:

bash
Copy code
mvn clean install
mvn spring-boot:run
Access the Application:

Open your browser and go to http://localhost:8080.
API Endpoints
User Authentication
POST /register - Register a new user.
POST /login - Authenticate and get JWT token.
Product Management
GET /products - Get all products.
GET /products/{id} - Get a product by ID.
POST /products - Add a new product (Admin).
PUT /products/{id} - Update a product (Admin).
DELETE /products/{id} - Delete a product (Admin).
Shopping Cart
POST /cart/add - Add a product to the cart.
GET /cart - View the shopping cart.
POST /cart/remove - Remove a product from the cart.
Order Management
POST /order - Place a new order.
GET /order - View order history.
PUT /order/{id}/status - Update order status (Admin).
