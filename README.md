# 🏡 Airbnb Clone Project

## 🚀 Overview
The Airbnb Clone Project is a comprehensive full-stack web application designed to simulate the functionality of the Airbnb platform.  
It focuses on backend development, database design, API creation, and application security.

## 🎯 Project Goals
- Build a secure and scalable backend architecture.
- Manage users, property listings, bookings, payments, and reviews.
- Implement authentication and authorization systems.
- Design relational database schemas using MySQL.
- Document APIs using the OpenAPI standard.
- Integrate CI/CD pipelines for automated deployment.

## ⚙️ Tech Stack
- **Backend Framework:** Django  
- **Database:** MySQL  
- **API Development:** Django REST Framework & GraphQL  
- **Caching & Async Tasks:** Redis & Celery  
- **Containerization:** Docker  
- **Version Control:** Git & GitHub  
- **CI/CD:** GitHub Actions  

### Backend Developer
Responsible for implementing the core logic of the application, including API endpoints, authentication, and business rules. Ensures data integrity and efficient communication between the frontend and the database.

### Database Administrator (DBA)
Designs and manages the project’s relational database. Ensures data consistency, optimizes queries, and implements indexing and backups for performance and reliability.

### DevOps Engineer
Handles deployment, monitoring, and scaling of the backend application. Builds CI/CD pipelines and manages infrastructure using Docker and cloud services.

### QA Engineer
Tests all system functionalities, identifying bugs and ensuring that all project features meet the quality standards before deployment.

### Project Manager
Coordinates the development process, defines milestones, manages communication within the team, and ensures deadlines are met.

## 🗄️ Database Design
### Entities and Attributes

#### 1. User
- id (Primary Key)
- name
- email
- password
- role (host or guest)

#### 2. Property
- id (Primary Key)
- title
- description
- location
- price_per_night
- owner_id (Foreign Key → User)

#### 3. Booking
- id (Primary Key)
- user_id (Foreign Key → User)
- property_id (Foreign Key → Property)
- check_in_date
- check_out_date
- status

#### 4. Payment
- id (Primary Key)
- booking_id (Foreign Key → Booking)
- amount
- payment_method
- payment_status

#### 5. Review
- id (Primary Key)
- property_id (Foreign Key → Property)
- user_id (Foreign Key → User)
- rating
- comment

### Relationships
- A **User** can own multiple **Properties**.  
- A **User** can make multiple **Bookings**.  
- A **Booking** belongs to one **Property** and one **User**.  
- A **Payment** belongs to one **Booking**.  
- A **Review** belongs to one **User** and one **Property**.

## 🧩 Feature Breakdown
### 1. User Management
Allows users to register, log in, and manage their profiles securely using authentication and authorization mechanisms.

### 2. Property Management
Hosts can create, update, and delete their property listings, including details like price, description, and location.

### 3. Booking System
Guests can book available properties, view booking details, and manage check-in/check-out dates.

### 4. Payment Processing
Secure handling of payments associated with bookings, recording transaction details for each completed payment.

### 5. Review System
Users can leave reviews and ratings for properties after their stay, enhancing trust and feedback for future guests.

### 6. API Documentation
APIs are documented using the OpenAPI standard, making integration and testing easy for developers.



## 🔐 API Security
### Authentication
Implements token-based authentication (e.g., JWT) to verify user identity before accessing restricted endpoints.

### Authorization
Ensures users can only perform actions within their permissions — for example, only property owners can modify their listings.

### Data Encryption
Sensitive information like passwords and payment details are encrypted using industry-standard algorithms.

### Rate Limiting
Prevents abuse and DDoS attacks by limiting the number of API requests a user can make within a specific time frame.

### Importance of Security
Security is critical to protect user data, prevent financial fraud, and maintain trust within the platform. All transactions and data communications will be handled over HTTPS.


## ⚙️ CI/CD Pipeline
Continuous Integration (CI) and Continuous Deployment (CD) are development practices that automate the process of testing, building, and deploying software.  
This ensures faster updates, fewer errors, and a more stable application.

### Tools Used
- **GitHub Actions:** Automates testing and deployment workflows.
- **Docker:** Provides isolated environments for consistent builds.
- **Celery & Redis:** Support background tasks in the deployment process.

By using CI/CD, developers can ensure that each code change is tested automatically, integrated smoothly, and deployed efficiently to the production environment.



### 📁 Repository Structure 

## 🧑‍💻 Author
**Kenny Da Silva** – Fullstack Developer  

