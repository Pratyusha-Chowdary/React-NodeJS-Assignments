# Practical 01: User Authentication System

## Problem Statement

Develop a User Authentication System using React, Node.js, and MongoDB.

### Requirements

- Create a user registration form.
- Implement user login functionality.
- Validate email and password fields.
- Store user details in MongoDB.
- Implement logout functionality.

## 1. Introduction

Authentication is the process of verifying the identity of a user. For example, when we log in to an application using an email address and password, the application checks whether the credentials are valid.

In this practical, we develop a user authentication system using the MERN stack.

## 2. Technologies Used

| Technology | Purpose |
|---|---|
| React | Develop the user interface |
| Node.js | Run JavaScript on the server |
| Express.js | Create backend APIs |
| MongoDB | Store user information |
| Mongoose | Define the user schema and interact with MongoDB |

## 3. Working of the Application

### A. Registration

1. The user enters their name, email address, and password.
2. React validates the input fields.
3. The frontend sends the details to the backend API.
4. Express validates the request and checks whether the email is already registered.
5. The password is hashed securely.
6. The user details are stored in MongoDB.
7. The backend returns a success or error response.

### B. Login

1. The user enters their email address and password.
2. React sends the credentials to the backend.
3. The backend finds the user by email.
4. The entered password is compared with the stored password hash.
5. If the credentials are valid, the backend establishes an authenticated session or issues a token.
6. The application allows the authenticated user to access protected functionality.

### C. Logout

1. The user clicks the Logout option.
2. The application ends the authenticated session or clears the appropriate authentication state.
3. The user is redirected to the login page.

## 4. Understanding Frontend and Backend

**Frontend:** Contains the registration form, login form, validation messages, and user interface.

**Backend:** Receives requests, validates data, verifies credentials, and communicates with MongoDB.

**Database:** Stores registered user information. Passwords must be stored as hashes, never as plaintext.

## 5. Code Files to Study

### Frontend

- `client/src/components/Register.jsx` — registration form and submission.
- `client/src/components/Login.jsx` — login form and submission.
- `client/src/components/Dashboard.jsx` — authenticated user interface.
- `client/src/components/Logout.jsx` — logout functionality.

### Backend

- `server/routes/authRoutes.js` — registration and login APIs.
- `server/models/User.js` — user schema and password handling.
- `server/server.js` — Express server and database configuration.
- `server/middleware/authMiddleware.js` — authentication middleware, if used.

Open these files in the repository to study the implementation.

## 6. Testing

| Test case | Expected result |
|---|---|
| Register with valid details | User registration succeeds |
| Register with an existing email | Duplicate registration is rejected |
| Enter an invalid email | Validation error is displayed |
| Log in with correct credentials | Login succeeds |
| Log in with an incorrect password | Login is rejected |
| Submit empty fields | Validation error is displayed |
| Log out | Authenticated state is cleared |

## 7. Learning Outcome

After completing this practical, We will understand React forms, API communication, Express routes, MongoDB integration, password hashing, authentication, validation, and logout functionality.

## 8. Security Guidelines

- Never store plaintext passwords.
- Never upload `.env` files or credentials to GitHub.
- Validate inputs on both frontend and backend.
- Protect authenticated routes on the server.
- Do not return sensitive information in API responses.
