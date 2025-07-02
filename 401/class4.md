# 401-Read_04

## Questions
### nosql vs sql

1. What type of database is the best fit for the complex query intensive environment?
If you're working in an environment where you need to ask a lot of complicated questions about your data — like finding patterns, combining data from different places, or analyzing lots of details — then a relational database is usually the best fit.

2. What type of database is the best fit for hierarchical data storage?
For storing hierarchical data (data with parent-child relationships, like a family tree or a folder system), the best fit is usually a:
✅ Graph Database or Document Database, depending on the use case.
    I. **Graph Database (like Neo4j)**
    II. **Document Database (like MongoDB)**

3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.
**Imagine you're running a small coffee shop.**
At first, you just have one cash register. That’s fine when business is slow — everything is organized, and you can keep track of all the orders and customers easily. That’s like a *SQL database: very organized and great at handling structured data*.
But as your shop grows and gets more customers, that one register gets overwhelmed. To handle more people, you'd need to upgrade that register to be faster and stronger. That’s called scaling up — and that’s how SQL databases usually grow. But there’s a limit to how powerful one register (or one computer) can get.

**Now imagine a NoSQL approach.**
Instead of upgrading one cash register, you add more registers and more workers, spreading the load across many people. That’s called scaling out, and it’s what NoSQL databases do really well. They’re designed to handle tons of data across many machines at once, which is great if your app or website grows quickly.

### sql modeling techniques

1. Among data tables, what is a one-to-many relationship and how do we “relate” them?
**What is a one-to-many relationship in data tables?**
Imagine you have two tables:
One for Teachers
One for Students

Each teacher can have many students, but each student has only one teacher.
That’s a one-to-many relationship — one teacher → many students.

**How do we “relate” them?**
We connect the two tables using something called a foreign key.
The Teachers table has a unique ID for each teacher (called a primary key).

The Students table has a column called teacher_id — this is the foreign key that stores the ID of the teacher that student belongs to.

2. Prior to designing your relational database, it might be useful to **create a diagram** of the database tables and their relationships.
3. Explain the difference between a primary and foreign key.
🔑 Primary Key vs. Foreign Key
✅ **Primary Key**
A *primary key* is a column in a table that uniquely identifies each row.
- It must be unique and cannot be empty.
- Each table has one primary key.
🧠 Think of it like a Social Security Number — no two people have the same one, and everyone must have one.

**Foreign Key**
A *foreign key* is a column in one table that refers to the primary key in another table.
- It’s used to link two related tables together.
- It helps enforce relationships between the data.
🧠 Think of it like writing a student's teacher ID in the student’s file to show who their teacher is.

## Videos
### sql vs nosql

1. How do we treat keywords and parameters differently in SQL syntax?
🔑 **Keywords**
These are reserved words in SQL.
- They tell the database what to do.
- Always written in UPPERCASE (by convention, though not required).
- You can’t change them or use them as names for tables or columns (unless quoted).
📦 **Parameters**
Parameters are values or placeholders that you pass into your SQL queries.
- They represent data you want to search for, insert, or update.
- In prepared statements, parameters are often represented by placeholders like ? or named variables like *:name*.

*Keywords* are like commands in a recipe: “Mix,” “Bake,” “Chop.”
*Parameters* are like ingredients: “2 eggs,” “1 cup sugar.”

2. Define normalization within the context of schemas and data.
**Normalization** is the process of organizing data in a database so that:
- It’s clean and efficient
- There’s no unnecessary repetition
- Data is stored in the right places

3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.
Imagine relationships between things like people and groups:
    1. One-to-One
    - Like a person and their passport.
    - Each person has only one passport, and each passport belongs to only one person.
    - It’s a one-to-one match.

    2. One-to-Many
    - Like a teacher and their students.
    - One teacher can have many students, but each student has only one teacher.
    - So, one on one side, many on the other.

    3. Many-to-Many
    - Like students and classes.
    - A student can take many classes, and each class can have many students.
    - So both sides have many connections.

* Why this matters in databases
Understanding these helps organize data properly so the system knows how things are connected. For example, making sure a student’s info and their classes are linked correctly.

