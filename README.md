
# **Task Management API** 🚀  

A simple Task Management API built with **Node.js, Express, and MongoDB** that supports **User Authentication (JWT), Task Management, and Category Filtering**.

## **Features**
✅ User Authentication (Login, Register) using JWT  
✅ Task Management (Add, Edit, Delete, View)  
✅ Categories for tasks (Work, Personal, etc.)  
✅ Filter tasks by category  

---

## **Tech Stack**  
- **Backend**: Node.js, Express.js  
- **Database**: MongoDB  
- **Authentication**: JWT  

---

## **Getting Started**  

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/rishika09090/upgradex_assignment.git
cd task-management-api
```

### **2️⃣ Install Dependencies**
```bash
npm install
```

### **3️⃣ Set Up Environment Variables**
Create a **.env** file in the root directory and add the following variables:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

### **4️⃣ Start the Server**
```bash
npm start
```
The server will run on **http://localhost:5000**

---

## **API Endpoints**  

### **🟢 User Authentication**  
**Register User**  
- **POST** `/api/auth/register`  
- **Body:**
  ```json
  {
    "name": "John Doe",
    "email": "johndoe@example.com",
    "password": "password123"
  }
  ```

**Login User**  
- **POST** `/api/auth/login`  
- **Body:**
  ```json
  {
    "email": "johndoe@example.com",
    "password": "password123"
  }
  ```

---

### **🟡 Categories**  
**Create a Category**  
- **POST** `/api/categories`  
- **Body:**
  ```json
  {
    "name": "Work"
  }
  ```

---

### **🔵 Task Management**  
**Create a Task**  
- **POST** `/api/tasks`  
- **Headers:** `{ "Authorization": "Bearer <your_jwt_token>" }`  
- **Body:**
  ```json
  {
    "title": "Complete the project",
    "description": "Finish backend API",
    "category": "category_id"
  }
  ```

**Get All Tasks (Filter by Category)**  
- **GET** `/api/tasks?category=category_id`  
- **Headers:** `{ "Authorization": "Bearer <your_jwt_token>" }`  

**Update a Task**  
- **PUT** `/api/tasks/:id`  
- **Headers:** `{ "Authorization": "Bearer <your_jwt_token>" }`  
- **Body:**
  ```json
  {
    "title": "Updated Task",
    "completed": true
  }
  ```

**Delete a Task**  
- **DELETE** `/api/tasks/:id`  
- **Headers:** `{ "Authorization": "Bearer <your_jwt_token>" }`  

---

## **🔍 Testing the API**  
You can use **Postman** or **Thunder Client** to test the API endpoints.

---

## **📜 License**  
This project is licensed under the **MIT License**.

---

