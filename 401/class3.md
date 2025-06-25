# 401-Read_03

## Questions

### Review: ES6 Classes

1. Classes are a template for creating **objects**.
2. Can a class declaration be hoisted?
No, class declarations are not hoisted like function declarations.
If you try to use a class before it is declared, you'll get a ReferenceError

3. How would you describe a constructor and contextual “this” to a non-technical friend?
Think of a constructor like a blueprint's “setup team” — it’s a special function inside a class that gets called automatically when you create something new from that class. It's like the part of a toy factory that says:
*"Okay, every time we make a new toy robot, give it two arms, two legs, and a name."*
So when you create a new robot, the constructor sets it up with everything it needs right from the start.

### Using Express Routing

1. Within Express, what does routing refer to?
In Express, routing refers to how your server responds to different HTTP requests (like GET, POST, PUT, DELETE) at specific URLs (or "routes").

2. What is the difference between a route path and a route method?
In Express, the difference between a route path and a route method is like the difference between:
*Where the request is going (path)*
*How the request is being made (method)*
**Route Path = URL Address**
**Route Method = HTTP Verb**

3. When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?
✅ When is it appropriate to add next as a parameter?
You add next as a parameter when you're writing:
Middleware functions that might pass control to the next function in the stack, or
*Route handlers that want to:*
- Pass errors to error-handling middleware, or
- Move on to the next matching route or middleware.

### Express Routing

1. What is an Express Router?
An Express Router is like a mini Express app used to organize your routes into separate files or sections — especially useful in larger applications.
**Express Router helps you break up your route logic into modular, manageable chunks.**

2. By what mean do we initialize express.Router() in an express server?
We initialize express.Router() in an Express server by requiring Express and then calling express.Router() to create a new router instance.

3. What do we use route middleware for?
We use route middleware in Express to add extra functionality or perform checks before the route handler runs.
*Route middleware is like a security checkpoint or pre-flight checklist — it can allow, block, modify, or log a request before the main route does its job.*

### Reflection

1. What are your learning goals after reading and reviewing the class README?
After reading the class README I feel I want to make cleaner routes in the backend and get more practice with CRUD.
