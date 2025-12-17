
# Node.js Jobs API – Production-Ready Backend (JWT + Swagger + MongoDB)

  

Fully functional, secure REST API built with Node.js, Express, and MongoDB.

Deployed and ready to test right now!

  

### Live Demo

**Swagger UI** → https://jobs-api-nodejs-8szj.onrender.com/api-docs/

  

Try the endpoints yourself — no setup needed!

  

### Features

- User authentication (register + login)

- JWT + protected routes

- Full CRUD for jobs (create, read, update, delete)

- Pagination, sorting, filtering, search

- Input validation (Mongoose + custom errors)

- Password hashing with bcryptjs

- Rate limiting, Helmet, CORS, XSS protection

- Interactive Swagger/OpenAPI documentation

  

## Models

  

### User

- name (String, required)

- email (String, required, unique)

- password (String, required)

  


### Job

- company (String, required, maxlength 50)

- position (String, required, maxlength 100)

- status (String, enum: ['interview', 'declined', 'pending'], default 'pending')

- createdBy (ObjectId, ref 'User', required)

  

## User Roles & Permissions

  

### Regular User

**Can do:**

- Register / Login

- Create/read/update/delete own jobs

- Access all own data

  

**Cannot do:**

- View other users' jobs

  

**Note:** No separate admin role – all authenticated users manage their own jobs.

  

### Tech Stack

- Node.js / Express

- MongoDB + Mongoose

- JWT authentication

- bcryptjs

- express-rate-limit, helmet, cors, xss-clean

- Swagger UI

  

### Quick Start (Local)

  
1. Basic Setup 	
```bash

git  clone  https://github.com/sadmanrashik1/Jobs-Api_Nodejs.git

cd  Jobs-Api_Nodejs

npm  install
```
2. Create .env file
```bash
MONGO_URL=

JWT_SECRET=

JWT_LIFETIME=

```
