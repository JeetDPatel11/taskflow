# TaskFlow – Team Task Management System

A full stack task management application where users create projects, assign tasks to team members and track progress through different stages.

## Overview
TaskFlow helps teams organize their work. Admins create projects and assign tasks, and members update the status of their tasks. A dashboard gives a quick summary of the work in each stage.

## Tech Stack
- **Frontend:** React.js, HTML5, CSS3
- **Backend:** Node.js, Express.js, REST APIs
- **Database:** MySQL
- **Authentication:** JWT (JSON Web Tokens), bcrypt password hashing
- **Tools:** Git, GitHub, Postman, VS Code

## Features
- User registration and login with JWT authentication
- Role-based access control (Admin / Member)
- Create and manage projects
- Create, assign and update tasks
- Task status tracking: To-Do, In-Progress, Done
- Dashboard showing task counts by status
- Search and filter tasks by status, project and assignee
- Responsive user interface

## User Roles
- **Admin:** create projects, create and assign tasks, view all tasks
- **Member:** view assigned tasks and update their status

## Database Design
The app uses a normalized MySQL schema with three main tables:

| Table | Columns |
|-------|---------|
| users | id, name, email, password_hash, role, created_at |
| projects | id, name, description, created_by, created_at |
| tasks | id, project_id, title, description, status, assigned_to, due_date, created_at |

Relationships:
- One user can create many projects
- One project has many tasks
- One task is assigned to one user

## API Endpoints (Planned)
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/auth/register | Register a new user |
| POST | /api/auth/login | Login and receive a JWT |
| GET | /api/projects | List projects |
| POST | /api/projects | Create a project (admin) |
| GET | /api/tasks | List tasks (search and filters) |
| POST | /api/tasks | Create and assign a task (admin) |
| PUT | /api/tasks/:id | Update a task or its status |
| DELETE | /api/tasks/:id | Delete a task (admin) |
| GET | /api/dashboard | Task counts by status |

## Application Flow
1. A user registers or logs in and receives a JWT.
2. The admin creates a project and adds tasks.
3. Tasks are assigned to team members.
4. Members move tasks from To-Do to In-Progress to Done.
5. The dashboard shows overall progress.

## Future Enhancements
- Task comments
- Due-date reminders
- Drag-and-drop task board
- Email notifications

## Author
Jeet Patel – [GitHub](https://github.com/JeetDPatel11)
