API Documentation - Dashboard Project
Base URL
http://localhost:5000/api
Authentication
1. Register User

Endpoint: /auth/register
Method: POST
Description: Creates a new user.

Request Body:

{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "password123"
}


Response:

{
  "id": "userId",
  "name": "John Doe",
  "email": "john@example.com",
  "token": "JWT_TOKEN"
}

2. Login User

Endpoint: /auth/login
Method: POST
Description: Logs in a user and returns a JWT token.

Request Body:

{
  "email": "john@example.com",
  "password": "password123"
}


Response:

{
  "id": "userId",
  "name": "John Doe",
  "email": "john@example.com",
  "token": "JWT_TOKEN"
}

3. Get Profile

Endpoint: /auth/profile
Method: GET
Headers: Authorization: Bearer JWT_TOKEN
Description: Returns logged-in user’s profile.

Response:

{
  "id": "userId",
  "name": "John Doe",
  "email": "john@example.com"
}

Tasks CRUD
1. Get All Tasks

Endpoint: /tasks
Method: GET
Headers: Authorization: Bearer JWT_TOKEN
Description: Fetch all tasks of the logged-in user.

Response:

[
  {
    "_id": "taskId1",
    "title": "Task 1",
    "description": "Task description",
    "completed": false
  },
  ...
]

2. Create Task

Endpoint: /tasks
Method: POST
Headers: Authorization: Bearer JWT_TOKEN
Request Body:

{
  "title": "New Task",
  "description": "Task description"
}


Response:

{
  "_id": "taskId",
  "title": "New Task",
  "description": "Task description",
  "completed": false
}

3. Update Task

Endpoint: /tasks/:id
Method: PUT
Headers: Authorization: Bearer JWT_TOKEN
Request Body: (any field to update)

{
  "title": "Updated Task",
  "description": "Updated description",
  "completed": true
}


Response:

{
  "_id": "taskId",
  "title": "Updated Task",
  "description": "Updated description",
  "completed": true
}

4. Delete Task

Endpoint: /tasks/:id
Method: DELETE
Headers: Authorization: Bearer JWT_TOKEN
Description: Deletes the task with given ID.

Response:

{
  "message": "Task deleted successfully"
}