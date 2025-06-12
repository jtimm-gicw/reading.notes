# 401-Read_02

## Questions

### An introduction to NodeJS and Express

1. Explain middleware, answer as though I were a non-technical recruiter.
Imagine a restaurant.
The customer (like a user) places an order.
The kitchen (like the server or app logic) prepares the food.
But in between, there's a waiter—this is your middleware.
*The waiter (middleware):*
Takes the order (user request)
Checks if the order is clear or valid (like checking if the user is logged in)
Maybe adds something extra to the order (like extra information or tracking)
Then brings it to the kitchen (the main app or server)

In software, middleware is code that sits between the user’s request and the final result. It helps handle things like:

- Security (Is this user allowed to do this?)
- Logging (Keep track of what’s happening)
- Data formatting (Clean or prepare the data)
- It keeps the core system cleaner and more organized, while still making sure important checks and tasks happen behind the scenes.

**So when a developer talks about using "middleware," think of it as a smart assistant that helps handle requests before the main system does the heavy lifting.**

2. Express the most popular **Node.js web framework**.

3. Express is “unopinionated.” What does that mean?
*When we say Express is "unopinionated," we mean:*
Express doesn’t force developers to follow one strict way of building an app.
🧱 Imagine building a house:
An opinionated tool gives you a blueprint and says:
*“Here’s where the kitchen goes, here’s the only way to do plumbing, and you must use this kind of window.”*

An unopinionated tool like Express says:
*“Here are the materials and tools—you decide how you want to build it.”*

In technical terms:

- Express gives developers freedom and flexibility.
- You can organize your project however you want.
- You can choose your own tools for things like databases, file structure, or user authentication.

4. What is a module and why is modularity useful to us as developers?
*Keeps things organized*
 Just like separate drawers keep your kitchen tidy, modules keep code clean and easier to understand.


*Makes code easier to reuse*
 If you build a module to do one job well, you can use it again in different projects or parts of the app without rewriting it.


*Simplifies debugging and updates*
 When something breaks, you only need to look inside the specific module responsible, not the entire codebase.
 Also, you can update one module without messing up the rest of the app.


*Helps teams work together*
 Different developers can work on different modules at the same time without stepping on each other’s toes.

### What is NPM?

1. What version of npm are you running on your machine?
v22.13.1

2. What command would you type to install a library/package called ‘jshint’ into your node project?
npm install jshint
* npm is Node’s package manager (like an app store for code libraries).
* install tells it to add a package.
* jshint is the name of the package (used to check JavaScript code for errors).

### What is TDD?

1. Explain why tests are important. Please explain as though I were your non technical elder.
Why tests are important:
**🛑 Catch mistakes early:**
Just like noticing you forgot the sugar before handing out cookies, tests help developers find errors in the code before users ever see them.

**🔄 Make changes safely:**
If you change the recipe a little (maybe add chocolate chips), you still taste it to be sure it didn’t ruin the batch.
Tests help developers safely update or improve code without accidentally breaking something else.

**✅ Give confidence:**
If all the tests pass, we know the software works the way it’s supposed to.
It gives peace of mind—like knowing your cookies always come out delicious.

2. What are three expected benefits of testing?
I. Catch Problems Early
Testing helps developers find bugs or mistakes in the code before the app goes live.
✅ Better to fix it now than have users run into problems later!

II. Make Future Changes with Confidence
When code is tested, developers can safely update or improve things without breaking something else by accident.
🔧 It’s like knowing you can remodel the kitchen without the roof falling in.

III. Save Time and Money
Fixing problems after something is live is more expensive and time-consuming.
🕒💰 Testing helps prevent big issues, which saves resources in the long run.

3. Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.
🧍‍♂️ Individual Pitfalls
1. Writing tests that are too tightly coupled to the code
- If the test is too dependent on the exact details of how the code works (instead of what the code is supposed to do), then even small changes can break the test unnecessarily.
- 🔄 This leads to lots of re-writing tests even when the feature still works fine.

2. Not testing edge cases
- A developer might only test the “happy path” (when everything works perfectly) and forget to test unusual or unexpected situations.
⚠️ This means bugs can sneak through when users do something unexpected.

👥 Team Pitfalls
1. Inconsistent testing practices
- If everyone on the team writes tests differently—or some don’t write them at all—it leads to messy, unreliable testing.
- 📉 This hurts team productivity and makes collaboration harder.

2. Relying too much on manual testing
- Some teams may skip writing automated tests and just test things by hand.
- ⏳ This slows down development and increases the chance of human error.

## CI/CD

1. What are three benefits of Continuous Integration?
    1. ✅ Catch Problems Early
CI automatically runs tests every time code is added or changed.
This means bugs are caught right away, not weeks later.
🛠️ Fixing small problems early is faster and cheaper.

    2. 🔄 Faster, Smoother Collaboration
When multiple developers work on the same project, CI helps make sure their code works together without breaking anything.
🤝 It’s like making sure all the puzzle pieces still fit as new ones are added.

    3. 🚀 Faster Delivery of Features
CI makes it easier and safer to release new updates frequently.
This means users get new features and fixes sooner.
⚡ Less waiting, more progress.

2. What is the difference between Continuos Delivery and Continuous Deployment?
**🚛 Continuous Delivery (CD):**
Code is automatically tested and prepared to go live.
But the release still requires a human decision to actually launch it.

*🧠 Think of it like a package being ready at your door—you just have to choose when to open it.*

**🚀 Continuous Deployment:**
Code is automatically tested AND automatically released to users without human approval.
Every change that passes tests goes live immediately.

*⚙️ It's like the package is delivered and automatically unboxed and set up for you.*


3. Explain how GitHub fits into this process assuming the listener comes from a non-technical background
**Imagine a shared online workspace for a team working on a project:**
- GitHub is like a central filing cabinet on the internet where everyone on a software team stores their work (the code).
- Each team member can add their changes, save their updates, and see what others have done, all in one safe place.

**How GitHub fits into Continuous Integration and Deployment:**
- When a developer finishes a piece of work, they upload their changes to GitHub.
- This upload triggers automatic checks (like tests) to make sure nothing is broken.
- If everything looks good, the changes can then be automatically or manually sent out to users.

**So, GitHub is like:**
- The hub where all work is saved and shared.
- The starting point that kicks off automatic testing and delivery.
- A collaboration tool that helps the team work together smoothly, avoiding mistakes or lost work.



