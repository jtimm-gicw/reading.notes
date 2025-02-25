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
