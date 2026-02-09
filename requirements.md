# Backend Requirements Specifications for Airbnb Clone

## 1. User Authentication

**Description:**  
Enable users to securely register, log in, and manage their account.

**API Endpoints:**
- `POST /api/register` – Create a new user account.
- `POST /api/login` – Authenticate user and return a JWT token.
- `GET /api/profile` – Retrieve user profile (authenticated).
- `PUT /api/profile` – Update user profile (authenticated).

**Input/Output Specifications:**
- Registration Input:
  ```json
  {
    "username": "string",
    "email": "string",
    "password": "string"
  }

{
  "user_id": "integer",
  "username": "string",
  "email": "string",
  "message": "Account created successfully"
}

{
  "email": "string",
  "password": "string"
}

{
  "token": "JWT string",
  "user_id": "integer",
  "username": "string"
}

{
  "title": "string",
  "description": "string",
  "price": "decimal",
  "location": "string"
}

{
  "property_id": "integer",
  "title": "string",
  "description": "string",
  "price": "decimal",
  "location": "string",
  "owner_id": "integer",
  "created_at": "timestamp"
}

{
  "property_id": "integer",
  "check_in": "date",
  "check_out": "date",
  "guests": "integer"
}

{
  "booking_id": "integer",
  "property_id": "integer",
  "user_id": "integer",
  "check_in": "date",
  "check_out": "date",
  "guests": "integer",
  "status": "confirmed",
  "created_at": "timestamp"
}


