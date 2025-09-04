# 📚 Bookstore Project

A full-stack **Bookstore Management System** built with **Spring Boot microservices** and **Angular 20** frontend.  
This project demonstrates **REST API design, JWT authentication, microservices architecture, database management, and frontend integration**.

---

## 🚀 Tech Stack

- **Backend (Microservices)**:
  - Java 21
  - Spring Boot 3
  - Spring Data JPA
  - MySQL
  - JWT Authentication
  - Maven
- **Frontend**:
  - Angular 20
  - TypeScript
  - Forms, Routing, HttpClient
  - TailwindCSS (optional)
- **Database**:
  - H2 (for now)
  - Later: MySQL (one DB per service) 
- **Tools**:
  - Git
  - Docker (optional, for multi-service orchestration)
  - VS Code (currently using) / IntelliJ IDEA

---

## 🌟 Features

- **User Service**
  - Register/Login
  - JWT-based authentication
  - Role-based access (Admin/Customer)
  
- **Book Service**
  - Add, Update, Delete, List books
  - Search by title, author, genre
  - Manage stock
  - REST API exposed to frontend

- **Order Service**
  - Cart management
  - Place orders
  - Track order status
  - Integrates with User & Book services

- **Frontend (Angular 20)**
  - Browse books
  - Add new books (Admin)
  - Responsive UI with routing
  - Communicates with backend services via REST API

---

## 🔧 Setup Instructions

### 1. Clone repository
```
git clone <your-repo-url>
cd bookstore-project
```

### 2. Backend Services

For each service (book-service, user-service, order-service):

1. Go to the service folder:

```
cd services/book-service
```

2.  Update src/main/resources/application.properties with your MySQL credentials:

```
spring.datasource.url=jdbc:mysql://localhost:3306/book_db

spring.datasource.username=root

spring.datasource.password=yourpassword

spring.jpa.hibernate.ddl-auto=update
```

3. Run the service:

```
./mvnw spring-boot:run
```

4. Services run on separate ports:

```
Book Service: 8081

User Service: 8082

Order Service: 8083
```

Optional: use Docker Compose to start all services + databases at once.


### 3. Frontend (Angular 20)

1. Navigate to the frontend folder:

```
cd frontend
```

2. Install dependencies:

```
npm install
```

3. Set backend API URLs in Angular environment files:

```
// src/environments/environment.ts
export const environment = {
  production: false,
  apiUrl: 'http://localhost:8081' // Book service
};
```

4. Run Angular dev server:

```
ng serve --port 4200
```
Frontend available at: http://localhost:4200

### 📜 License

MIT License

