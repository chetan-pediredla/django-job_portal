# django-job_portal

# Django Project README

This is a Django project for [project name/description].

## Setup Instructions

Follow these steps to set up and run the project locally:

### 1. Create a Virtual Environment

```bash
# Create a new virtual environment (replace 'env' with your preferred name)
python -m venv env

# Activate the virtual environment
# On Windows
env\Scripts\activate
# On macOS/Linux
source env/bin/activate


# Make sure pip is up-to-date
pip install --upgrade pip

# Install dependencies from requirements.txt
pip install -r requirements.txt


# Apply database migrations
python manage.py makemigrations
python manage.py migrate


# Create a superuser for accessing the Django admin interface
python manage.py createsuperuser
# Follow the prompts to set your username, email, and password

# Start the Django development server
python manage.py runserver
