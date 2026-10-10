# ShulePay

A secure, scalable school fees payment platform for schools that want to collect tuition and other charges digitally using M-Pesa Daraja.

ShulePay is designed to simplify fee collection with a clean REST API, reliable payment processing, and an architecture that can grow from a small school system into a broader education payments platform.

## Why this project?

Many schools still rely on manual fee collection, which is slow, error-prone, and difficult to audit. ShulePay aims to provide a simple digital alternative that:

- allows students and administrators to track fee records clearly;
- supports secure mobile-money payment initiation via M-Pesa STK Push;
- reduces payment delays and manual reconciliation work;
- creates a foundation for future school administration features.

## Project goals

- Build a production-ready backend API with Spring Boot;
- Integrate M-Pesa Daraja for real-world payment flows;
- Handle payment callbacks securely and reliably;
- Manage student and payment data with clean persistence models;
- Document architecture and API usage for future extension.

## Core features

### Current capabilities

- Student registration and record management;
- Fee payment tracking;
- M-Pesa STK Push payment initiation;
- Callback handling for transaction status updates;
- Payment history retrieval;
- API-first design with documentation in mind.

### Planned capabilities

- Administrator authentication and authorization;
- Student portal access;
- Admin dashboard for payment monitoring;
- Email and notification workflows;
- Dockerized deployment;
- CI/CD automation;
- Monitoring, metrics, and observability.

## Architecture overview

This project follows a modular, API-first architecture based on a Java backend and a frontend client.

The repository currently includes the foundational project documentation and architecture reference, while the implementation work can be expanded into dedicated backend/frontend modules as the project evolves.

See:

- `system-architecture.md` for the system diagram and architecture overview;
- `docs/architecture.md` for architectural notes;
- `docs/api.md` for API reference material.

## Tech stack

### Backend

- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA
- PostgreSQL
- Maven
- JUnit 5
- Mockito
- OpenAPI / Swagger

### Frontend

- React
- Vite
- Tailwind CSS
- Axios

## Repository structure

```text
school-fees-payment-api/
├── README.md
├── LICENSE
├── .gitignore
├── system-architecture.md
├── docs/
│   ├── architecture.md
│   ├── api.md
│   └── learning-journal.md
└── .github/                  # optional project automation and workflows
```

> The project is designed to evolve into a backend + frontend application, but the current repository focuses on the design and planning foundation for the platform.

## API overview

### Students

| Method | Endpoint | Description |
| --- | --- | --- |
| POST | `/api/v1/students` | Create a new student record |
| GET | `/api/v1/students` | List all students |
| GET | `/api/v1/students/{id}` | Get a single student by ID |
| PUT | `/api/v1/students/{id}` | Update a student record |
| DELETE | `/api/v1/students/{id}` | Delete a student record |

### Payments

| Method | Endpoint | Description |
| --- | --- | --- |
| POST | `/api/v1/payments/stk-push` | Initiate an M-Pesa STK Push transaction |
| POST | `/api/v1/payments/callback` | Receive and process Daraja callback data |
| GET | `/api/v1/payments/{id}` | Retrieve payment details |

## Environment variables

The application requires the following configuration values before running in a real environment:

- `DARAJA_CONSUMER_KEY`
- `DARAJA_CONSUMER_SECRET`
- `DARAJA_SHORTCODE`
- `DARAJA_PASSKEY`
- `CALLBACK_URL`
- `DB_URL`
- `DB_USERNAME`
- `DB_PASSWORD`

> Never commit credentials or secrets to version control. Use environment variables or a secure secrets manager in production.

## Getting started

### 1. Clone the repository

```bash
git clone https://github.com/Sheeba193/school-fees-payment-api.git
cd school-fees-payment-api
```

### 2. Configure environment variables

Create a local `.env` file or set the required environment variables before starting the backend.

### 3. Start the backend

```bash
cd backend
mvn spring-boot:run
```

### 4. Start the frontend

```bash
cd frontend
npm install
npm run dev
```

## Roadmap

- [x] Project concept and architecture foundation
- [x] Student module planning
- [x] Payment module planning
- [x] Daraja integration design
- [x] STK Push payment flow design
- [x] Callback processing design
- [ ] Authentication and authorization
- [ ] Admin dashboard
- [ ] Student portal
- [ ] Docker support
- [ ] CI/CD pipeline
- [ ] Production deployment
- [ ] Monitoring and logging

## Documentation

Project documentation lives in the repository under the `docs/` folder and in the root architecture document:

- `system-architecture.md`
- `docs/architecture.md`
- `docs/api.md`
- `docs/learning-journal.md`

## Contributing

Contributions are welcome. If you want to improve the project:

1. Fork the repository.
2. Create a feature branch.
3. Implement the change and document it.
4. Open a pull request with a clear description of the improvement.

## License

This project is licensed under the MIT License.

---

Built to demonstrate a realistic, portfolio-ready approach to integrating M-Pesa payments into a school management workflow.
