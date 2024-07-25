# MERN Registration API

## Description

This MERN stack application allows users to register with their personal information and profile picture. It provides APIs for user registration, viewing user data, updating user data, and deleting users. The application includes a React.js frontend to interact with these APIs.

## Requirements

### 1. Registration API

- **Endpoint**: `/user/register`
- **Method**: POST
- **Request Body**:
  - `name` (string) - Person's full name
  - `email` (string) - User's email address
  - `username` (string) - User's chosen username
  - `contact` (number) - Contact information
  - `profilePhoto` (file) - Profile picture (handled with Multer or similar library)
- **Functionality**: Validates input data and stores user information, including the profile picture, in a MongoDB database.

### 2. View Registration Data API

- **Endpoint**: `/user`
- **Method**: GET
- **Functionality**: Retrieves and returns a list of registered users from the MongoDB database. Sensitive information such as passwords is excluded from the response.

### 3. Update Registration User Data API

- **Endpoint**: `/user/edit/:userId`
- **Method**: PUT
- **Request Body**:
  - `fieldsToUpdate` (object) - Fields and their updated values
- **Functionality**: Accepts a user's unique identifier (e.g., user ID) and the fields to update, validates the data, and updates the user’s information in the MongoDB database.

### 4. Delete User API

- **Endpoint**: `/user/delete/:userId`
- **Method**: DELETE
- **Functionality**: Accepts a user’s unique identifier (e.g., user ID) and removes the corresponding user from the MongoDB database.

### 5. User Interface

- **Technologies**: React.js
- **Functionality**:
  - Registration: Form to register a new user with validation.
  - View Users: Display the list of registered users and provide options to view individual user details.
  - Update User: Form to update user data with validation.
  - Delete User: Option to delete a user from the list.

## Setup and Installation

### Prerequisites

- Node.js
- MongoDB

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/VrushabhVeer/MERN-Practical-Task.git

### For Backend
   
1. Navigate to the Backend directory:
   ```bash
   cd backend
   
2. Install backend dependencies:
   ```bash
   npm install
   
3. Run the server:
   ```bash
   npm start

4. Environmental Variables:
   ```bash
   MONGOURL = "mongodb+srv://vrushabhveer:vrushabhveer@cluster0.8mbinij.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0"
   PORT = 8000

### For Frontend
   
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   
2. Install backend dependencies:
   ```bash
   npm install
   
3. Run the server:
   ```bash
   npm start

### Testing
Test the APIs using Postman or any other API testing tool by sending requests to the endpoints specified above.

## Preview

| Registration Page      | Users Page             |
| ---------------------- | ---------------------- |
| ![Screenshot_1](https://github.com/user-attachments/assets/22c1be1e-b991-4e35-a436-2b788d25d8c4) | ![Screenshot_2](https://github.com/user-attachments/assets/4efeb9f7-c76b-4436-95ef-43a893d510fb) |
