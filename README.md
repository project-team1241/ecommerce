# ecommerce

<details>
    <summary>Project Structure</summary>

    ecommerce-microservices/
    │
    ├── pom.xml (Parent POM for Maven) / build.gradle (for Gradle)
    │
    ├── graven-user/                    # User service (authentication, profile)
    │   ├── src/
    │   │   ├── main/
    │   │   │   ├── java/
    │   │   │   │   ├── com/
    │   │   │   │   │   └── ecommerce/
    │   │   │   │   │       └── user/
    │   │   │   │   │           ├── UserServiceApplication.java
    │   │   │   │   │           ├── controller/
    │   │   │   │   │           │   └── UserController.java
    │   │   │   │   │           ├── model/
    │   │   │   │   │           │   └── User.java
    │   │   │   │   │           ├── repository/
    │   │   │   │   │           │   └── UserRepository.java
    │   │   │   │   │           ├── service/
    │   │   │   │   │           │   └── UserService.java
    │   │   │   │   │           └── config/
    │   │   │   │   │               └── SecurityConfig.java
    │   │   │   └── resources/
    │   │   │       ├── application.yml
    │   │   │       └── application-dev.yml
    │   │   └── test/
    │   └── pom.xml (for Graven User Service)
    │
    ├── graven-product/                 # Product catalog service
    │   ├── src/
    │   │   ├── main/
    │   │   │   ├── java/
    │   │   │   │   ├── com/
    │   │   │   │   │   └── ecommerce/
    │   │   │   │   │       └── product/
    │   │   │   │   │           ├── ProductServiceApplication.java
    │   │   │   │   │           ├── controller/
    │   │   │   │   │           │   └── ProductController.java
    │   │   │   │   │           ├── model/
    │   │   │   │   │           │   └── Product.java
    │   │   │   │   │           ├── repository/
    │   │   │   │   │           │   └── ProductRepository.java
    │   │   │   │   │           └── service/
    │   │   │   │   │               └── ProductService.java
    │   │   │   └── resources/
    │   │   │       ├── application.yml
    │   │   │       └── application-dev.yml
    │   │   └── test/
    │   └── pom.xml (for Graven Product Service)
    │
    ├── graven-order/                   # Order management service
    │   ├── src/
    │   │   ├── main/
    │   │   │   ├── java/
    │   │   │   │   ├── com/
    │   │   │   │   │   └── ecommerce/
    │   │   │   │   │       └── order/
    │   │   │   │   │           ├── OrderServiceApplication.java
    │   │   │   │   │           ├── controller/
    │   │   │   │   │           │   └── OrderController.java
    │   │   │   │   │           ├── model/
    │   │   │   │   │           │   └── Order.java
    │   │   │   │   │           ├── repository/
    │   │   │   │   │           │   └── OrderRepository.java
    │   │   │   │   │           └── service/
    │   │   │   │   │               └── OrderService.java
    │   │   │   └── resources/
    │   │   │       ├── application.yml
    │   │   │       └── application-dev.yml
    │   │   └── test/
    │   └── pom.xml (for Graven Order Service)
    │
    ├── graven-payment/                 # Payment processing service
    │   ├── src/
    │   │   ├── main/
    │   │   │   ├── java/
    │   │   │   │   ├── com/
    │   │   │   │   │   └── ecommerce/
    │   │   │   │   │       └── payment/
    │   │   │   │   │           ├── PaymentServiceApplication.java
    │   │   │   │   │           ├── controller/
    │   │   │   │   │           │   └── PaymentController.java
    │   │   │   │   │           └── service/
    │   │   │   │   │               └── PaymentService.java
    │   │   │   └── resources/
    │   │   │       ├── application.yml
    │   │   │       └── application-dev.yml
    │   │   └── test/
    │   └── pom.xml (for Graven Payment Service)
    │
    ├── api-gateway/                    # API Gateway to route requests
    │   ├── src/
    │   │   ├── main/
    │   │   │   ├── java/
    │   │   │   │   ├── com/
    │   │   │   │   │   └── ecommerce/
    │   │   │   │   │       └── gateway/
    │   │   │   │   │           └── ApiGatewayApplication.java
    │   │   │   └── resources/
    │   │   │       ├── application.yml
    │   │   │       └── application-dev.yml
    │   │   └── test/
    │   └── pom.xml (for API Gateway)
    │
    ├── config-server/                  # Centralized configuration service
    │   ├── src/
    │   │   ├── main/
    │   │   │   ├── java/
    │   │   │   │   ├── com/
    │   │   │   │   │   └── ecommerce/
    │   │   │   │   │       └── config/
    │   │   │   │   │           └── ConfigServerApplication.java
    │   │   │   └── resources/
    │   │   │       └── application.yml
    │   │   └── test/
    │   └── pom.xml (for Config Server)
    │
    └── shared-lib/                     # Common libraries, utilities, and models (optional)
        ├── src/
        │   ├── main/
        │   │   ├── java/
        │   │   │   ├── com/
        │   │   │   │   └── ecommerce/
        │   │   │   │       └── common/
        │   │   │   │           ├── utils/
        │   │   │   │           └── model/
        │   │   └── resources/
        └── pom.xml (shared utilities for microservices)


</details>

# 🌟 E-Commerce Backend

![Project Logo](https://via.placeholder.com/728x90.png?text=E-Commerce+Backend)

An advanced **Spring Boot** backend application for e-commerce platforms. This project implements secure authentication and authorization using **JWT**, **OAuth**, and **Spring Security**, and is ready for scalable deployments using Docker.

---

## 🚀 Features

- 🛡️ **Secure APIs**: Authentication and authorization with **JWT** & **OAuth**.
- 👥 **Role-Based Access Control**: Restrict access to specific APIs.
- 📦 **Product Management**: CRUD operations for products.
- 📜 **Order Management**: Handle orders seamlessly.
- 🐳 **Dockerized Deployment**: Easy containerization using **Docker Compose**.
- ⚡ **High Performance**: Optimized for scalability and extensibility.

---

## 🛠️ Tech Stack

| **Technology**     | **Version**   | **Purpose**                     |
|---------------------|---------------|----------------------------------|
| **Java**           | 21+           | Core development language       |
| **Spring Boot**    | Latest        | Backend framework               |
| **Spring Security**| Latest        | Authentication & Authorization  |
| **JWT & OAuth**    | Latest        | Secure token-based auth         |
| **Maven**          | Latest        | Build and dependency management |
| **Docker**         | Latest        | Containerization                |
| **Docker Compose** | Latest        | Multi-container orchestration   |

---

## 📖 Getting Started

### Prerequisites

Ensure the following are installed:
- **Java** (JDK 21 or higher)
- **Maven**
- **Docker Desktop** or another Docker client  [0ptional]

### Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/ecommerce-backend.git
   cd ecommerce-backend
   ```
** Note : Try to use our dev/test db in the .evn-dev

   ```bash
   mvn clean install -DskipTests
   mvn clean package -DskipTests
   ```

   ```bash
   mvn spring-boot:run
   ```
---

### Docker

   ```bash
   docker-compose up --build
   docker-compose down

   docker tag ecommerce-backend <your-registry>/<project-name>:latest
   docker push <your-registry>/<project-name>:latest
   ```
---

