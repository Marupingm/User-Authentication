# User Authentication System

A secure user authentication system built with Node.js, Express, MongoDB, and JWT.

## Features

- User registration with password hashing
- User login with JWT authentication
- Protected user profile route
- Email validation
- Password encryption using bcrypt
- MongoDB integration with Mongoose
- Error handling and validation
- CORS enabled

## Prerequisites

- Node.js (v12 or higher)
- MongoDB
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd user-authentication
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory and add your configuration:
```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/user-auth
JWT_SECRET=your-super-secret-jwt-key
JWT_EXPIRE=24h
```

## Usage

### Development
```bash
npm run dev
```

### Production
```bash
npm start
```

## API Endpoints

### Register User
- **POST** `/api/auth/register`
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "123456"
}
```

### Login User
- **POST** `/api/auth/login`
```json
{
  "email": "john@example.com",
  "password": "123456"
}
```

### Get User Profile
- **GET** `/api/auth/profile`
- Requires Authorization header: `Bearer <token>`

## Security Features

- Password hashing using bcrypt
- JWT for secure authentication
- Protected routes using middleware
- Input validation and sanitization
- Email format validation
- Secure password requirements

## Project Structure

```
user-authentication/
├── controllers/
│   └── authController.js
├── middleware/
│   └── auth.js
├── models/
│   └── User.js
├── routes/
│   └── auth.js
├── .env
├── .gitignore
├── package.json
├── README.md
└── server.js
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License. 