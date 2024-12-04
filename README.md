Base URL

http://127.0.0.1:8000/api

Endpoints and Usage

1. Register
Endpoint: /register
Method: POST
Request Body:
json
{
    "name": "test name 1",
    "email": "test@gmail.com",
    "password": "12345678",
    "password_confirmation": "12345678"
}
Description:
Creates a new user account.


2. Login
Endpoint: /login
Method: POST
Request Body:
json
{
    "email": "test@gmail.com",
    "password": "12345678"
}
Description:
Authenticates a user and returns a token to access protected routes.


3. Logout
Endpoint: /logout
Method: POST
Headers:
Authorization: Bearer {your_token}
Description:
Logs out the user and invalidates the token.
Note: Token is required.


4. Create a Post
Endpoint: /posts
Method: POST
Headers:
Authorization: Bearer {your_token}
Request Body:
json
{
    "title": "post 2",
    "content": "post content 2"
}
Description:
Adds a new post.
Note: Token is required.


5. Get All Posts
Endpoint: /posts
Method: GET
Description:
Retrieves all posts.


6. Get a Single Post
Endpoint: /posts/{id}
Method: GET
Description:
Retrieves the details of a specific post using its ID.


7. Update a Post
Endpoint: /posts/{id}
Method: PUT
Headers:
Authorization: Bearer {your_token}
Request Body:
json
{
    "title": "updated title",
    "content": "updated content"
}
Description:
Updates an existing post by its ID.
Note: Token is required.


8. Delete a Post
Endpoint: /posts/{id}
Method: DELETE
Headers:
Authorization: Bearer {your_token}
Description:
Deletes a post by its ID.
Note: Token is required.