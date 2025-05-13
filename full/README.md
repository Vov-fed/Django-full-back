# 📰 Django + React Blog API Project

A full-stack blog platform built with **Django REST Framework** and **React (Vite)**.  
Users can register, login, browse articles, post/edit/delete their own comments, and view others.  
Admins can create/manage articles.  

---

## 🔧 Technologies Used

- **Backend**: Django, Django REST Framework, SimpleJWT, Python Decouple
- **Frontend**: React with Vite, Axios
- **Database**: SQLite
- **Authentication**: JWT tokens (access + refresh)

---

## 📦 Features

### 🔐 Authentication
- JWT login/register
- Tokens saved in localStorage
- Custom token includes username

### 📄 Articles
- List and search all articles (open to all)
- View article detail + comments
- Admin can create/edit/delete articles

### 💬 Comments
- Authenticated users can post, edit, and delete their own comments
- Admin can manage all comments

### 🧑‍💻 User Roles
- Admin: full control
- Regular user: post and manage own comments only

---

## 🔁 API Endpoints

### 🔑 Auth
- `POST /api/register/`
- `POST /api/token/`
- `POST /api/token/refresh/`

### 📄 Articles
- `GET /api/articles/`
- `GET /api/articles/<id>/`
- `POST /api/articles/` (admin only)
- `PUT/PATCH/DELETE /api/articles/<id>/` (admin only)

### 💬 Comments
- `GET /api/articles/<article_id>/comments/`
- `POST /api/articles/<article_id>/comments/`
- `PATCH /api/comments/<id>/` (owner only)
- `DELETE /api/comments/<id>/` (owner or admin)

---

## 🌱 Seed Data

- 2 users:
  - 1 admin
  - 1 regular user
- 2 articles
- 2 comments per article

All created via Django Admin panel.

---

## 🧪 How to Run

### Backend
```bash
pipenv install
pipenv shell
python manage.py runserver
```

admin userName: vladimirfedoruk
admin password: Fedova@307

### Frontend
```bash
cd frontend
npm install
npm run dev
```

---

## 🛡 Environment (.env)

Using `python-decouple`, the backend reads from a `.env` file:

```
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=127.0.0.1,localhost
```

---

## 📦 Backend Requirements

List from `requirements.txt`:

```
asgiref==3.8.1
django==4.2.20
psycopg2-binary==2.9.10
python-decouple==3.8
sqlparse==0.5.3
typing-extensions==4.13.0
```

---

## 💻 Frontend Features

- Vite + React
- Axios for API calls
- JWT stored in localStorage
- Routes:
  - `/` — Article list (with search)
  - `/login` — Login form
  - `/register` — Register form
  - `/articles/:id` — Article detail + comments
- Responsive UI (custom CSS)
- Conditional rendering for login/logout/comment controls

---

## ✅ Submission Checklist (As per PDF)

- [x] Django + DRF backend
- [x] JWT Auth (SimpleJWT)
- [x] React frontend (Vite)
- [x] Article + Comment models
- [x] Permissions & roles
- [x] .env file
- [x] Clean UI (responsive)
- [x] Seeded DB
- [x] Working API endpoints
- [x] Full documentation (this file ✅)

---

## 📸 Screenshots (add here)

- Home / Articles
- Article + Comments
- Comment editing
- Login/Register
- Admin panel
