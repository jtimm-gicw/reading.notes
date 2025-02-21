# 301-Read_02

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

2. List 4 things that the spread operator can do.

3. Give an example of using the spread operator to combine two arrays.

4. Give an example of using the spread operator to add a new item to an array.

5. Give an example of using the spread operator to combine two objects into one.