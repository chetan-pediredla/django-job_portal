## Django-job_portal


This is a Django project for job_portal.

The Job Portal Application is a comprehensive web-based platform designed to bridge the gap between job seekers and potential employers. The application provides an efficient and user-friendly interface for users to search and apply for jobs, while allowing recruiters to post and manage job listings. Built with Django, this application ensures robust and scalable performance.

## Features

- User Registration and Authentication: Secure signup and login functionalities for both job seekers and recruiters.
- Job Listings: Recruiters can post jobs with detailed descriptions and seekers can browse and apply for these jobs.
- Job Application Management: Seamless job application process with status tracking.
- Profile Management: Users can manage their profiles, upload resumes, and update their personal information.
- Email Notifications: Automated email notifications for account creation, job applications, and updates.
- Admin Panel: Admin interface for managing users, jobs, and applications.

## Models

### StudentUser:

Fields: `user, mobile, image, gender, type, resume, is_verified`

Description: Represents a student user with personal details and resume.
### Recruiter:

Fields: `user, mobile, image, gender, type, company, about_company, status`

Description: Represents a recruiter with company details and status.
### Job:

Fields: `recruiter, start_date, end_date, title, salary, image, description, experience, location, skills, eligibility_criteria, job_type, process, role_responsibilities, mode_of_work, creation_date`

Description: Represents a job posting with details about the job, skills required, and the recruitment process.

### Apply:

Fields: `job, student, resume, apply_date, status`

Description: Represents a job application made by a student user for a specific job.

## Technologies Used
- Backend: Django
- Frontend: HTML, CSS, Bootstrap
- Database: SQLite (default), can be configured for PostgreSQL, MySQL, etc.
- Email: SMTP for email notifications
- Authentication: Django's built-in authentication system

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

### 5. Configure Email Sending
To enable email sending from your Django application, add the following configuration to your settings.py file:
```
# Email sending configuration
EMAIL_HOST_USER = 'your_email@gmail.com'  # Your Gmail address or SMTP email
EMAIL_HOST_PASSWORD = 'your_password'  # Your email account's password
```
Replace 'your_email@gmail.com' with your actual email address and 'your_password' with the password for your email account. Ensure that your email provider allows SMTP access and follow their security guidelines, such as enabling "Less secure apps" or generating an "App password" if required.
### 6. Start the Django development server
```
python manage.py runserver
```
The development server should now be running at http://127.0.0.1:8000/
## Usage
- Job Seekers: Register, log in, browse available jobs, and apply for positions.
- Recruiters: Register, log in, post job openings, and manage applications from job seekers.
- Admin: Use the admin panel to manage users, jobs, and applications.

