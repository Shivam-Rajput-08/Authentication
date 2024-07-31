# Authentication API with Node.js and JWT

## Overview

Blue-Infinity-Tech @ Authentication-Test-Task
This project is a basic authentication API built with Node.js using the MVC pattern. It includes functionality for user registration, login, and logout, with password hashing and JWT (JSON Web Tokens) for secure authentication.

## Prerequisites

Before setting up the project, ensure you have the following installed:

- [Node.js]
- [MongoDB]

## Setup and Installation

Follow these steps to set up and run the project locally:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Shivam-Rajput-08/Authentication.git
   cd Authentication
   ```

2. **Install Dependencies:**

   Install the required Node.js packages by running:

   ```bash
    npm install
   ```

3. **Create Environment Variables:**

   Create a .env file in the root of the project and add the following environment variables:

   PORT=3000
   MONGO_URI=mongodb://127.0.0.1:27017/authdb
   JWT_SECRET=your_jwt_secret_key
   JWT_EXPIRES_IN=1h

   Note: Replace your_jwt_secret_key with a strong secret key for JWT signing.

4. **Start MongoDB:**

   Ensure MongoDB is running. If you are using a local MongoDB server, start it with:
   mongod or mongosh

5. **Run the Project:**

   Start the Node.js server with:

   npm start

The server will start and listen on the port specified in .env (default is 3000).

## Using the API with Postman

You can use Postman to test the API endpoints. Below is the Postman data to interact with the API. For each request, make sure to replace placeholders like `<JWT Token>, email and password` with actual values obtained during API interactions.

### 1. **Register a New User**

- **Method:** POST
- **Endpoint:** `/api/auth/register`
- **Request Body:**

  ```json
  {
    "username": "exampleUser",
    "email": "user@example.com",
    "password": "examplePassword"
  }
  ```

### 2. **Login a User**

- **Method:** POST
- **Endpoint:** `/api/auth/login`
- **Request Body:**

  ```json
  {
    "email": "user@example.com",
    "password": "examplePassword"
  }
  ```

### 3. **Logout a User**

- **Method:** POST
- **Endpoint:** `/api/auth/logout`
- **Headers:**
  - **Authorization:** `Bearer <JWT Token>`
