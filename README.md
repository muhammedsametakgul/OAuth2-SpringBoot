# OAuth2 Demo Application

This project is a simple demo application that provides OAuth2-based authentication using Spring Boot. It allows users to log in using GitHub and manage authorized users.

## Technologies Used

- **Spring Boot**: A Java-based framework for building web applications.
- **Spring Security**: A Spring module that provides security features.
- **OAuth2**: An authentication and authorization protocol.
- **GitHub OAuth**: A service that provides authentication via GitHub.
- **Thymeleaf**: A server-side template engine used in Java applications.

## Setup and Running

### Prerequisites

- Java 17 or above
- Maven or Gradle
- An IDE (IntelliJ IDEA, Eclipse, etc.)
- Git

### 1. Clone the Repository

First, clone the repository from GitHub:

```bash
git clone https://github.com/muhammedsametakgul/OAuth2-SpringBoot.git
cd oauth2-demo-app
```

To run application, please create application-local.yml and fill the properties. I give you a temlplate below
```bash
spring:
  security:
    oauth2:
      client:
        registration:
          github:
            client-id: ---
            client-secret: ----
            scope: read:user
            redirect-uri: "{baseUrl}/login/oauth2/code/{registrationId}"
