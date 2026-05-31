# REST-API-using-DJANGO

This project demonstrates how to build and manage a Posts REST API using Django REST Framework. It covers everything from basic API setup to advanced features like authentication, permissions, filtering, and search.

Features Covered
1. Hello World API
Created a simple REST endpoint (/api/hello/) that returns "Hello World".

Confirms that the REST framework is working correctly.

2. Creating Models in Admin
Defined a Post model with fields like title, content, author, and created_at.

Registered the model in Django Admin for easy management.

Admin credentials:

Username: admin

Password: 1234512345

3. Posting APIs
Implemented POST /api/posts/ to create new posts.

Uses serializers to validate and save data.

4. Segregating into Pages
Added pagination to API responses.

Example: /api/posts/?page=2 returns the second page of posts.

5. Setting Authentication
Enabled Token Authentication for secure access.

User credentials:

Username: user

Password: Bhawna@2026

6. Adding Username to Posts
Automatically attaches the logged-in user’s username to each post created.

Ensures accountability and ownership of posts.

7. Adding Permissions
Configured permissions so only authenticated users can create posts.

Only the author can edit or delete their own posts.

8. Filtering by Username
Added query parameter: /api/posts/?username=user1

Returns posts created by a specific user.

9. Search Filter
Implemented search functionality: /api/posts/?search=keyword

Allows searching posts by title or content.

10. Filtering by Date
Added date filter: /api/posts/?created_at=2026-05-31

Returns posts created on a specific date.

11. Ordering Filters
Supports ordering by fields: /api/posts/?ordering=-created_at

Example: -created_at → newest posts first.

Tech Stack
Backend: Django, Django REST Framework

Database: SQLite (default, can be replaced with PostgreSQL/MySQL)

Auth: Token-based authentication

How to Run
Clone the repository.

Install dependencies:


pip install django djangorestframework
Run migrations:


python manage.py makemigrations
python manage.py migrate
Create superuser (admin):


python manage.py createsuperuser
Start server:


python manage.py runserver
Access APIs at:

http://127.0.0.1:8000/api/posts/

http://127.0.0.1:8000/admin/
