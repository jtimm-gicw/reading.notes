# 401-Read_08

## Questions

### 5 steps to RBAC

1. What is Role Based Access Control (RBAC) and why do we care?
Role-Based Access Control (RBAC) is a way to manage who can do what in a system based on their role—like a job title or position.
**RBAC helps because it:**
- Keeps systems secure – Only the right people can access sensitive data or actions.
- Makes permissions easier to manage – Instead of updating every individual, you update roles.
- Reduces mistakes – Limits users from accidentally (or maliciously) doing things they shouldn’t.

2. Describe a Role/Permission heirarchy that you might implement using RBAC.
🔒 **Roles and Their Permissions**
    1. Admin
💼 *Full control over everything in the system.*
Permissions:
- Manage users (create, delete, assign roles)
- Edit site settings
- Create, edit, delete content
- View analytics and logs

    2. Editor
📝 *Can manage and publish content, but not change system settings or manage users.*
Permissions:
- Create, edit, delete content
- Publish content
- View analytics

    3. Author
✍️ *Can write content, but can’t publish or edit others’ work.*
Permissions:
- Create and edit own content
- Submit content for review

    4. Viewer (or Reader)
👀 *Can only read published content.*
Permissions:
- View public content

3. What approach might you take to implement RBAC?
✅ 1. Define Roles and Permissions
Start by outlining the roles (Admin, Editor, User, etc.) and what each can do.
🗂 2. Store Roles and Permissions in the Database
🔐 3. Assign Roles to Users
⚙️ 4. Check Permissions Using Middleware
🔄 5. Load User Roles and Permissions at Login
🧪 6. Test and Maintain
🛠 Optional: Use a Library

💡 **TL;DR:**
Define roles & permissions clearly.
Store them in your DB.
Assign roles to users.
Check permissions with middleware.
Keep logic modular and maintainable.


### wiki - RBAC

1. If Authentication is “you are who you say you are,” what is Authorization?
✅ **Authentication:**
“You are who you say you are.”
 This is the process of verifying identity—usually through a username and password, or something like a token or fingerprint.

✅ **Authorization:**
“You can do what you're allowed to do.”
 This is the process of checking what you’re allowed to access or do after you’ve been authenticated.
👉 *Example:* Now that you're logged in:
Can you view the admin dashboard?
Can you delete another user’s post?
Can you change settings?

✔️ **Authorization decides what you’re allowed to do based on your role or permissions.**


2. Name three primary rules defined for RBAC.
    1. Role Assignment
🔑 A user must be assigned a role to access the system.
    2. Role Authorization
✅ A user can only take on roles for which they are authorized.
    3. Permission Authorization
🔒 A user can only perform an action if their assigned role has the required permission.

3. Describe RBAC to a non-technical friend.
🏢 Imagine an Office Building
In this office, people have different jobs—like receptionist, manager, and IT admin. Each job has its own responsibilities and access:
- The receptionist can greet guests and answer phones, but can’t enter the server room.
- The manager can approve time off and see team reports.
- The IT admin can access everything, including secure areas and computer systems.
- Instead of giving each person individual keys to everything they might need, the office just gives them a badge based on their job role. That badge controls where they can go and what they can do.


## Videos

### RBAC tutorial

1. What Are access rights Associated with? The User? or The Role? Explain.
🔐 Access rights are associated with the Role, not the User.
A **role** is like a **toolbox** that holds a set of permissions (access rights).
 The **user** doesn’t carry individual tools—they are just handed the toolbox.
So when you give a user a **role**, you're giving them all the **access rights** that come with that role.

2. Access Rights, or Authorization, is activated after a user successfully does what?
**Access Rights** (or *Authorization*) are activated after a user successfully authenticates — meaning:
👉 After the user proves who they are (usually by logging in with a username and password, or other method).

3. Explain how RBAC might benefit a business.
✅ 1. Improves Security
RBAC helps ensure that people only access what they need to do their jobs—no more, no less.
✅ 2. Simplifies User Management
Instead of setting up permissions for every individual employee, you just assign them a role (like "Manager" or "Sales Rep").
✅ 3. Supports Business Compliance
Many industries (like healthcare, finance, or government) have rules about who can access what. RBAC helps enforce those rules automatically.
✅ 4. Increases Productivity
Employees don’t waste time sifting through tools or information they don’t need. They get exactly what their role requires.
✅ 5. Scales with the Company
As your business grows, you can create new roles or adjust existing ones—without reworking permissions for hundreds of users.


#### Reflection
1. What are your learning goals after reading and reviewing the class README?
I am curious about the application control & access control.


