WorkHub - Freelance Job Portal
Overview
WorkHub is a full-stack web application designed to connect freelancers with clients for project collaboration. Inspired by platforms like Upwork and Fiverr, it offers essential features such as user registration, profile management, job posting, applications, and communication, all built with Python (Flask) backend and a modern responsive frontend. The project aims to provide a robust, extendable, and easy-to-deploy freelance marketplace.
Features
User Authentication: Sign up and login for freelancers and clients, with password hashing and session management.
Profiles: Create and update freelancer and client profiles, including skills, portfolios, and personal info.
Job Posting: Clients can post detailed jobs with categories, skills, budgets, and durations.
Find Freelancers: Browse, search, and filter freelancers based on skills, rates, and ratings.
Applications: Freelancers can apply for jobs; clients can review proposals, accept or reject applications.
Communication: Basic messaging system between users.
Admin Panel: Manage users, jobs, and applications through admin API endpoints.
Dark Mode: Toggle interface theme with persistent user preference.
Responsive UI: Mobile-friendly design for ease of access across devices.
Technologies Used
Backend
Python 3.x
Flask web framework
SQLite (via SQLAlchemy)
RESTful API architecture
Frontend
HTML, CSS (CSS variables & media queries)
Vanilla JavaScript (fetch API, modals, dark mode toggle)
Setup & Deployment
Prerequisites
Python 3.x installed
Basic knowledge of command line
Code editor (VSCode, Sublime Text, etc.)
Browser (Chrome, Firefox, etc.)
Installation
Clone or download the repository:
bash
git clone <repository_url>
cd workhub
Create a virtual environment and activate it:
bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:
bash
pip install -r requirements.txt
Initialize the database (if not done automatically):
python
python
>>> from app import app
>>> with app.app_context():
...     db.create_all()
>>> exit()
Run the backend server:
bash
python app.py
The API will be accessible at http://127.0.0.1:5000/.
Serve the frontend:
Open another terminal, navigate to project folder:
bash
python -m http.server 8000
Open browser: http://localhost:8000/index.html
Usage
Open the frontend in your browser.
Register as either a Freelancer or Client.
Use the modals to Login, Register, Post a Job, or Find Freelancers.
Browse jobs, apply, chat, and manage projects directly from the interface.
Admin endpoints allow managing users and jobs programmatically or via API tools like Postman.
API Endpoints
Please refer to API_DOCS.md for detailed routes, request/response schemas, and usage examples.
File Structure
text
workhub/
│
├── app.py                # Flask backend with endpoints and database setup
├── requirements.txt      # Required Python dependencies
├── index.html            # Frontend UI with responsive design
├── static/               # Static assets (images, icons, etc.) if added
├── README.md             # This file
└── CONNECT_GUIDE.md      # Guide to connect frontend and backend
Future Enhancements
Implement real-time messaging & notifications
Integrate escrow payment system
Add skill tests, badges, and verification
Develop admin dashboard with analytics
Include user review & rating system
Extend to mobile app (React Native, Flutter)
License
This project is open source under the MIT License. Feel free to modify, extend, and deploy.
