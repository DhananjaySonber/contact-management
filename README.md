# Contact Management API

## Overview

This is a **Node.js** and **Express.js** backend for a Contact Management Application. It allows users to **create, read, update, and delete** contacts stored in **MongoDB**.

## Features

- **CRUD Operations**
  - Add new contacts
  - Fetch all contacts
  - Fetch a contact by ID
  - Update a contact by ID
  - Delete a contact by ID
- **Data Validation** using `express-validator`
- **Error Handling** with proper HTTP status codes
- **MongoDB Integration**

## Installation

### Prerequisites

- **Node.js** (>= 14.0.0)
- **MongoDB** installed and running locally or using MongoDB Atlas

### Steps to Install

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/contact-management-api.git
   ```
2. Navigate to the project directory:
   ```sh
   cd contact-management-api
   ```
3. Install dependencies:
   ```sh
   npm install
   ```
4. Start the server:
   ```sh
   npm start
   ```
   The server will run on `http://localhost:5000`

## API Endpoints

### 1. Get All Contacts

```http
GET /contacts
```

Response:

```json
[
  {
    "_id": "123",
    "name": "John Doe",
    "email": "john@example.com",
    "phone": "123-456-7890",
    "address": "123 Main St",
    "createdAt": "2024-01-01T00:00:00.000Z"
  }
]
```

### 2. Get Contact by ID

```http
GET /contacts/:id
```

### 3. Create a Contact

```http
POST /contacts
```

Request Body:

```json
{
  "name": "Jane Doe",
  "email": "jane@example.com",
  "phone": "987-654-3210",
  "address": "456 Another St"
}
```

### 4. Update a Contact

```http
PUT /contacts/:id
```

### 5. Delete a Contact

```http
DELETE /contacts/:id
```
