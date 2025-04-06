# 🛡️ User API with NestJS

This is a simple user management API built with **NestJS**, focused on security best practices and data validation. It provides user registration, login, and authentication via JWT, and uses **Prisma ORM** to interact with the database.

---

## 🚀 Technologies Used

- **[NestJS](https://nestjs.com/)** – A modern Node.js framework
- **[Prisma ORM](https://www.prisma.io/)** – ORM for relational databases
- **[bcrypt](https://github.com/kelektiv/node.bcrypt.js)** – Password encryption
- **[JWT](https://jwt.io/)** – Authentication with JSON Web Tokens
- **[class-validator](https://github.com/typestack/class-validator)** – Data validation
- **[class-transformer](https://github.com/typestack/class-transformer)** – DTO data transformation

---

## 📦 Features

- ✅ User registration with validation  
- ✅ User login with JWT authentication  
- ✅ Password encryption using **bcrypt**  
- ✅ Validation and transformation with **Pipes**, `class-validator`, and `class-transformer`  
- ✅ Integration with **Prisma** for database persistence  
- ✅ JWT-protected routes  

---

### Install dependencies

```bash
npm install
```

---

### Set up environment variables

Create a .env file in the root of the project with the following content:

DATABASE_URL="postgresql://user:password@host:port/database"
SECRET_KEY="your_secret_key"


---

### Generate Prisma client

```bash
npx prisma generate
```

---

### Run database migrations

```bash
npx prisma migrate dev --name init
```

---

### Start the project

```bash
npm run start:dev
```

---

## 📡 API Endpoints

### **POST** `/users`
Create a new user.  
**Body:**
```json
{
  "email": "user@example.com",
  "password": "123456"
}
```

---

### **GET** `/users`
Returns all users.

🔒 Requires JWT authentication 

---

### **GET** `/users/:id`
Returns a specific user by ID.

---

### **PATCH** `/users/:id`
Updates a user by ID.

**Body:**
```json
{
  "email": "newemail@example.com"
}
```

---

### **DELETE** `/users/:id`
Deletes a user by ID.
