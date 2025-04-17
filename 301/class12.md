# 301-Read_12

## Questions
### Status Codes Based On REST Methods
1. In your own words, describe what each group of status code represents:
100’s = Hold on (informational codes)
200’s = Success
300’s = Redirect
400’s = Client error 
500’s = Server client

2. What is a status code 202?  
✅ “We got your request, and we’re working on it — but it’s not done yet.”

3. What is a status code 308? 
✅ Status Code 308 = "Go to a new place — permanently, and do it the same way."

4. What code would you use if an update didn’t return data to a client?  
If your update (like a PUT or PATCH request) was successful but you’re not returning any data to the client, the correct status code is:
✅ 204 No Content

5. What code would you use if a resource used to exist but no longer does?
**404 Not Found** = Maybe it was never here, or maybe it's temporarily gone.
**410 Gone** = It definitely was here, but has been permanently removed.

6. What is the ‘Forbidden’ status code?
🚫 403 Forbidden
"We know who you are — but you're not allowed to do this."

## Videos
### Build A REST API With Node.js, Express, & MongoDB - Quick - First 20 minutes
1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
We move our MongoDB connection string into a .env file because:
- security 
- flexibility
- cleaner code

2. What is middleware?
🧩 Middleware = Code that runs between the request and the response

Middleware is like a helper that steps in when a request comes to your server — it can check, change, or handle things before the final response is sent.
3. What does app.use(express.json()) do?
✅ app.use(express.json()) — in simple terms:
It tells your Express app to automatically read and parse JSON from incoming requests — so you can use the data easily in your code.

4. What does the /:id mean in a route?
The /:id in a route is a route parameter used in Express (and many other web frameworks) to capture dynamic values from the URL.

5. What is the difference between PUT and PATCH?
✅ PUT = Replace the entire resource
- PUT replaces all of the current data of a resource with the new data you send.
- If you don’t include a piece of data that was already there, it will be removed.
✅ PATCH = Update only part of the resource
- PATCH is used for making partial updates — just modifying the parts of the resource you send.
- It doesn't remove any data unless explicitly specified.

6. How do you make a default value in a schema?
To set a default value in a Mongoose schema, you can use the default property in the schema definition. This allows you to specify a value that will be used if no value is provided when creating a document.

7. What does a 500 error status code mean?
🚨 500 Internal Server Error = Something went wrong on the server.

8. What is the difference between a status 200 and a status 201?
✅ 200 OK = Request was successful
✅ 201 Created = Resource was successfully created


