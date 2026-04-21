# FlowKart

> E-commerce order orchestration platform built with **Camunda 8**, **Java 21**, **Spring Boot 3**, and **microservices**.

![Java](https://img.shields.io/badge/Java-21-blue?logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2-brightgreen?logo=springboot)
![Camunda](https://img.shields.io/badge/Camunda-8.5-orange)
![License](https://img.shields.io/badge/License-Apache%202.0-blue)

---

## What is FlowKart?

FlowKart is the companion project for the Udemy course  
**"Camunda 8 with Java & Spring Boot: Real-World BPM & Microservices"**.

It demonstrates how to orchestrate a complete e-commerce order lifecycle  
using Camunda 8 as the workflow engine — from order placement through  
payment, fulfillment, and returns.

---

## What you will build

- Order placement → inventory check → payment → shipping → delivery
- Payment failure handling with compensation (saga pattern)
- Return & refund workflow with DMN decision tables
- Timer-based order auto-cancellation
- Email notifications via Camunda message events
- Live process monitoring in Camunda Operate

---

## Architecture

| Service | Port | Role |
|---|---|---|
| flowkart-gateway | 8080 | API entry point |
| flowkart-order | 8081 | Camunda 8 orchestrator |
| flowkart-inventory | 8082 | Stock management |
| flowkart-payment | 8083 | Payment processing |
| flowkart-notify | 8084 | Notifications |
| flowkart-return | 8085 | Returns & refunds |

---

## Tech stack

- **Camunda 8** (Zeebe, Operate, Tasklist, Modeler)
- **Java 21** + **Spring Boot 3.2**
- **Spring Data JPA** + H2 (dev) / PostgreSQL (prod)
- **Maven multi-module** project structure
- **REST APIs** with SpringDoc OpenAPI / Swagger

---

## Quick start

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/flowkart.git
cd flowkart

# 2. Copy and fill in Camunda credentials
cp .env.example .env

# 3. Build all modules
mvn clean install -DskipTests

# 4. Run the order service
cd flowkart-order
mvn spring-boot:run
```

---

## Course branches

Each Git branch is the **starting point** for a course section:

| Branch | Section |
|---|---|
| s01-environment-setup | Section 1 — Setup |
| s02-order-bpmn-basics | Section 2 — First BPMN |
| s03-inventory-service | Section 3 — Inventory |
| s04-payment-error-handling | Section 4 — Payments |
| s05-notification-messaging | Section 5 — Messaging |
| s06-return-dmn | Section 6 — Returns & DMN |
| s07-advanced-features | Section 7 — Advanced |
| s08-capstone-complete | Section 8 — Capstone |

---

## License

Apache License 2.0 — see [LICENSE](LICENSE)
