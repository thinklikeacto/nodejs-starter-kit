# nodejs-starter-kit

The `nodejs-starter-kit` is a generic, production-ready microservice boilerplate built using **NestJS with TypeScript**, designed for Swaraj’s microservices architecture. It follows a clean, modular structure aligned with the `user-auth-gateway` service and is suitable for creating backend services like `notification`, `process-engine`, or any other supporting microservice.

## 🚀 Features

- Scalable and modular NestJS architecture
- Follows a clean folder structure for easy code organization
- Pre-integrated environment configuration and logging
- Ready for Docker-based deployment
- Compatible with Kafka, PostgreSQL, Redis, MongoDB
- Easy to extend and plug into the Swaraj microservices ecosystem
- ✔️ Graceful shutdown setup-ready for clean service termination

## 📁 Folder Structure

```
nodejs-starter-kit/
├── src/
│   ├── main.ts                        # Entry point
│   ├── app.module.ts                 # Root module
│   ├── api/                          # API route controllers
│   │   └── v1/
│   │       └── core.controller.ts   # Example base controller
│   ├── models/                       # DTOs, interfaces, schemas
│   │   └── core.model.ts
│   ├── repositories/                # Database access layer
│   │   └── core.repository.ts
│   ├── services/                    # Business logic layer
│   │   └── core.service.ts
│   ├── middleware/                  # Custom guards, interceptors, middleware
│   │   └── logger.middleware.ts
│   ├── utils/                       # Utility functions and constants
│   │   ├── logger.ts
│   │   └── constants.ts
│   ├── config/                      # Config and env handling
│   │   ├── config.module.ts
│   │   ├── config.service.ts
│   │   └── env.validation.ts
│   └── shared/                      # Shared modules across services
│       └── health.module.ts
├── test/                            # Test cases and mocks
├── .env.example                     # Environment variable template
├── .gitignore
├── Dockerfile                       # Docker setup
├── docker-compose.yml              # Multi-container config (DBs, Redis, etc.)
├── package.json
├── tsconfig.json
├── README.md
```

> 🧩 Each folder can include multiple modules depending on the domain or feature.

## 🛠️ Tech Stack

- [NestJS](https://nestjs.com/) with TypeScript
- `class-validator` and `class-transformer` for DTO validation
- PostgreSQL / MongoDB / Redis (pluggable)
- Kafka integration ready (optional)
- Docker + Docker Compose support

## 🧪 Scripts

```bash
# Install dependencies
yarn install

# Run development server
yarn start:dev

# Run production build
yarn build && yarn start:prod

# Run tests
yarn test
```

## 📦 Environment Variables

Copy `.env.example` to `.env` and configure your values:

```bash
PORT=3000
NODE_ENV=development
DB_HOST=localhost
DB_PORT=5432
...
```

## 🎯 Philosophy

This kit is optimized for fast development, MVPs, and structured microservice design. While production-ready in structure, some performance, observability, and scaling configurations can be layered in based on project needs.

The goal of this starter kit is clarity, structure, and fast onboarding—not minimalism or zero-dependency footprint. It's ideal for bootstrapping new backend services and growing them iteratively as needs evolve.

## 🧩 When to Use
Use this starter kit whenever you want to:
- Build a new backend microservice within Swaraj
- Create a standalone NestJS service with clean structure
- Quickly bootstrap MVPs for backend components

## 📄 License
MIT

---

Feel free to fork, contribute, and adapt this kit as part of your microservices journey in Swaraj.
