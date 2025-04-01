# IntelliSQR Backend

A TypeScript-based authentication backend built with Express.js and Prisma ORM.

## Features

- User authentication (login/signup)
- JWT-based authentication
- Password hashing with bcrypt
- RESTful API endpoints
- TypeScript type safety
- Prisma ORM for database operations

## Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- PostgreSQL database
- TypeScript

## Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
PORT=3000
DATABASE_URL="postgresql://user:password@localhost:5432/intellisqr"
JWT_SECRET=your-secret-key-here
```

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up the database:
   ```bash
   npx prisma generate
   npx prisma migrate dev
   ```
4. Create a `.env` file with the required environment variables

## Running the Application

### Development Mode

```bash
npm run dev
```

### Production Mode

```bash
npm run build
npm start
```

## Project Structure

```
backend/
├── src/              # Source code
│   ├── server.ts     # Main server file
│   └── ...           # Other source files
├── prisma/           # Prisma configuration
│   └── schema.prisma # Database schema
├── package.json      # Project dependencies
├── tsconfig.json     # TypeScript configuration
└── .env              # Environment variables
```

## API Endpoints

- POST `/api/auth/signup` - Register a new user
- POST `/api/auth/login` - Authenticate user
- GET `/api/auth/me` - Get current user information

## Technologies Used

- Express.js
- TypeScript
- Prisma ORM
- PostgreSQL
- bcryptjs
- jsonwebtoken
- cors

## License

ISC License