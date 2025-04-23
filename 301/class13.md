# 301-Read_13

## Questions 
# CRUD Basics
1. Which HTTP method would you use to update a record through an API?
To update a record through an API, you would use the PUT or PATCH HTTP method.
PUT is used when you want to replace the entire record with a new one.
PATCH is used when you want to update only part of the record.

*Why: They are designed for updates:*
- PUT = full update
- PATCH = partial update
This tells the server exactly what kind of change you're making.

2. Which REST methods require an ID parameter?
In REST, GET, PUT, PATCH, and DELETE typically require an ID when you're working with a specific record.

*Simple breakdown:*
- GET /items/123 → Get item with ID 123
- PUT /items/123 → Replace item 123
- PATCH /items/123 → Update part of item 123
- DELETE /items/123 → Delete item 123
*Why: The ID tells the API which specific item you're acting on.*

## Videos
*Speed Coding: Building a CRUD API (Watch a Twitch streamer code an Express API in 20 minutes!)*

1. What’s the relationship between REST and CRUD? 
REST and CRUD are related because REST uses HTTP methods to perform CRUD operations on data.

**Simple mapping:**
Create → POST
Read → GET
Update → PUT/PATCH
Delete → DELETE
**In short:** *REST is a style for building APIs, and CRUD is the basic way we interact with data. REST maps its methods to do CRUD actions.*

2. If you had to describe the process of creating a RESTful API in 5 steps, what would they be?
**STEP 1:** Plan your data
 – Decide what resources (like users, posts, products) your API will manage.

**STEP 2:** Set up your server
 – Use a backend framework (like Express for Node.js) to handle requests.

**STEP 3:** Create endpoints
 – Set up routes like GET /users, POST /users, PUT /users/:id, etc.

**STEP 4:** Connect to a database
 – Store and retrieve data using something like MongoDB or PostgreSQL.

**STEP 5:** Test your API
 – Use tools like Postman or curl to make sure each endpoint works as expected.



