# 201-Read_03

## **HTML:**
1. When should you use an unordered list in your HTML document? When the sequence or position is not important
2. How do you change the bullet style of unordered list items? In CSS use the list-style-type to change the shape to square, disc, circle, etc. ex: list-style-type: square;
3. When should you use an ordered list vs an unorder list in your HTML document? Use an ordered list when the order or sequence of items matters and unordered when all items are of equal importance.
4. Describe two ways you can change the numbers on list items provided by an ordered list? There are several ways to do this.  
- Using the type Attribute. ex:`<ol type="A">` <!-- Capital letters →
- Using the start Attribute. ex:`<ol start="5">` <!-- Starts numbering at 5 -->

## **CSS:**
1. When should you use an unordered list in your HTML document? When the sequence or position is not important
2. How do you change the bullet style of unordered list items? In CSS use the list-style-type to change the shape to square, disc, circle, etc. ex: list-style-type: square;
3. When should you use an ordered list vs an unorder list in your HTML document? Use an ordered list when the order or sequence of items matters and unordered when all items are of equal importance.
4. Describe two ways you can change the numbers on list items provided by an ordered list? There are several ways to do this.  
- Using the type Attribute. ex:<ol type="A"> <!-- Capital letters →
- Using the start Attribute. ex:<ol start="5"> <!-- Starts numbering at 5 -->
5. List and describe the four parts of an HTML elements box as referred to by the box model.
- *Content*: The core part, where the text or images live.
- *Padding*: Space inside the border, around the content.
- *Border*: The visible edge surrounding padding and content.
- *Margin*: Space outside the border, separating the element from others.

## **JS**
1. What data types can you store inside of an Array? An array can store any data type, making it a versatile structure.
- Primitive data types: numbers, arrays, strings, booleans, null, & undefined
- Reference data types: arrays, functions, dates, objects
2. Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why? Yes, the code creates a valid JavaScript array called people. This array contains nested arrays, meaning each item in people is its own array with separate values.
3. List five shorthand operators for assignment in javascript and describe what they do.
- += (Addition Assignment)
Adds the right value to the left variable and assigns the result to the left variable.
- -= (Subtraction Assignment)
Subtracts the right value from the left variable and assigns the result to the left variable.
- *= (Multiplication Assignment)
Multiplies the left variable by the right value and assigns the result to the left variable.
- /= (Division Assignment)
Divides the left variable by the right value and assigns the result to the left variable.
- %= (Remainder Assignment)
Divides the left variable by the right value, takes the remainder, and assigns it to the left variable.
4. Read the code below and evaluate the last expression and explain what the result would be and why.
- Evaluate (a + c):
a is 10 (a number).
c is false (a boolean).
In JS, *false is converted to 0 when used in a numeric context*.
So, 10 + 0 equals 10.
- Evaluate 10 + b:
b is 'dog' (a string).
When a number (10) is added to a string ('dog'), JavaScript converts the number to a string and then concatenates.
Therefore, 10 + 'dog' becomes **'10dog'**.
5. Describe a real world example of when a conditional statement should be used in a JavaScript program. 
Let’s say you have a program that checks if a store is open based on the current hour. The store is open from 9 AM to 5 PM, and you want to show a message telling customers if it’s open or closed.




