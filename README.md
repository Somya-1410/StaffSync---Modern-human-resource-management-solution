# StaffSync

### Modern people operations for growing teams

StaffSync is a modern, role-aware human resource management solution built to bring everyday people operations into one clear workspace. HR teams can manage employee information, review leave requests, monitor attendance, and share company updates. Managers can support their teams, while employees get a simple way to stay informed and manage their work-life essentials.

The project is designed as a clean MERN-stack foundation with a polished React dashboard and an Express API that can be connected to MongoDB as the product grows.

![StaffSync dashboard](https://placehold.co/1200x650/f4f1ff/6246d9?text=StaffSync+HR+Dashboard)

---

## Why StaffSync?

People operations should feel organized, not overwhelming. StaffSync gives teams:

- **One source of truth** for employee and team information
- **Clear role-based workflows** for HR managers, managers, and employees
- **Fast leave management** with approve and decline actions
- **Attendance visibility** through simple, readable dashboards
- **Better communication** through company announcements
- **A foundation for automation** as the system connects to MongoDB and production services

## Features

### HR and workspace management

- Dashboard with employee, attendance, leave, and hiring metrics
- Employee onboarding modal
- Team directory preview
- Responsive sidebar navigation
- Workspace profile menu with logout

### Leave and attendance

- Leave request list with employee details and dates
- Approve or decline leave requests
- Attendance overview chart
- Team availability indicators
- CSV attendance report export

### Communication

- Announcement composer modal
- Notification feedback for common actions
- Help center and settings entry points

### Authentication

- Login screen with role selection
- JWT-based login API
- Persistent browser session using `localStorage`
- Logout flow that clears the active session
- API error and loading states

## Tech stack

| Layer | Technology |
| --- | --- |
| Frontend | React 18, JavaScript, CSS |
| Build tool | Vite |
| Backend | Node.js, Express.js |
| Authentication | JSON Web Token (JWT) |
| Database-ready | MongoDB / Mongoose |
| API format | JSON |
| Styling | Custom responsive CSS |

## Demo users

Use any of the following example accounts on the local login screen:

| Name | Email | Password | Role |
| --- | --- | --- | --- |
| Olivia Rhye | `olivia@staffsync.demo` | `StaffSync@123` | HR manager |
| Phoenix Baker | `phoenix@staffsync.demo` | `StaffSync@123` | Manager |
| Lana Steiner | `lana@staffsync.demo` | `StaffSync@123` | Employee |

> **Demo authentication note:** The current development API accepts any valid email and non-empty password. These credentials are provided as easy-to-remember examples for demonstrations. They are not production accounts.

## Run locally

### Requirements

- Node.js 18 or newer
- npm 9 or newer

### Installation

```bash
npm install
npm run dev
```

The application will be available at:

- Frontend: [http://localhost:5173](http://localhost:5173)
- API health check: [http://localhost:5000/api/health](http://localhost:5000/api/health)

### Environment variables

Copy the example environment file before connecting external services:

```bash
copy .env.example .env
```

PowerShell alternative:

```powershell
Copy-Item .env.example .env
```

Available variables:

```env
PORT=5000
MONGODB_URI=mongodb://127.0.0.1:27017/staffsync
JWT_SECRET=replace-with-a-long-random-secret
```

The current starter uses in-memory API data so the dashboard works immediately. The API contracts and environment configuration are ready for MongoDB and Mongoose models.

## Available scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Starts the frontend and Express API together |
| `npm run client` | Starts only the Vite development server |
| `npm run server` | Starts only the Express API |
| `npm run build` | Creates a production frontend build |
| `npm run preview` | Previews the production frontend build |

## API endpoints

| Method | Endpoint | Description |
| --- | --- | --- |
| `GET` | `/api/health` | Checks whether the API is running |
| `POST` | `/api/auth/login` | Creates a JWT session |
| `GET` | `/api/employees` | Returns employee records |
| `GET` | `/api/leave-requests` | Returns leave requests |
| `PATCH` | `/api/leave-requests/:id` | Approves or declines a request |
| `GET` | `/api/announcements` | Returns workspace announcements |

## Project structure

```text
StaffSync/
├── server/
│   └── index.js          # Express API and JWT login
├── src/
│   ├── main.jsx          # React app, screens, state, and interactions
│   └── styles.css        # Responsive application styling
├── .env.example          # Environment variable template
├── .gitignore             # Git exclusions
├── index.html             # Vite entry HTML
├── package.json           # Scripts and dependencies
├── package-lock.json      # Locked dependency versions
└── vite.config.js         # Vite and API proxy configuration
```

## Uploading to GitHub

Upload these project files and folders:

```text
.gitignore
.env.example
index.html
package.json
package-lock.json
vite.config.js
README.md
server/
src/
```

Do **not** upload:

```text
node_modules/
dist/
.env
*.log
.vscode/
.idea/
```

These files are excluded by [.gitignore](./.gitignore).

## Roadmap

- MongoDB persistence with Mongoose models
- Protected API middleware for JWT verification
- Full HR, manager, and employee dashboards
- Employee profile editing and document management
- Real attendance check-in and check-out
- Payroll and reporting workflows
- Email notifications for leave and announcements
- Production deployment configuration

## License

This project is intended for educational, portfolio, and product-prototyping use.

---

Built with React, Node.js, Express, JWT, and a focus on better people operations.
