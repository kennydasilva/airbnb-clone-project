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



### 📁 Repository Structure 

## 🧑‍💻 Author
**Kenny Da Silva** – Fullstack Developer  

