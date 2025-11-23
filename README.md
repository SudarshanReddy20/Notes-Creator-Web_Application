# Notes-Creator

**Full-stack notes app — Django (DRF) backend + React frontend.**  
Lightweight, secure CRUD with JWT auth, Docker support, and simple deployment instructions.

---

## Tech stack
- Backend: Python, Django, Django REST Framework
- Frontend: React, Vite, Tailwind CSS
- Auth: JWT (djangorestframework-simplejwt)
- DB: PostgreSQL (development: SQLite supported)
- Dev: Docker, GitHub Actions

---

## Features
- Email/password signup and JWT login
- Create / Read / Update / Delete notes
- Private user notebooks (notes scoped to user)
- Search and basic tagging
- Example dataset for quick demo

---

## Repo layout
/backend # Django project (API)
├─ app/ # core apps (notes, users)
├─ requirements.txt
/frontend # React app (Vite)
├─ src/
├─ package.json
/docs # screenshots, demo GIFs
/docker-compose.yml

yaml
Copy code

---

## Quickstart — local (Linux / macOS)
**Backend**
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env           # edit DB and SECRET settings as needed
python manage.py migrate
python manage.py createsuperuser  # optional
python manage.py runserver
Frontend

bash
Copy code
cd frontend
npm install
npm run dev
# open http://localhost:5173
Windows note: use venv\Scripts\activate to activate the virtualenv.

Quickstart — Docker
bash
Copy code
docker-compose up --build
# Backend: http://localhost:8000
# Frontend: http://localhost:3000
Environment variables (.env example)
ini
Copy code
DJANGO_SECRET_KEY=your_secret_key
DATABASE_URL=postgres://user:pass@db:5432/notes_db
DEBUG=True
FRONTEND_URL=http://localhost:3000
API endpoints (examples)
POST /api/auth/register/ — register

POST /api/auth/token/ — get JWT

GET /api/notes/ — list user notes

POST /api/notes/ — create note

(Full API docs: /docs or Swagger UI if enabled.)

Tests
bash
Copy code
cd backend
pytest -q
Screenshots / Demo
Place screenshots or a 10–20s demo GIF in /docs and reference them here:
![app-demo](/docs/demo-notes.gif)

Contributing
Fork → branch feature/<name> → PR.

Follow PEP8; run black ..

Add tests for new features.

License
MIT — see LICENSE file.

Contact
Sudarshan Reddy — sudarshan382003@gmail.com
Resume: /mnt/data/Sudarshan_Reddy_Medapati_Resume.pdf
