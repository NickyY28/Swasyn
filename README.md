# Swasyn
AI-powered Health Monitoring &amp; Analysis Platform — bridging patients and doctors through real-time insights, predictive analytics, and smart reports.

# Swasyn – Hospital Management System (HMS) Web App

**Swasyn** is a full-stack web application built to streamline hospital operations — enabling Admins (hospital staff), Doctors, and Patients to interact seamlessly through one system.

### 🚀 Key Features  
- Role-based access: Admin, Doctor, Patient  
- Admin can add/update/delete doctors, view/search patients and appointments  
- Doctors can see their upcoming appointments, mark as completed/cancelled, and update patient treatment history (diagnosis, prescriptions, notes)  
- Patients can register/login, view/edit their profile, search doctors by specialization/availability, book/reschedule/cancel appointments, view past appointment & treatment history  
- Asynchronous/background jobs via Celery + Redis:  
  - Daily reminders for upcoming appointments  
  - Monthly activity report for doctors (sent via email)  
  - Patient-triggered export of treatment records (CSV)  
- Caching (Redis) for performance optimization (e.g., list of available doctors)  
- Built with modern tech stack:  
  - **Backend**: Flask (Python), SQLite (database)  
  - **Frontend**: Vue.js + Bootstrap  
  - **Async Jobs / Cache**: Celery + Redis  

### 📁 Project Structure
/project_root
├── /backend
│   ├── app.py
│   ├── /models
│   ├── /routes
│   ├── celery_worker.py
│   └── requirements.txt
└── /frontend
├── /src
│   ├── /components
│   ├── main.js
│   └── router.js
└── package.json

### 🛠 Why This Stack?  
- **Flask** gives lightweight, flexible backend APIs in Python — perfect when you don’t need heavyweight features of frameworks like Django.  
- **Vue.js** enables fast, reactive and component-based UI — clean separation of concerns.  
- **SQLite** keeps things simple for local/demo deployment (no heavy DB setup).  
- **Redis + Celery** allow background tasks and caching — enhances user experience and handles non-blocking operations (reminders, exports).  
- **Bootstrap** ensures responsive, consistent styling without over-engineering the CSS.

### 🔧 Setup Instructions  
1. Clone the repo.  
2. In `/backend`, create a virtual environment, install dependencies (`pip install -r requirements.txt`).  
3. Run database migrations / model creation (via script).  
4. Start Redis server.  
5. Start Celery worker/beat scheduler for asynchronous tasks.  
6. In `/frontend`, install dependencies (`npm install`), then `npm run serve`.  
7. Access the app at `http://localhost:8080` (or configured port).  
8. Use seeded Admin credentials (specified in docs) to begin.

### ✅ Scope & Limitations  
- This is built for demo/local setup; for production consider using a production-grade DB, HTTPS, secure credentials, etc.  
- No payment gateway integration (unless added as optional feature).  
- For simplicity, some UI flows may be basic; feel free to enhance them.

### 🧾 Future Enhancements (Optional)  
- Generate PDF reports instead of just CSV/HTML.  
- Integrate charts/visualisations (e.g., ChartJS) for Doctor dashboards.  
- Add live notifications (websockets) for real-time updates.  
- Implement mobile-friendly optimisations and PWA support.  

### 📝 Licence  
This project is licensed under the MIT Licence (or your chosen licence).

---
