
# Django Project Setup

This document provides a step-by-step guide to setting up and running a Django project.

## Prerequisites

Ensure the following are installed on your system:
- Python (version 3.8 or higher)
- Pip (Python package manager)
- Virtualenv (optional but recommended for environment isolation)
- A database system (e.g., SQLite, PostgreSQL, MySQL)

---

## Setup Instructions

### Step 1: Clone the Repository
```bash
git clone <https://github.com/umairinayat/DevSerach.git>
cd <DevSerach>
```

### Step 2: Create a Virtual Environment
Create a virtual environment to isolate dependencies:
```bash
python -m venv env
```

Activate the virtual environment:
- **Linux/MacOS:**
  ```bash
  source env/bin/activate
  ```
- **Windows:**
  ```bash
  env\Scripts\activate
  ```

### Step 3: Install Dependencies
Install all required packages from `requirements.txt`:
```bash
pip install -r requirements.txt
```

### Step 4: Configure Environment Variables
Set up environment variables required for the project. You can create a `.env` file and add key-value pairs:
```
DEBUG=True
SECRET_KEY=your_secret_key
DATABASE_URL=your_database_url
```

Make sure the project is configured to read from this file (e.g., using `django-environ`).

### Step 5: Apply Migrations
Run Django migrations to set up the database schema:
```bash
python manage.py migrate
```

### Step 6: Create a Superuser
To access the Django Admin, create a superuser account:
```bash
python manage.py createsuperuser
```

### Step 7: Start the Development Server
Run the server locally:
```bash
python manage.py runserver
```

Visit the server at [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

---

## Additional Commands

### Run Tests
To run tests for the application:
```bash
python manage.py test
```

### Collect Static Files
For production, collect static files:
```bash
python manage.py collectstatic
```

---

## Common Issues and Solutions

### Missing Dependencies
Ensure you installed dependencies with:
```bash
pip install -r requirements.txt
```

### Database Connection Errors
Double-check your `DATABASE_URL` or database settings in `settings.py`.

### Debugging
Set `DEBUG=True` in your `.env` file to enable detailed error messages (for development only).

---

## Deployment
For deployment, consider using platforms like **Heroku**, **AWS**, or **Docker**. Ensure you:
1. Set `DEBUG=False`.
2. Configure a production-ready database.
3. Set up static and media file hosting.

---

Feel free to reach out for further support! 😊
