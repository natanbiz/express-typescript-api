# Express TypeScript API Starter

A modern, production-ready REST API built with Express, TypeScript, and Prisma ORM. This template provides a solid foundation for building secure and scalable web applications with comprehensive authentication, data validation, and documentation.

<div align="center">

![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-3982CE?style=for-the-badge&logo=Prisma&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)
![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)
![Logtail](https://img.shields.io/badge/Logtail-00A36C?style=for-the-badge&logo=better-stack&logoColor=white)

</div>

## ✨ Key Features

- **Authentication** - Secure user registration and login with JWT
- **Database Integration** - PostgreSQL with Prisma ORM for type-safe queries
- **Error Handling** - Comprehensive error management system
- **API Documentation** - Interactive Swagger documentation
- **TypeScript** - Full type safety throughout the application
- **CORS Support** - Configured for cross-origin requests
- **Request Validation** - Ensures data integrity
- **Cloud Logging** - Structured logging with Logtail

## 📋 Requirements

- Node.js 14+
- PostgreSQL database
- npm or yarn package manager
- Logtail account for logging

## 🚀 Quick Start

### Clone and Install

```bash
git clone https://github.com/natanbiz/express-typescript-api.git
cd express-typescript-api
npm install
```

### Configure Environment

Create a `.env` file in the root directory:

```
DATABASE_URL="postgresql://username:password@localhost:5432/dbname"
JWT_SECRET="your-secure-secret-key"
PORT=3000
LOGTAIL_ENDPOINT="https://your-logtail.betterstackdata.com"
LOGTAIL_TOKEN="your-logtail-source-token"
```

### Database Setup

```bash
npx prisma migrate dev --name init
```

### Start Development Server

```bash
npm run dev
```

Your API will be available at `http://localhost:3000`

## 📚 API Reference

### Authentication

| Method | Endpoint        | Description      | Auth Required |
|--------|-----------------|------------------|--------------|
| POST   | /auth/register  | Create new user  | No           |
| POST   | /auth/login     | Authenticate user| No           |

### Posts

| Method | Endpoint        | Description      | Auth Required |
|--------|-----------------|------------------|--------------|
| GET    | /posts          | Get all posts    | No           |
| GET    | /posts/:id      | Get post by ID   | No           |
| POST   | /posts          | Create new post  | Yes          |
| PUT    | /posts/:id      | Update post      | Yes          |
| DELETE | /posts/:id      | Delete post      | Yes          |

## 🧪 Testing

The API can be tested using the provided Postman collection. After importing the collection:

1. Execute the login request to get a JWT token
2. The collection will automatically store the token for authenticated requests

## 📊 Logging

The application uses Logtail for cloud-based structured logging:

- **Real-time log streaming** - View logs as they happen
- **Structured logging** - JSON-based logging for better analysis
- **Search and filters** - Easily find specific log events
- **Alerts and notifications** - Get notified of critical issues
- **Dashboard visualization** - Monitor application health

Configure your Logtail token in the `.env` file to enable logging to your Logtail account.

## 🔧 Project Structure

```
├── src/
│   ├── controllers/    # Request handlers
│   ├── middleware/     # Express middleware
│   ├── routes/         # API routes
│   ├── services/       # Business logic
│   ├── utils/          # Helper functions
│   ├── logger/         # Logtail configuration
│   ├── app.ts          # Express application
│   └── server.ts       # Server entry point
├── prisma/
│   └── schema.prisma   # Database schema
└── swagger/            # API documentation
```

## 🔒 Security Features

- Password hashing with bcrypt
- JWT token-based authentication
- Request validation
- CORS protection
- Rate limiting

## 📝 License

[MIT](LICENSE)
