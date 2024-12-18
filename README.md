# Todo-List-API
Build RESTful API to allow users to manage their to-do list.

In this project you are required to develop a RESTful API to allow users to manage their to-do list. The previous backend projects have only focused on the CRUD operations, but this project will require you to implement user authentication as well.

![TodoListAPI](https://github.com/user-attachments/assets/2e7819ba-a95e-47b6-bc09-9b3974e71d56)


# Goals

The skills you will learn from this project include:

* User authentication
* Schema design and Databases
* RESTful API design
* CRUD operations
* Error handling
* Security

# Requirements

You are required to develop a RESTful API with following endpoints

* User registration to create a new user
* Login endpoint to authenticate the user and generate a token
* CRUD operations for managing the to-do list
* Implement user authentication to allow only authorized users to access the to-do list
* Implement error handling and security measures
* Use a database to store the user and to-do list data (you can use any database of your choice)
* Implement proper data validation
* Implement pagination and filtering for the to-do list

  
Given below is a list of the endpoints and the details of the request and response:  

# User Registration

Register a new user using the following request:

    POST / Register
    {
      "name" : "John Doe",
      "email" : "john@doe.com",
      "password" : "password"
    }


This will validate the given details, make sure the email is unique and store the user details in the database. Make sure to hash the password before storing it in the database. Respond with a token that can be used for authentication if the registration is successful.

    {
      "token" : "hjfgj%or85u%kg@ln(60yt#ghtywm"
    }


The token can either be a JWT or a random string that can be used for authentication. We leave it up to you to decide the implementation details.


# User Login

Authenticate the user using the following request:

    POST /login
    {
      "email" : "john@doe.com",
      "password" : "password"
    }


This will validate the given email and password, and respond with a token if the authentication is successful.

    {
      "token" : "tu67@kg(#$lgt^pq@h80vn$kghrks"
    }


# Create a To-Do Item

Create a new to-do item using the following request:

    POST /todos
    {
      "title" : "Buy groceries",
      "description" : "Buy milk, eggs, bread, and cheese"
    }


User must send the token received from the login endpoint in the header to authenticate the request. You can use the Authorization header with the token as the value. In case the token is missing or invalid, respond with an error and status code 401.

    {
      "message" : "Unauthorized"
    }


Upon successful creation of the to-do item, respond with the details of the created item.

    {
      "id" : 1,
      "title" : "Buy groceries",
      "description" : "Buy milk, eggs and bread"
    }


# Update a To-Do Item

Update an existing to-do item using the following request:

    PUT /todos/1
    {
      "title" : "Buy groceries",
      "description" : "Buy milk, eggs, and Cheese"
    }


Just like the create todo endpoint, user must send the token received. Also make sure to validate the user has the permission to update the to-do item i.e. the user is the creator of todo item that they are updating. Respond with an error and status code 403 if the user is not authorized to update the item.

    {
      "message" : "Forbidden"
    }


Upon successful update of the to-do item, respond with the updated details of the item.

    {
      "id" : 1,
      "title" : "Buy groceries",
      "description" : "Buy milk, eggs, bread and cheese"
    }


# Delete a To-Do Item

Delete an existing to-do item using the following request:

    DELETE /todos/1

User must be authenticated and authorized to delete the to-do item. Upon successful deletion, respond with the status code 204.


# Get To-Do Items

Get the list of to-do items using the following request:

    GET /todos?page=1&limit=10


User must be authenticated to access the tasks and the response should be paginated. Respond with the list of to-do items along with the pagination details.

    {
     "data" : [
         {
           "id" : 1,
           "title" : "Buy groceries",
           "description" : "Buy milk, eggs, bread"
         },
         {
           "id" : 2,
           "title" : "Pay bills",
           "description" : "pay electricity and water bills"
         }
     ],
     "page" : 1,
     "limit" : 10,
     "total" : 2
    }
      


# Bonus 

* Implement filtering and sorting for the to-do list
* Implement unit tests for the API
* Implement rate limiting and throttling for the API
* Implement refresh token mechanism for the authentication

This project will helps one to understand how to design and implement a RESTful API with user authentication. Also learn how to work with databases, handle errors, and implement security measures.

Project submitting url : https://roadmap.sh/projects/todo-list-api

  





















  

