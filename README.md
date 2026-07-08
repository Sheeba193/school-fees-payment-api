
# ShulePay

> **A production-ready school fees payment platform built with Spring Boot and the M-PESA Daraja API.**

---

## **Overview**

ShulePay is a full-stack application that demonstrates how to build secure, scalable, and maintainable payment integrations using the M-PESA Daraja API. It is being developed as part of the JVM Community Challenge with a focus on production-ready backend engineering.

---

## **Objectives**

- Learn Spring Boot fundamentals.
- Build a clean REST API.
- Integrate the M-PESA Daraja STK Push API.
- Handle payment callbacks securely.
- Apply validation, logging, testing, and documentation best practices.
- Build a portfolio-quality project.

---

## **Tech Stack**

### **Backend**
- Java
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Maven
- JUnit & Mockito
- OpenAPI / Swagger

### **Frontend**
- React
- Vite
- Tailwind CSS
- Axios

---

## **Project Structure**

```text
shulepay/
├── backend/
│   ├── src/
│   ├── pom.xml
│   └── Dockerfile
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
├── docs/
│   ├── architecture.md
│   ├── api.md
│   ├── diagrams/
│   └── screenshots/
├── docker-compose.yml
├── .gitignore
├── README.md
└── LICENSE
```

---

## **Features**

### **Current**
- Student management
- Payment records
- STK Push payment initiation
- Daraja callback processing
- Payment history

### **Planned**
- User authentication
- Admin dashboard
- Student portal
- Docker support
- CI/CD
- Monitoring & metrics

---

## **REST API**

### **Students**
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/v1/students` | Create student |
| GET | `/api/v1/students` | List students |
| GET | `/api/v1/students/{id}` | Get student |
| PUT | `/api/v1/students/{id}` | Update student |
| DELETE | `/api/v1/students/{id}` | Delete student |

### **Payments**
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/v1/payments/stk-push` | Initiate STK Push |
| POST | `/api/v1/payments/callback` | Receive Daraja callback |
| GET | `/api/v1/payments/{id}` | Get payment details |

---

## **Environment Variables**

Required configuration:

- `DARAJA_CONSUMER_KEY`
- `DARAJA_CONSUMER_SECRET`
- `DARAJA_SHORTCODE`
- `DARAJA_PASSKEY`
- `CALLBACK_URL`
- `DB_URL`
- `DB_USERNAME`
- `DB_PASSWORD`

> Never commit secrets to version control.

---

## **Getting Started**

### **1. Clone the Repository**

```bash
git clone <repository-url>
cd shulepay
```

### **2. Run the Backend**

```bash
cd backend
mvn spring-boot:run
```

### **3. Run the Frontend**

```bash
cd frontend
npm install
npm run dev
```

---

## **Roadmap**

- [ ] Project setup
- [ ] Student module
- [ ] Payment module
- [ ] Daraja authentication
- [ ] STK Push integration
- [ ] Callback handling
- [ ] Testing
- [ ] Docker
- [ ] CI/CD
- [ ] Deployment

---

## **Documentation**

Project documentation will be available in the `docs/` directory:

- Architecture
- API Reference
- Setup Guide
- Screenshots
- Diagrams

---

## **License**

Licensed under the **MIT License**.
