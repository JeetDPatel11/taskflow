# TaskFlow – Team Task Management System

A full stack task management application where users create projects, assign tasks, and track progress.

## Tech Stack
- **Frontend:** React.js, HTML5, CSS3
- **Backend:** Node.js, Express.js, REST APIs
- **Database:** MySQL
- **Authentication:** JWT (JSON Web Tokens), role-based access (Admin / Member)

## Features (Roadmap)
-  User registration and login with JWT authentication
-  Role-based access control (Admin / Member)
-  Create and manage projects
-  Create, assign and update tasks (To-Do, In-Progress, Done)
-  Dashboard showing task counts by status
-  Search and filter tasks

## Database Design
The app uses a normalized MySQL schema with three main tables:
- **users** – id, name, email, password hash, role
- **projects** – id, name, description, created by
- **tasks** – id, project, title, description, status, assigned to, due date

## Project Structure
```
taskflow/
├── backend/    # Express server, routes, controllers, MySQL queries
└── frontend/   # React app
```

## Author
Jeet Patel – [GitHub](https://github.com/JeetDPatel11)
