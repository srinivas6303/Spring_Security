# Spring Security Implementations

This repository demonstrates different authentication mechanisms using **Spring Security** in a Spring Boot application.
It contains three branches, each implementing a specific authentication strategy.

---

## Branches

### 1. `sessionbaseAuth` (Default Branch)
- **Description:** Implements **Session-Based Authentication**.
- **How it works:**
  - The client sends credentials (username & password) to the server.
  - If valid, the server creates a **session** and returns a **session ID** to the client.
  - The session ID is sent back in **cookies** for subsequent requests.
- **Type:** Stateful authentication

---

### 2. `basic-auth`
- **Description:** Implements **Basic Authentication**.
- **How it works:**
  - Each request carries the **username and password** in the **Authorization header** (Base64 encoded).
  - No session is maintained on the server; each request is **stateless**.
- **Type:** Stateless authentication

---

### 3. `jwt`
- **Description:** Implements **JWT (JSON Web Token) Authentication**.
- **How it works:**
  - Upon successful login, the server generates a **JWT token** and sends it to the client.
  - The client includes the token in the **Authorization header** for subsequent requests.
  - The server validates the token for each request.
- **Type:** Stateless authentication using tokens

---

## Technologies Used
- Java 17
- Spring Boot 3.x
- Spring Security 6+
- Maven
- JWT (io.jsonwebtoken library)

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/srinivas6303/spring_security.git
   
Checkout the desired branch:
bash
git checkout sessionbaseAuth
# or
git checkout basic-auth
# or
git checkout jwt

## Run the application:
Test endpoints using Postman or any API client.

## Notes
Session-Based Auth: Good for web applications where the server maintains state.
Basic Auth: Simple and stateless; recommended over HTTPS only.
JWT: Suitable for REST APIs and microservices; stateless and scalable.

## Author
Srinivas Dappu
GitHub: [https://github.com/username](https://github.com/srinivas6303)
LinkedIn: [https://www.linkedin.com/in/dappusrinivas/](https://www.linkedin.com/in/dappusrinivas/)
Portfolio: https://dappusrinivas.netlify.app/






