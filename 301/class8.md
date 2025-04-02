# 301-Read_08

## Questions

### xAPI Design Best Practices

1. What does REST stand for? 
REST stands for Representational State Transfer. It is an architectural style for designing networked applications, relying on stateless communication and standard HTTP methods (such as GET, POST, PUT, DELETE). RESTful APIs allow clients to interact with resources using URLs and HTTP requests in a consistent and scalable manner.

2. REST APIs are designed around a **resources**.
A resource is any object, data, or service that can be accessed via the API. Each resource is identified by a unique URL, and interactions with resources are performed using standard HTTP methods such as:
**GET** (retrieve a resource)
**POST** (create a new resource)
**PUT** (update an existing resource)
**DELETE** (remove a resource)

Resources in REST APIs are typically represented in formats like JSON or XML.

3. What is an identifier of a resource? Give an example.
An identifier of a resource in a REST API is a URI (Uniform Resource Identifier), typically a URL that uniquely identifies a resource.
Example:
If we have a REST API for managing users, a specific user can be identified by a URL like:
`https://api.example.com/users/123`
Here, */users/123* is the resource identifier for the user with *ID 123*.
- A **GET** request to this URL would retrieve the details of that specific user.
- A **DELETE** request to this URL would remove that user from the database.

4. What are the most common HTTP verbs?
*The most common HTTP verbs used in RESTful APIs are:*
**GET** – Retrieves data from the server (e.g., fetching user details).
- Example: GET /users/123 (Fetch user with ID 123)
**POST** – Creates a new resource on the server.
- Example: POST /users (Create a new user)
**PUT** – Updates an existing resource or creates it if it doesn’t exist (idempotent).
- Example: PUT /users/123 (Update user with ID 123)
**PATCH** – Partially updates an existing resource.
- Example: PATCH /users/123 (Update specific fields of user 123)
**DELETE** – Removes a resource from the server.
- Example: DELETE /users/123 (Delete user with ID 123)

5. What should the URIs be based on?
URIs in a RESTful API should be based on resources, not actions or operations. They should be clear, consistent, and hierarchical, following best practices for readability and maintainability.

6. Give an example of a good URI.
A good URI follows RESTful principles by using nouns, being descriptive, and maintaining a clear hierarchy.
- *Example:*
URI for retrieving a specific user's order:
GET `/users/123/orders/456`

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
A *"chatty"* web API refers to an API that requires multiple requests to accomplish a task that could be handled with fewer requests. This often happens when an API provides small pieces of data separately, forcing clients to make many calls to gather all the necessary information.

8. What status code does a successful GET request return?
A successful GET request typically returns the 200 OK status code.

9. What status code does an unsuccessful GET request return?
An unsuccessful GET request can return a variety of HTTP status codes, depending on the nature of the error. Some common ones include:
**404 Not Found**
When: The requested resource does not exist on the server.
**400 Bad Request**
When: The request is malformed or invalid (e.g., incorrect query parameters).
**401 Unauthorized**
When: The request is missing authentication credentials or the credentials provided are invalid.
**403 Forbidden**
When: The server understands the request, but the client does not have permission to access the resource.
**500 Internal Server Error**
When: The server encounters an error while processing the request.

10. What status code does a successful POST request return?
A successful **POST** request typically returns the 201 Created status code when a new resource has been successfully created on the server.
*Other Possible Status Codes for POST:*
- 200 OK → If the server processes the request successfully, but the action does not involve resource creation (e.g., updating something).
- 202 Accepted → If the request has been accepted for processing but not yet completed (asynchronous processing).
- 400 Bad Request → If the POST data is invalid or incomplete.

11. What status code does a successful DELETE request return?
A successful **DELETE** request typically returns the 204 No Content status code, indicating that the resource has been deleted, but there is no content in the response body.
*Other Possible Status Codes for DELETE:*
- 200 OK: If the server returns a message confirming the deletion (not common for DELETE requests but sometimes used).
- 404 Not Found: If the resource to be deleted does not exist.

