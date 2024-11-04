# Employee Management API

This is a RESTful API for managing employee records, built using Django and Django REST Framework. It includes features such as employee CRUD operations, pagination, filtering, and JWT authentication.

## Features

- **Employee CRUD Operations**: Create, Read, Update, and Delete employee records.
- **JWT Authentication**: Secure endpoints with token-based authentication.
- **Pagination**: Limit results per page to 10 employees, with support for multiple pages.
- **Filtering**: Filter employees by department and role.

## Technologies Used

- Python
- Django
- Django REST Framework
- Django Filters
- Simple JWT for authentication

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Mahesh6221/emp_management
   cd emp_management

## Run migrations:

python manage.py makemigrations

## Apply migrations:

python manage.py migrate

## Create a superuser (for accessing the Django admin):
python manage.py createsuperuser


## Run the development server:

python manage.py runserver


## Access the API:

Open your browser and go to http://127.0.0.1:8000/api/employees/ to view the API endpoints.

## API Endpoints
## Authentication
## Token Generation:

## POST /api/token/
Body:
json
Copy code
{ 
  "username": "yourusername", 
  "password": "yourpassword" 
}
Returns: JWT token for authentication.
Employee Endpoints
Get All Employees:

## GET /api/employees/
Supports pagination and filtering by department and role.
Get Single Employee:

## GET /api/employees/{id}/
Retrieve details of a single employee by ID.
Create Employee:

## POST /api/employees/
Body:
json
{ 
  "name": "John Doe", 
  "department": "HR", 
  "role": "Manager" 
}

Creates a new employee record.

## Update Employee:

## PUT /api/employees/{id}/
Body:
json
Copy code
{ 
  "name": "John Doe", 
  "department": "HR", 
  "role": "Senior Manager" 
}
Updates the employee record by ID.


## Delete Employee:

## DELETE /api/employees/{id}/
Deletes the employee record by ID.

## Pagination
To paginate through the employee list, use the page query parameter:

Example: GET /api/employees/?page=1 to get the first 10 employees.
Example: GET /api/employees/?page=2 to get the next 10 employees.


## Filtering
You can filter employees by department and role using query parameters:
Example: GET /api/employees/?department=HR
Example: GET /api/employees/?role=Manager
