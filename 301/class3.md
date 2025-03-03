# 301-Read_03

## Questions 

1. What does .map() return?
.map() returns a new array where each element is transformed based on the function you provide. It does not change the original array.
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
In React, you can use *.map()* to loop through an array and display each value in JS
**Breakdown:**
*.map()* loops through items and returns an `<li>` for each value.
The key prop helps React track list items efficiently.
The component returns a `<ul>` containing the list items.
3. Each list item needs a unique **"key"**.

4. What is the purpose of a key?
The purpose of a key in React is to help React efficiently update and re-render lists by uniquely identifying each list item.

*Why is it important?*
- Improves Performance – Helps React quickly determine what has changed, added, or removed.
- Prevents Unnecessary Re-renders – Without a unique key, React may re-render the entire list instead of just the changed items.
- Maintains State – If components inside a list hold state, using stable keys ensures their state is preserved correctly.

### The Spread Operator

1. What is the spread operator?
The spread operator `(...)` in JavaScript is used to expand elements of an iterable (like an array or object) into individual elements. It’s a powerful tool for copying, merging, and manipulating data structures efficiently.
2. List 4 things that the spread operator can do.
    -Copy an array (Makes a duplicate of an array)
    -Merger arrays
    -Copy & update an object
    -Pass array elements as function arguments
3. Give an example of using the spread operator to combine two arrays.
`const firstArray = [1, 2, 3];`
`const secondArray = [4, 5, 6];`

`const combinedArray = [...firstArray, ...secondArray];`

`console.log(combinedArray); // Output: [1, 2, 3, 4, 5, 6]`
*How it Works:*
The `...firstArray` expands [1, 2, 3] into 1, 2, 3
The `...secondArray` expands [4, 5, 6] into 4, 5, 6
The new array `[...firstArray, ...secondArray]` combines all the elements into a single array.

4. Give an example of using the spread operator to add a new item to an array.
`const fruits = ["apple", "banana", "orange"];` // Adding a new item ("grape") at the end 
`const newFruits = [...fruits, "grape"]; console.log(newFruits);` // Output: `["apple", "banana", "orange", "grape"]`
**How It Works:**
`...fruits` spreads the existing array items.
"grape" is added at the end.
The result is a new array with the additional item.

5. Give an example of using the spread operator to combine two objects into one.
`const person = { name: "Alice", age: 25 };`
`const job = { title: "Developer", company: "Tech Corp" };`
`const combinedObject = { ...person, ...job };`

`console.log(combinedObject);`
// Output: `{ name: "Alice", age: 25, title: "Developer", company: "Tech Corp" }`
**How It Works:**
`...person` spreads the properties of person into the new object.
`...job` spreads the properties of job into the new object.
The result is a single object containing all the properties from both.

### Video
1. In the video, what is the first step that the developer does to pass functions between components? 
He creates a buttone to handle the delete button for the blog post with an empty function so that he can pass an arguement into a custom function.
2. In your own words, what does the `handleClick` function do? 
Usually used to respond when a user clicks on something, like a button. It is a common name for a function in JavaScript (especially in React) that gets triggered when a click event happens.
3. How can you pass a method from a parent component into a child component?
You can pass a method (function) from a parent component to a child component in React by using props.

**Steps:**
Define the method in the parent component.
Pass it as a prop to the child component.
Call the method inside the child component using props.
4. How does the child component invoke a method that was passed to it from a parent component?
The child component invokes a method passed from the parent component simply by calling it like a normal function using props.

**Steps:**
a. The parent component passes the function as a prop to the child.
b. The child component receives it as a prop.
c. The child calls the function when an event occurs (like a button click).