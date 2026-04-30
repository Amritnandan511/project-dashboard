#  Flowspace — Project Management App

A fully-featured, role-based project management web app built as a single standalone HTML file. No backend, no dependencies, no build step — just open and use.

![HTML](https://img.shields.io/badge/HTML-Single%20File-orange?style=flat-square&logo=html5)
![CSS](https://img.shields.io/badge/CSS-Vanilla-blue?style=flat-square&logo=css3)
![JS](https://img.shields.io/badge/JavaScript-Vanilla-yellow?style=flat-square&logo=javascript)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

##  Features

###  Authentication
- Sign up and sign in with email & password
- Form validation (email format, minimum password length, duplicate detection)
- One-click demo login for **Admin** and **Member** roles
- Role-based access control throughout the entire UI

###  Project Management
- Create, edit, and delete projects
- Assign emoji icons and team members per project
- Visual progress bar based on task completion
- Project detail view with filtered task list
- Admin-only edit/delete controls

### ✅ Task Management
- Full CRUD — create, edit, delete tasks
- Fields: name, project, notes, priority, status, assignee, due date
- Four statuses: **To Do**, **In Progress**, **Done**, **On Hold**
- Three priority levels: **High**, **Medium**, **Low**
- Inline status change from the task detail modal
- One-click toggle to mark tasks done/undone
- Overdue detection with visual warnings

### 📊 Dashboard
- Personalized greeting based on time of day
- Live stats: Total Tasks, In Progress, Completed, Overdue
- Overdue alert banner
- Recent tasks list
- Active projects grid

### 🔍 Tasks Page
- Live search bar
- Filter pills: All / To Do / In Progress / Done / On Hold / Overdue / Assigned to Me
- Smart sorting: overdue tasks bubble to top, then sorted by priority

### 👥 Team Management *(Admin only)*
- View all members with task counts and completion stats
- Invite new members with a temporary password
- Toggle roles between Admin and Member
- Remove members (tasks are automatically unassigned)

### 📈 Reports *(Admin only)*
- Completion rate, high-priority open tasks, overdue count
- Bar charts: Tasks by Project, Tasks by Member, Priority breakdown
- Live activity log tracking all key actions

---

## 🚀 Getting Started

### Option 1 — Open directly in browser
```bash
# Just double-click flowspace.html
# Or open it from your browser: File → Open
```

### Option 2 — Serve locally
```bash
# Using Python
python -m http.server 8080

# Using Node.js
npx serve .

# Then visit http://localhost:8080/flowspace.html
```

### Option 3 — Host on GitHub Pages
1. Push `flowspace.html` to a GitHub repository
2. Go to **Settings → Pages → Source: main branch**
3. Your app is live at `https://YOUR_USERNAME.github.io/REPO_NAME/flowspace.html`

---

## 🔑 Demo Credentials

| Role   | Email              | Password   |
|--------|--------------------|------------|
| Admin  | admin@demo.com     | password   |
| Member | member@demo.com    | password   |

> The app ships with 4 demo users, 3 projects, and 10 tasks so you can explore immediately.

---

## 🏗 Project Structure

```
flowspace.html          # The entire app — HTML + CSS + JS in one file
README.md               # This file
```

The app is intentionally a single file for maximum portability. Everything lives in `flowspace.html`:

| Section       | Description                                          |
|---------------|------------------------------------------------------|
| `<style>`     | All CSS — design system, components, dark theme      |
| Auth Screen   | Login / Signup UI                                    |
| App Shell     | Topbar, Sidebar, Content area                        |
| Pages         | Dashboard, Projects, Tasks, Team, Reports            |
| Modals        | Create/Edit Project, Create/Edit Task, Invite Member |
| `<script>`    | Data store, all logic, rendering, event handlers     |

---

## 🎨 Tech Stack

| Layer      | Technology                        |
|------------|-----------------------------------|
| Markup     | HTML5                             |
| Styling    | Vanilla CSS (custom properties)   |
| Logic      | Vanilla JavaScript (ES6+)         |
| Fonts      | Google Fonts — DM Sans + Playfair Display |
| Storage    | In-memory (JS object)             |
| Backend    | None required                     |

> **Note:** Data resets on page refresh since there's no persistent backend. To add persistence, wire up `localStorage` or connect a backend API.

---

## 👤 Role Permissions

| Feature                  | Admin | Member |
|--------------------------|:-----:|:------:|
| View Dashboard           | ✅    | ✅     |
| Create / Edit Projects   | ✅    | ❌     |
| Delete Projects          | ✅    | ❌     |
| Create Tasks             | ✅    | ✅     |
| Edit / Delete Any Task   | ✅    | ❌     |
| Update Own Task Status   | ✅    | ✅     |
| View Team Page           | ✅    | ❌     |
| Invite / Remove Members  | ✅    | ❌     |
| Change Member Roles      | ✅    | ❌     |
| View Reports             | ✅    | ❌     |

---

## 🔮 Potential Enhancements

- **Persistent storage** — connect to `localStorage`, IndexedDB, or a REST API
- **Real authentication** — JWT tokens, OAuth (Google/GitHub)
- **Comments** on tasks
- **File attachments** per task
- **Drag-and-drop** Kanban board view
- **Email notifications** for assignments and due dates
- **Dark/light mode toggle**
- **Export to CSV / PDF**

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

> Built with ❤️ using plain HTML, CSS, and JavaScript — no frameworks, no build tools, no nonsense.
