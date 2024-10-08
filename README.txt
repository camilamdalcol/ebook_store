# Django Project Setup Guide

## Step-by-Step Instructions

1. **Create and activate a virtual environment**:
    python -m venv env
    .\env\Scripts\activate  # On Windows
    source env/bin/activate  # On macOS/Linux

2. **Install the required packages**:
    
    pip install -r requirements.txt

3. **Create a PostgreSQL database and user:**
  
    CREATE DATABASE your_database_name;
    CREATE USER your_username WITH PASSWORD 'your_password';
    GRANT ALL PRIVILEGES ON DATABASE your_database_name TO your_username;

4. **Update the settings.py file with your database details:**

    DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_database_name',
        'USER': 'your_username',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
        }
       }

5. **Apply database migrations:**

    python3 manage.py makemigrations
    python3 manage.py migrate

6. **Create a superuser:**

    python3 manage.py createsuperuser

7. **Run the development server:**

    python3 manage.py runserver

Your Django project should now be up and running at http://127.0.0.1:8000/.


Render url: https://django-ebook-store.onrender.com

