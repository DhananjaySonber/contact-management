# Contact Management API

![Node.js](https://img.shields.io/badge/Node.js-18.x-green)
![Express.js](https://img.shields.io/badge/Express.js-4.x-lightgrey)
![MongoDB](https://img.shields.io/badge/MongoDB-7.x-blue)

A RESTful API backend for managing contacts, built with Node.js, Express.js, and MongoDB.

## Features

- CRUD operations for contacts
- MongoDB database integration
- Input validation
- Error handling with proper HTTP status codes
- RESTful API design
- CORS support
- Environment configuration

## Technologies Used

- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **Dotenv** - Environment variables management
- **CORS** - Cross-Origin Resource Sharing

## Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/contact-manager-backend.git
cd contact-manager-backend

2. Install dependencies
npm install

3. Set up environment variables
Create a .env file in the root directory:

MONGODB_URI=mongodb://localhost:27017/contactsdb
PORT=3000

4. Start the server
node app.js

The API will be available at http://localhost:3000

API Endpoints
Method	Endpoint	Description
GET	/contacts	Get all contacts
POST	/contacts	Create new contact
GET	/contacts/:id	Get single contact
PUT	/contacts/:id	Update contact
DELETE	/contacts/:id	Delete contact
Request/Response Examples
Create Contact (POST /contacts)

// Request
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "1234567890",
  "address": "123 Main St"
}

// Response (201 Created)
{
  "contactId": "65a1b4e8c8b9f12e3f8d7c5a",
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "1234567890",
  "address": "123 Main St",
  "createdAt": "2024-01-12T10:30:00.000Z"
}

Get All Contacts (GET /contacts)

json
Copy
// Response (200 OK)
[
  {
    "contactId": "65a1b4e8c8b9f12e3f8d7c5a",
    "name": "John Doe",
    "email": "john@example.com",
    "phone": "1234567890",
    "address": "123 Main St",
    "createdAt": "2024-01-12T10:30:00.000Z"
  }
]
Error Handling
Sample error responses:

400 Bad Request

json
Copy
{
  "errors": ["Name is required", "Email is required"]
}
404 Not Found

json
Copy
{
  "error": "Contact not found"
}
500 Internal Server Error

json
Copy
{
  "error": "Server error"
}
Testing the API
You can test the API using:

Postman

curl

Thunder Client (VS Code extension)

Example curl command:

bash
Copy
curl -X POST -H "Content-Type: application/json" -d '{
  "name": "Jane Smith",
  "email": "jane@example.com",
  "phone": "0987654321"
}' http://localhost:3000/contacts
Contributing
Fork the project

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request
