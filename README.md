# ecommerce
<details>
    <summary>Project Structure</summary>
```
ecommerce/
│
├── pom.xml                      # Parent POM for Maven (shared dependencies and plugin configurations)
│
├── user-service/                # User service (authentication, profile)
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   ├── com/
│   │   │   │   │   └── ecommerce/
│   │   │   │   │       └── user/
│   │   │   │   │           ├── UserServiceApplication.java   # @SpringBootApplication
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
│   │   │       ├── application.yml   # Configuration file
│   │   │       └── application-dev.yml
│   └── pom.xml                     # User Service POM
│
├── product-service/              # Product catalog service
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   ├── com/
│   │   │   │   │   └── ecommerce/
│   │   │   │   │       └── product/
│   │   │   │   │           ├── ProductServiceApplication.java  # @SpringBootApplication
│   │   │   │   │           ├── controller/
│   │   │   │   │           │   └── ProductController.java
│   │   │   │   │           ├── model/
│   │   │   │   │           │   └── Product.java
│   │   │   │   │           ├── repository/
│   │   │   │   │           │   └── ProductRepository.java
│   │   │   │   │           └── service/
│   │   │   │   │               └── ProductService.java
│   │   │   └── resources/
│   │   │       ├── application.yml   # Configuration file
│   │   │       └── application-dev.yml
│   └── pom.xml                     # Product Service POM
│
├── order-service/                # Order management service
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   ├── com/
│   │   │   │   │   └── ecommerce/
│   │   │   │   │       └── order/
│   │   │   │   │           ├── OrderServiceApplication.java  # @SpringBootApplication
│   │   │   │   │           ├── controller/
│   │   │   │   │           │   └── OrderController.java
│   │   │   │   │           ├── model/
│   │   │   │   │           │   └── Order.java
│   │   │   │   │           ├── repository/
│   │   │   │   │           │   └── OrderRepository.java
│   │   │   │   │           └── service/
│   │   │   │   │               └── OrderService.java
│   │   │   └── resources/
│   │   │       ├── application.yml   # Configuration file
│   │   │       └── application-dev.yml
│   └── pom.xml                     # Order Service POM
│
├── payment-service/              # Payment processing service
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   ├── com/
│   │   │   │   │   └── ecommerce/
│   │   │   │   │       └── payment/
│   │   │   │   │           ├── PaymentServiceApplication.java  # @SpringBootApplication
│   │   │   │   │           ├── controller/
│   │   │   │   │           │   └── PaymentController.java
│   │   │   │   │           └── service/
│   │   │   │   │               └── PaymentService.java
│   │   │   └── resources/
│   │   │       ├── application.yml   # Configuration file
│   │   │       └── application-dev.yml
│   └── pom.xml                     # Payment Service POM
│
├── api-gateway/                  # API Gateway to route requests
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   ├── com/
│   │   │   │   │   └── ecommerce/
│   │   │   │   │       └── gateway/
│   │   │   │   │           └── ApiGatewayApplication.java   # @SpringBootApplication
│   │   │   └── resources/
│   │   │       ├── application.yml   # Configuration for routing
│   │   │       └── application-dev.yml
│   └── pom.xml                     # API Gateway POM
│
├── config-server/                # Centralized configuration service
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   ├── com/
│   │   │   │   │   └── ecommerce/
│   │   │   │   │       └── config/
│   │   │   │   │           └── ConfigServerApplication.java  # @SpringBootApplication + @EnableConfigServer
│   │   │   └── resources/
│   │   │       └── application.yml   # Configuration file for Config Server
│   └── pom.xml                     # Config Server POM
│
└── shared-lib/                   # Common libraries, utilities, and models (optional)
    ├── src/
    │   ├── main/
    │   │   ├── java/
    │   │   │   ├── com/
    │   │   │   │   └── ecommerce/
    │   │   │   │       └── common/
    │   │   │   │           ├── utils/
    │   │   │   │           └── model/
    │   │   └── resources/
    └── pom.xml                     # Shared Utilities POM
```
</details>