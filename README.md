Task API

A simple REST API for managing tasks, built with Node.js and Express.

Installation and running

Clone or download this project, open a terminal in the project folder, and install the dependencies:

npm install


Start the API with:

npm start


The API will run at:

http://localhost:3000


Swagger API documentation is available at:

http://localhost:3000/docs

API endpoints
Method	Endpoint	Description
GET	/	Returns basic API information
GET	/health	Checks whether the API is running
GET	/tasks	Returns all tasks
GET	/tasks/:id	Returns one task by ID
POST	/tasks	Creates a new task
PUT	/tasks/:id	Updates an existing task
DELETE	/tasks/:id	Deletes a task
GET	/docs	Opens the Swagger UI documentation
Example curl output

Example request:

curl -i http://localhost:3000/health


Example response:

HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8

{"status":"ok"}

Swagger documentation

The API includes interactive Swagger documentation.

Open:

http://localhost:3000/docs


A screenshot of the Swagger UI is included in this repository as swagger.png.

Important note about data

This API currently stores tasks in memory rather than in a database. This means that tasks created while the server is running will be lost when the server is stopped or restarted.

Project structure
CRUD-API/
├── server.js
├── openapi.json
├── package.json
├── package-lock.json
├── swagger.png
├── .gitignore
└── README.md