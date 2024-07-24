## django-job_portal


This is a Django project for job_portal.

## Setup Instructions

Follow these steps to set up and run the project locally:

### 1. Create a Virtual Environment


Create a new virtual environment (replace 'env' with your preferred name)
```
python -m venv env
```
Activate the virtual environment
- On Windows
```
env\Scripts\activate
```
or 
```
.env/Scripts/activate
```
- On macOS/Linux
```
source env/bin/activate
```

### 2. Install Requirements
Make sure pip is up-to-date
```
pip install --upgrade pip
```
Install dependencies from requirements.txt
```
pip install -r requirements.txt
```

### 3. Make Migrations
Apply database migrations
```
python manage.py makemigrations
python manage.py migrate
```
### 4. Create a Super User

Create a superuser for accessing the Django admin interface
```
 python manage.py createsuperuser
```
Follow the prompts to set your username, email, and password

### 5. Start the Django development server
```
python manage.py runserver
```
The development server should now be running at http://127.0.0.1:8000/
