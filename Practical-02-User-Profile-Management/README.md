# Practical 02: User Profile Management System

## Problem Statement

Design and develop a User Profile Management System using React, Node.js, and MongoDB.

### Requirements

- User Registration
- User Login
- View Profile
- Edit Profile
- Change Password
- Input Validation
- Store and retrieve user data from MongoDB

## 1. Introduction

A User Profile Management System allows registered users to view and manage their personal information after logging in.

In this practical, we extend the User Authentication System developed in Practical 1. Users will be able to view their profile, update editable details, and change their password.

The application uses React for the frontend, Node.js and Express.js for backend APIs, and MongoDB for storing user information.

## 2. Technologies Used

| Technology | Purpose |
|---|---|
| React | Develop the user interface |
| Node.js | Run JavaScript on the server |
| Express.js | Create backend APIs |
| MongoDB | Store user information |
| Mongoose | Define schemas and interact with MongoDB |
| bcryptjs | Hash passwords and compare password hashes |

## 3. Working of the Application

### A. User Registration and Login

1. The user registers with the required details.
2. The backend validates the input and stores the user record in MongoDB.
3. The user logs in using their registered email and password.
4. The backend verifies the credentials and establishes an authenticated session or issues a token.

These features are carried forward from Practical 1.

### B. View Profile

1. The authenticated user opens the profile page.
2. The frontend requests the user's profile from the backend.
3. The backend identifies the authenticated user.
4. The user's permitted profile details are retrieved from MongoDB.
5. The frontend displays the details.

### C. Edit Profile

1. The user opens the edit profile form.
2. The existing profile information is displayed.
3. The user modifies the permitted fields.
4. The frontend and backend validate the submitted data.
5. The backend updates the user's record in MongoDB.
6. A success or error message is displayed.

### D. Change Password

1. The user enters the current password and the new password.
2. The backend verifies the current password.
3. The new password is validated.
4. The backend hashes the new password before updating MongoDB.
5. The user receives a confirmation message.

### E. Input Validation

The application must validate required fields, email format, and password requirements. The backend must repeat the necessary validation rather than relying only on React.

## 4. Understanding Frontend and Backend

**Frontend:** Displays the profile, edit profile form, password change form, and validation messages.

**Backend:** Provides APIs to retrieve and update profile information and change passwords.

**Database:** Stores user information in MongoDB and retrieves it when required.

**Authentication:** Ensures that users can access and modify only their own profile information.

## 5. Code Files to Study

### Frontend

- `client/src/components/Register.jsx` — user registration.
- `client/src/components/Login.jsx` — user login.
- `client/src/components/Dashboard.jsx` — profile display and navigation.
- Additional profile and password components created for this practical.

### Backend

- `server/models/User.js` — user schema.
- `server/routes/authRoutes.js` — registration and login APIs.
- `server/routes/profileRoutes.js` — profile-related APIs, if used.
- `server/middleware/authMiddleware.js` — authentication checks.
- `server/server.js` — Express configuration and database connection.

The exact filenames may vary according to the implementation.

## 6. Suggested API Operations

| Operation | Example endpoint | Purpose |
|---|---|---|
| Register | `POST /api/auth/register` | Create a user |
| Login | `POST /api/auth/login` | Authenticate a user |
| View profile | `GET /api/profile` | Retrieve the current user's profile |
| Edit profile | `PUT /api/profile` | Update permitted profile fields |
| Change password | `PUT /api/profile/change-password` | Change the authenticated user's password |

These are suggested endpoints; use the actual routes implemented in your application.

## 7. Testing

| Test case | Expected result |
|---|---|
| Log in with valid credentials | Login succeeds |
| View profile after login | Correct user details are displayed |
| Update profile with valid details | Profile is updated |
| Submit invalid profile details | Validation error is displayed |
| Change password with the correct current password | Password is updated |
| Change password with an incorrect current password | Password change is rejected |
| Access another user's profile | Access is denied |
| Submit an invalid new password | Validation error is displayed |

## 8. Learning Outcomes

After completing this practical, We can be able to:

- Build profile management components using React.
- Retrieve and update data through REST APIs.
- Use Express routes and Mongoose for database operations.
- Validate profile and password inputs.
- Implement authenticated, user-specific operations.
- Hash passwords securely before storing them in MongoDB.

## 9. Security Guidelines

- Never store plaintext passwords.
- Verify the authenticated user's identity on the backend.
- Allow users to modify only permitted profile fields.
- Verify the current password before changing it.
- Never expose password hashes or sensitive information in API responses.
- Keep database credentials and authentication secrets out of GitHub.

## 10. Expected Outcome

A working User Profile Management System integrated with the authentication features from Practical 1. Registered users should be able to log in, view and edit their own profiles, and securely change their passwords.
