# Food Ordering System

A full-stack web application for food ordering with React frontend and Spring Boot backend.

## Features

### Customer Features
- User registration and login with JWT authentication
- Browse food items by category and restaurant
- Search and filter food items
- View food details (price, description, rating, availability)
- Add items to cart, increase/decrease quantity, remove items
- Place orders and view order summary
- Track order status
- View order history
- Provide ratings and reviews for food

### Admin Features
- Secure login
- Add, update, delete food items
- Manage food categories and restaurants
- View all users and orders
- Update order status
- View analytics (total orders, revenue, popular items)

## Tech Stack

- **Backend**: Spring Boot, Spring Security, JWT, MongoDB
- **Frontend**: React, React Router, Axios
- **Database**: MongoDB

## Setup Instructions

### Backend

1. Ensure MongoDB is running on localhost:27017
2. Navigate to `food-ordering` directory
3. Run `mvn spring-boot:run`

### Frontend

1. Navigate to `frontend` directory
2. Run `npm install`
3. Run `npm start`

The application will be available at:
- Backend API: http://localhost:8080
- Frontend: http://localhost:3000

## API Endpoints

### Authentication
- POST /api/auth/register
- POST /api/auth/login

### Foods
- GET /api/foods
- GET /api/foods/{id}
- POST /api/foods (Admin)
- PUT /api/foods/{id} (Admin)
- DELETE /api/foods/{id} (Admin)

### Categories
- GET /api/categories
- POST /api/categories (Admin)
- PUT /api/categories/{id} (Admin)
- DELETE /api/categories/{id} (Admin)

### Cart
- GET /api/cart
- POST /api/cart/add
- PUT /api/cart/update
- DELETE /api/cart/clear

### Orders
- POST /api/orders
- GET /api/orders
- PUT /api/orders/{orderId}/status (Admin)
- GET /api/orders/admin (Admin)

### Reviews
- POST /api/reviews
- GET /api/reviews/food/{foodId}
- GET /api/reviews

### Admin
- GET /api/admin/users
- GET /api/admin/orders
- GET /api/admin/analytics

## Security
- JWT-based authentication
- Role-based access control (CUSTOMER, ADMIN)
- Password encryption with BCrypt