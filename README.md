# Todo-List-API
Build a RESTful API to allow users to manage their to-do list.

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

![TodoListAPI1](https://github.com/user-attachments/assets/38b2ca5b-e8b3-4693-81d1-577a10b094a0)

This will validate the given details, make sure the email is unique and store the user details in the database. Make sure to hash the password before storing it in the database. Respond with a token that can be used for authentication if the registration is successful.

![TodoListAPI2](https://github.com/user-attachments/assets/ab94bc59-fef7-43f9-b178-b9782c0b824b)

The token can either be a JWT or a random string that can be used for authentication. We leave it up to you to decide the implementation details.


# User Login

Authenticate the user using the following request:

![TodoListAPI3](https://github.com/user-attachments/assets/39e76fcd-433b-49b0-b074-e72c5d7b921d)

This will validate the given email and password, and respond with a token if the authentication is successful.

![TodoListAPI4](https://github.com/user-attachments/assets/3516e188-e645-4bfe-b35d-6ce40b063a11)

# Create a To-Do Item

Create a new to-do item using the following request:

![TodoListAPI5](https://github.com/user-attachments/assets/a129b30a-3789-490c-87cb-9c277a85cb96)

User must send the token received from the login endpoint in the header to authenticate the request. You can use the Authorization header with the token as the value. In case the token is missing or invalid, respond with an error and status code 401.

![TodoListAPI6](https://github.com/user-attachments/assets/c97e7808-a478-4e9a-a9b1-13561c1c996a)

Upon successful creation of the to-do item, respond with the details of the created item.

![TodoListAPI7](https://github.com/user-attachments/assets/be8793fa-8dfd-40b8-a3f2-b099ecd1ba06)

# Update a To-Do Item

Update an existing to-do item using the following request:

![TodoListAPI8](https://github.com/user-attachments/assets/8fadb067-2289-472c-bb31-0a4225f93f13)

Just like the create todo endpoint, user must send the token received. Also make sure to validate the user has the permission to update the to-do item i.e. the user is the creator of todo item that they are updating. Respond with an error and status code 403 if the user is not authorized to update the item.

![TodoListAPI9](https://github.com/user-attachments/assets/ab5d06aa-e14d-4371-8861-18e887ee77cd)

Upon successful update of the to-do item, respond with the updated details of the item.

![TodoListAPI10](https://github.com/user-attachments/assets/c675f6cb-6029-450a-9ef0-e657075d5830)

# Delete a To-Do Item

Delete an existing to-do item using the following request:

![TodoListAPI11](https://github.com/user-attachments/assets/70ebccaf-4f23-433a-848d-311c77e4e315)

User must be authenticated and authorized to delete the to-do item. Upon successful deletion, respond with the status code 204.


# Get To-Do Items

Get the list of to-do items using the following request:

![TodoListAPI12](https://github.com/user-attachments/assets/989b70e7-3cba-4890-9f38-7aabfdbe7342)

User must be authenticated to access the tasks and the response should be paginated. Respond with the list of to-do items along with the pagination details.

![TodoListAPI13](https://github.com/user-attachments/assets/cfc90b63-7e85-4caa-8aa8-92c01bb07fc1)

# Bonus 

* Implement filtering and sorting for the to-do list
* Implement unit tests for the API
* Implement rate limiting and throttling for the API
* Implement refresh token mechanism for the authentication

  





















  

