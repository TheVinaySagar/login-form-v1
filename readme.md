# User Authentication System

A secure user authentication system built with Node.js, Express, and MongoDB. The system provides user registration and login functionality with JWT (JSON Web Token) authentication.

https://github.com/user-attachments/assets/e3f7b167-f1fd-4090-88f8-bc4a3a90d8f0


## Features

- 🔐 User registration with password hashing
- 🔑 Secure login system
- 🎫 JWT-based authentication
- 📧 Email uniqueness validation
- 🔒 Password encryption using bcrypt
- 🚀 RESTful API endpoints
- 📱 Responsive web interface

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (jsonwebtoken)
- **Password Hashing**: bcryptjs
- **API Testing**: Postman (recommended)

## Prerequisites

Before running this project, make sure you have:
- Node.js (v12 or higher)
- MongoDB installed and running
- npm (Node Package Manager)

## Installation

1. Clone the repository:
```bash
git clone [your-repository-url]
cd [repository-name]
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/loginApp
JWT_SECRET=your_jwt_secret
```

## Project Structure

```
├── config/
│   └── db.js           # Database configuration
├── models/
│   └── User.js         # User model schema
├── routes/
│   └── auth.js         # Authentication routes
├── public/
│   ├── index.html      # Login page
│   └── register.html   # Registration page
└── server.js           # Express server setup
```

## API Endpoints

### Authentication Routes

#### Register User
- **POST** `/register`
- **Body**: 
  ```json
  {
    "email": "user@example.com",
    "password": "yourpassword"
  }
  ```
- **Response**: Success message or error details

#### Login User
- **POST** `/`
- **Body**: 
  ```json
  {
    "email": "user@example.com",
    "password": "yourpassword"
  }
  ```
- **Response**: JWT token or error details

## Running the Application

1. Start MongoDB:
```bash
mongod
```

2. Run the server:
```bash
node server.js
```

3. Access the application:
- Open `http://localhost:5000` for the login page
- Navigate to `http://localhost:5000/register` for registration

## Security Features

- Password hashing using bcrypt
- JWT for secure authentication
- Email uniqueness validation
- Password strength validation
- Protected routes using JWT middleware

## Dependencies

```json
{
  "express": "^4.17.1",
  "mongoose": "^6.0.0",
  "bcryptjs": "^2.4.3",
  "jsonwebtoken": "^8.5.1",
  "body-parser": "^1.19.0"
}
```

## Development

To modify the system:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Create a Pull Request

## Error Handling

The system includes comprehensive error handling for:
- Invalid credentials
- Duplicate email addresses
- Server errors
- Database connection issues
- Invalid JWT tokens

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the GitHub repository or contact the maintainers.

## Acknowledgments

- Built with [Express.js](https://expressjs.com/)
- Database by [MongoDB](https://www.mongodb.com/)
- Authentication using [JWT](https://jwt.io/)

