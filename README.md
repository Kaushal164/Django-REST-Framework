# DRF Student Management API

A Django REST Framework project for managing student information.

## Features

- Student model with name, age, description, and enrollment date
- RESTful API endpoints for student operations
- Token-based authentication
- Django admin interface

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd drf-tuts/drfproj
   ```

2. Install dependencies:
   ```bash
   pip install django djangorestframework
   ```

3. Run migrations:
   ```bash
   python manage.py migrate
   ```

4. Create a superuser:
   ```bash
   python manage.py createsuperuser
   ```

5. Run the development server:
   ```bash
   python manage.py runserver
   ```

## API Endpoints

### Authentication
- `POST /api/token/` - Obtain authentication token

### Student API
- `GET /` - Retrieve the first student (requires authentication)
- `POST /` - Create a new student (requires authentication)

### Admin
- `/admin/` - Django admin interface

## Usage

1. Obtain an authentication token by posting to `/api/token/` with username and password.
2. Include the token in the Authorization header for API requests: `Authorization: Token <your-token>`
3. Use the API endpoints to manage student data.

## Models

### Student
- `name` (CharField, max_length=100)
- `age` (IntegerField)
- `description` (TextField)
- `date_enrolled` (DateTimeField, auto_now=True)

## Technologies Used

- Django 6.0.3
- Django REST Framework
- SQLite (default database)