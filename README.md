# Notes Creator

**Short:** Full-stack notes management app with JWT auth, Django (DRF) backend and React frontend.

## Demo
![screenshot](docs/screenshot-notes.gif)  // replace with actual image

## Tech stack
- Backend: Python, Django, Django REST Framework
- Frontend: React.js, Tailwind CSS
- Auth: JWT
- DB: PostgreSQL / MySQL
- Dev: Docker, Git, GitHub Actions

## Features
- User signup / login (JWT)
- Create / Read / Update / Delete notes
- Protected routes and role-ready structure

## Run locally (quick)
```bash
# Backend
cd backend
python -m venv venv
source venv/bin/activate      # or venv\Scripts\activate on Windows
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver

# Frontend
cd frontend
npm install
npm run dev
