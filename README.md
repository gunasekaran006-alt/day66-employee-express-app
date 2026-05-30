# Employee Management API

A simple, lightweight RESTful API built with Node.js and Express.js to manage employee records. This project demonstrates backend development fundamentals, including custom environment setup, routing, controllers, MVC structure, and basic CRUD operations.

## ✨ Features

- **Get All Employees**: Retrieve a list of all employees in the database.
- **Add Employee**: Create a new employee profile with a unique ID.
- **Update Employee**: Modify details of an existing employee by their ID.
- **Delete Employee**: Remove an employee record from the system.

## 🚀 Tech Stack

- **Backend**: Node.js
- **Framework**: Express.js
- **Development Tool**: Nodemon
- **Database**: In-memory Array (Mock Data)

## 🛠️ Project Setup & Installation Steps

Follow these exact steps to set up and run the project locally:

### Step 1: Create a New Folder
Create a project folder on your system and navigate into it.

### Step 2: Initialize Node.js Application
Generate a default `package.json` file:
```bash
npm init -y
```

### Step 3: Configure Entry Point
Open `package.json` and rename the default `"main": "index.js"` into `"main": "main.js"`.

### Step 4: Create Main File
Create a new file named `main.js` in the root directory.

### Step 5: Dependency Installation
Install the Express framework:
```bash
npm i express
```

### Step 6: Git Configuration
Create a `.gitignore` file and add the `node_modules` folder name into it to prevent uploading unnecessary files to GitHub.

### Step 7: Create Express Server
Write the complete Express server setup in your `main.js` file.

### Step 8: Install Development Dependency
Install the `nodemon` library as a dev dependency to restart the server automatically on file changes:
```bash
npm i -D nodemon
```

### Step 9: Add Development Script
Add a `dev` script inside the `"scripts"` block of your `package.json` file:
```json
"scripts": {
  "dev": "nodemon main.js"
}
```

### Step 10: Start the Application
Run the project in development mode using the command below:
```bash
npm run dev
```
The server will start running on `http://localhost:8080`.

## 📁 Folder Structure

```text
day66-employee-express-app/
├── controllers/
│   └── employee.controller.js  # Contains the CRUD logic
├── models/
│   └── employee.model.js       # In-memory array data store
├── routes/
│   └── employee.routes.js      # Defines API endpoints mapping
├── .gitignore                  # Ignores node_modules
├── main.js                     # Main entry point of the application
├── package.json                # Project configuration and scripts
└── README.md                   # Project documentation
```

## 🛣️ API Endpoints

### 1. Get All Employees
* **URL:** `/employees`
* **Method:** `GET`
* **Success Response (200 OK):**
  ```json
  [
    {
      "id": "1717112345678",
      "name": "John Doe",
      "email": "john@example.com",
      "role": "Developer"
    }
  ]
  ```

### 2. Create Employee
* **URL:** `/employees`
* **Method:** `POST`
* **Request Body:**
  ```json
  {
    "name": "Alex Router",
    "email": "alex@example.com",
    "role": "Designer"
  }
  ```
* **Success Response (201 Created):**
  ```json
  {
    "message": "Employee data Added"
  }
  ```

### 3. Update Employee
* **URL:** `/employees/:id`
* **Method:** `PUT`
* **Request Body:**
  ```json
  {
    "role": "Senior Designer"
  }
  ```
* **Success Response (200 OK):**
  ```json
  {
    "message": "Employee data updated"
  }
  ```

### 4. Delete Employee
* **URL:** `/employees/:id`
* **Method:** `DELETE`
* **Success Response (200 OK):**
  ```json
  {
    "message": "Employee data removed"
  }
  ```

## 📝 License

This project is open-source and available under the MIT License.
