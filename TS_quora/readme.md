# TS_Quora - A Django-based Q&A Platform

TS_Quora is a simple Quora-like web application built using Django. It allows users to register, login, post questions, answer them, and like answers from others.

## Features

- User Registration and Authentication (Login/Logout)
- Post questions (only by authenticated users)
- Answer questions (any logged-in user can answer)
- Like answers (users can like others' answers)
- Simple UI using Django Templates

## Tech Stack

- **Backend:** Django (Python)
- **Database:** SQLite (default)
- **Frontend:** HTML, CSS (via Django Templates)
- **Environment:** Virtualenv (Python)


## Models Overview

- **User** (from Django's built-in User model)
- **Question**
  - `title`
  - `description`
  - `user` (ForeignKey to User)
- **Answer**
  - `question` (ForeignKey to Question)
  - `answer_text`
  - `user` (ForeignKey to User)
- **Like**
  - `answer` (ForeignKey to Answer)
  - `user` (ForeignKey to User)

## Installation and Setup

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd TS_quora

2. **Create virtual environment & activate**
python -m venv myenv
source myenv/bin/activate   # On Windows: myenv\Scripts\activate

3. **Install dependencies**
pip install -r requirements.txt

4. **Run migrations**
python manage.py migrate

5. **Start development server**
python manage.py runserver

6. **Create superuser to access admin panel**
python manage.py createsuperuser

