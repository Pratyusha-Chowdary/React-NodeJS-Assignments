# React-NodeJS-Assignments



# Assignment 1 – User Authentication System

## React and Node JS Lab

### Objective

Develop a User Authentication System using React.js, Node.js, Express.js and MongoDB.

The application should allow users to register, login and logout securely.

---

## Technologies to Use

- React.js
- Node.js
- Express.js
- MongoDB
- Mongoose
- HTML
- CSS
- JavaScript

---

## Requirements

### 1. User Registration

Create a registration page containing:

- Full Name
- Email
- Password
- Register button

The application should:

- Accept user details through a React form.
- Validate the input.
- Validate the email format.
- Validate the password.
- Check whether the email is already registered.
- Store the user details in MongoDB.
- Display an appropriate success or error message.

---

### 2. User Login

Create a login page containing:

- Email
- Password
- Login button

The application should:

- Accept email and password.
- Validate the entered details.
- Check the credentials against the database.
- Display an appropriate error message for invalid credentials.
- Allow the user to access the dashboard after successful login.

---

### 3. Dashboard

After successful login, display a dashboard containing:

- Welcome message
- User name
- User email
- Logout button

Example:

Welcome, Rahul!

Email: rahul@example.com

[Logout]

---

### 4. Logout

Implement logout functionality.

When the user clicks Logout:

- Remove the user's login information.
- Redirect/display the login page.
- The user should no longer be treated as logged in.

---

## Backend Requirements

Create appropriate REST API endpoints.

Example:

POST /api/auth/register

POST /api/auth/login

Use Express.js to handle the API requests.

---

## Database Requirements

Use MongoDB to store registered user information.

Example fields:

- name
- email
- password

Passwords must NOT be stored as plain text.

Use password hashing such as bcrypt.

---

## Validation

The application should handle:

- Empty fields
- Invalid email
- Short/invalid password
- Already registered email
- Invalid login credentials

Display appropriate messages to the user.

---

# GitHub Requirements

Each student must maintain the project in their own GitHub repository.

## Repository Naming Format

Use:

USN-StudentMart

Example:

1AT23CS001-StudentMart

---

## Faculty Access

Add the faculty GitHub account as a collaborator.

Faculty GitHub Username:

Pratyusha-Chowdary

---

## Git Commits

Students must commit and push their work regularly.

Example:

git add .

git commit -m "Implemented user registration"

git push

Use meaningful commit messages.

Examples:

- Initial project setup
- Created registration form
- Implemented registration API
- Connected MongoDB
- Implemented login
- Implemented logout
- Completed Assignment 1

---

## Important

DO NOT upload the following to GitHub:

- node_modules
- .env
- Passwords
- Database credentials
- Secret keys

Your .gitignore file should contain:

node_modules/
.env
dist/

---

# Submission

Submit the following details:

Name:

USN:

GitHub Username:

GitHub Repository Link:

---

# Evaluation

The assignment will be evaluated based on:

1. Registration functionality
2. Login functionality
3. MongoDB integration
4. Validation
5. Logout functionality
6. React UI
7. API implementation
8. GitHub repository and commits
9. README documentation
10. Overall functionality

---

# Viva

Students should be prepared to answer questions about:

- React
- Components
- State
- Forms
- API
- HTTP methods
- Node.js
- Express.js
- MongoDB
- Mongoose
- bcrypt
- Git
- GitHub
