# REST-API-using-DJANGO

📂 Project Overview
This project is a Django REST Framework API for managing user profiles.
It supports full CRUD operations (Create, Read, Update, Delete) via REST endpoints.

⚙️ Features
List & Create user profiles at /api/users/

Retrieve, Update, Delete individual profiles at /api/users/<id>/

Fields: name, email, bio, profile_picture

Admin panel integration for managing profiles

🛠️ Setup Instructions
1. Clone or create project
bash
django-admin startproject userprofile_project
cd userprofile_project
python manage.py startapp users
2. Install dependencies
bash
pip install django djangorestframework
3. Add apps in settings.py
python
INSTALLED_APPS = [
    ...
    'rest_framework',
    'users',
]
4. Apply migrations
bash
python manage.py makemigrations
python manage.py migrate
5. Create superuser 
bash
python manage.py createsuperuser
Username: admin
Password: Admin12345
7. Run server
bash
python manage.py runserver
📌 API Endpoints
Endpoint	Method	Description
/api/users/	GET	List all profiles
/api/users/	POST	Create new profile
/api/users/<id>/	GET	Retrieve profile
/api/users/<id>/	PUT/PATCH	Update profile
/api/users/<id>/	DELETE	Delete profile


🧪 Example Requests
Create Profile
json
POST /api/users/
{
  "name": "john",
  "email": "john123@gmail.com",
  "bio": "Customer Care Executive",
  "profile_picture": null
}
Update Profile
json
PATCH /api/users/1/
{
  "bio": "Now working in Noida"
}
Delete Profile
Code
DELETE /api/users/1/
