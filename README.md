✈️ TripSync – Travel Management System

TripSync is a comprehensive travel management platform built using a microservices architecture. It enables users to explore travel destinations, book tour packages, complete secure payments, and provide feedback on their travel experiences.

The project demonstrates real-world implementation of Spring Boot microservices, API Gateway routing, JWT-based security, and modern React frontend integration.

👨‍💻 Developed By

Adarsh Mani

Rishi Dattatray Dusane

🚀 Architecture Overview

TripSync follows a microservices-based backend with a React frontend.

Frontend: React 19 + Vite

Backend: Java Spring Boot Microservices

Communication: REST APIs via API Gateway

Authentication: JWT-based security

Payments: Stripe integration

🏗️ Backend Microservices

The backend uses a parent–child Maven structure and consists of the following services:

🔹 API Gateway (Port: 8090)

Acts as the single entry point

Routes incoming requests to appropriate microservices

Centralized request handling

🔹 Auth Service (Port: 8081)

User registration and login

JWT-based authentication

Forgot password & reset password flow with token validation

🔹 Catalog Service (Port: 8082)

Manages travel destinations and tour packages

CRUD operations for travel offerings

Admin-controlled package management

🔹 Booking Service (Port: 8083)

Handles booking lifecycle

Integrates Stripe payment gateway

Automatically confirms booking after successful payment

🔹 Feedback Service (Port: 8084)

User reviews and ratings (1–5 scale)

View feedback by user or by package

Review management APIs

🎨 Frontend

The frontend is built using React 19 and Vite, ensuring fast builds and smooth UI performance.

Key Frontend Technologies

React Router for navigation

Axios for API communication

Modular component-based UI

🛠️ Tech Stack
Backend

Java 21

Spring Boot 3.2.1

Spring Cloud 2023.0.0

Spring Security

JWT (JSON Web Token)

Maven

Frontend

React 19

Vite 7

React Router 7

Axios

CSS

Payments

Stripe

📂 Project Routes & Structure
Backend Routing (via API Gateway)
Service	Route Path	Port
Auth Service	/api/auth/**	8081
Catalog	/api/destinations/**, /api/packages/**	8082
Booking	/api/bookings/**, /api/payments/**	8083
Feedback	/api/reviews/**	8084
Frontend Pages

/ – Landing Page

/login, /signup – User Authentication

/dashboard – Main user interface

/packages/:destinationId – View tour packages

/my-bookings – Booking history

/admin – Admin-only protected routes

✨ Key Features

JWT Authentication with secure login & registration

Forgot Password flow with email-based reset tokens

Tour Catalog Management with admin controls

Real-time Booking & Payment Processing

Stripe Payment Integration

Automatic Booking Confirmation

User Feedback & Rating System

Role-Based Access Control (Admin/User)

⚙️ Installation & Setup
Backend Setup
Prerequisites

Java 21

Maven

Steps
cd backend/travel
mvn clean install


Run each microservice individually:

Auth Service

Catalog Service

Booking Service

Feedback Service

API Gateway

Frontend Setup
cd frontend
npm install
npm run dev

🎯 Learning Outcomes

Designed and implemented Spring Boot microservices

Implemented API Gateway & service routing

Secured APIs using JWT & Spring Security

Integrated Stripe payment gateway

Built a scalable React + REST API system

Followed enterprise-grade backend architecture

📌 Future Enhancements

Centralized logging and monitoring

Docker containerization

Config Server for centralized configuration

Cloud deployment (AWS / Azure)

Email notifications for bookings

🌍 TripSync

Streamlining your travel experiences with scalable microservices architecture.
Email notifications for bookings


