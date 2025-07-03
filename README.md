# 🚀 Node.js Microservice Starter Kit

A production-ready Node.js microservice boilerplate built with **NestJS + TypeScript**, following clean architecture and modular design principles. Designed as part of the **Swaraj** open-source ecosystem, it is suitable for scalable, backend microservices such as `notification`, `process-engine`, and more.

---

## ✨ Features

- Clean Architecture: Clear separation of concerns with layered modular design
- Microservices Ready: Each service is independently deployable
- Multiple Database Support: Works with PostgreSQL, MongoDB, Redis
- API Development: RESTful APIs via NestJS controllers and decorators
- Authentication Ready: Easily integrate JWT-based auth
- Graceful Shutdown: Handles cleanup on termination signals
- Optimized Docker Setup:
  - Multi-stage builds
  - Lightweight images
  - Separate production and development dependencies
  - Health checks and service isolation
- Structured Logging: Custom logger with context support
- Testing: Jest setup with sample test files
- API Versioning: Built-in via route prefixes (e.g., `/api/v1/...`)
- CORS Configured
- Environment-driven Configs using dotenv
- Git Workflow Ready (GitFlow branch strategy)

---

## 📁 Folder Structure

```bash
nodejs-starter-kit/
├── src/
│   ├── main.ts                        # Application entry point
│   ├── app.module.ts                 # Root NestJS module
│   ├── api/                          # API route controllers
│   │   └── v1/
│   │       └── core.controller.ts
│   ├── models/                       # DTOs, interfaces, schemas
│   │   └── core.model.ts
│   ├── repositories/                # DB access layer
│   │   └── core.repository.ts
│   ├── services/                    # Business logic layer
│   │   └── core.service.ts
│   ├── middleware/                  # Guards, interceptors, etc.
│   │   └── logger.middleware.ts
│   ├── utils/                       # Helper functions and constants
│   │   ├── logger.ts
│   │   └── constants.ts
│   ├── config/                      # Config & env setup
│   │   ├── config.module.ts
│   │   ├── config.service.ts
│   │   └── env.validation.ts
│   └── shared/                      # Shared modules (e.g., health)
│       └── health.module.ts
├── services/
│   ├── postgres/
│   │   ├── config/
│   │   ├── init/
│   │   └── docker/
│   ├── mongodb/
│   │   ├── config/
│   │   ├── init/
│   │   └── docker/
│   └── redis/
│       ├── config/
│       └── docker/
├── test/                            # Unit and integration tests
├── .env.example                     # Env variable template
├── .gitignore
├── Dockerfile
├── docker-compose.yml
├── package.json
├── tsconfig.json
├── README.md
```

---

## 📋 Prerequisites

Make sure the following are installed:

- Node.js v18+ (preferably LTS)
- Docker and Docker Compose
- PostgreSQL, MongoDB, Redis (if using those services)

---

## 🔧 Getting Started

```bash
# Clone the repository
git clone <repository-url>
cd nodejs-starter-kit

# Install dependencies
yarn install

# Run development server
yarn start:dev

# Build and run production
yarn build && yarn start:prod

# Run tests
yarn test
```

---

## 🌍 Environment Variables

Copy `.env.example` → `.env` and fill in required variables:

```env
PORT=3000
NODE_ENV=development
DB_HOST=localhost
DB_PORT=5432
...
```

---

## 📚 API Docs

Once server is running:
- Swagger: `/api/v1/docs` (planned)

---

## 🎯 Philosophy

This kit is optimized for **fast MVPs and clean microservice design**. It prioritizes clarity, modularity, and scalability while remaining lightweight enough to be extended into production-grade systems.

---

## 📦 Dependencies

- NestJS
- TypeScript
- class-validator / class-transformer
- PostgreSQL / MongoDB / Redis (optional)
- dotenv, Winston (or pino) for logging
- Jest for testing

---

## 🤝 Git Workflow

We recommend [GitFlow](https://nvie.com/posts/a-successful-git-branching-model/):

- `main`: Production-ready code
- `develop`: Active development
- `feature/*`: New features
- `release/*`: Pre-release
- `hotfix/*`: Urgent production fixes

---

## 📄 License

MIT

---

Feel free to fork, adapt, and grow this as part of your Swaraj journey 🚀
