# Fintech-Microservices-Platform
A scalable fintech microservices platform supporting wallet, UPI payments, and transaction processing using Spring Boot, Kafka, Redis, and REST APIs


# 📌 Fintech Microservices Platform

A scalable, secure, and event-driven digital payment system inspired by fintech applications (like Paytm), built using Spring Boot Microservices architecture. The system supports wallet management, UPI payments, and transaction processing.

---

## 🚀 Features

- JWT-based Authentication & Authorization  
- Wallet Management (Add / Withdraw / Balance)  
- Transaction Processing (Debit / Credit / History)  
- UPI Payment Simulation  
- Event-driven architecture using Kafka  
- Redis for caching & distributed locking  
- Swagger API documentation  
- Unit testing (JUnit, Mockito)  
- Docker support  

---

## 🏗️ Architecture
            ┌──────────────┐
            │ API Gateway  │
            └──────┬───────┘
                   │
┌──────────────┬──────────────┬──────────────┬──────────────┐
│ Auth Service │ Wallet Service │ Transaction Service │ UPI Service │
└──────────────┴──────────────┴──────────────┴──────────────┘
│
┌──────────────┐
│ Kafka Broker │
└──────────────┘
│
┌──────────────┐
│ Redis Cache │
└──────────────┘

---

## 🧩 Services

### Auth Service
- User registration & login  
- JWT token generation  
- API security  

### Wallet Service
- Create wallet  
- Add / withdraw money  
- Check balance  
- Redis locking for concurrency  

### Transaction Service
- Debit / credit operations  
- Transaction history  
- Kafka-based updates  

### UPI Service
- UPI payment simulation  
- Kafka event publishing  

---

## ⚙️ Tech Stack

- Java 8  
- Spring Boot  
- Spring Security + JWT  
- Apache Kafka  
- Redis  
- MySQL  
- Maven  
- Swagger  
- JUnit, Mockito  
- Docker  

---

## 📦 API Endpoints

### Auth

POST /auth/register
POST /auth/login

### Wallet

POST /wallet/add
POST /wallet/withdraw
GET /wallet/balance


### Transaction

GET /transaction/history


### UPI

POST /upi/pay

🔄 Kafka Flow
UPI Service sends event
Kafka publishes
Transaction Service consumes
Wallet updates balance
Status updated

🔐 Security Flow
Login → JWT token generated
Token passed in headers
Services validate token

⚡ Concurrency
Redis distributed locking
Prevents race conditions
Ensures consistency


fintech-microservices-platform/
├── auth-service/
├── wallet-service/
├── transaction-service/
├── upi-service/
├── api-gateway/
├── common-lib/
└── docker-compose.yml


🧠 Concepts
Microservices
Event-driven architecture
Distributed locking
Idempotency
Exception handling
REST API design


📈 Future Scope
API Gateway
Eureka Service Discovery
Circuit Breaker
CI/CD Pipeline

👨‍💻 Author

Nand Lal Verma
Java Full Stack Developer
