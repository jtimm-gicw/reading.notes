# 201-Read_04

## HTML

1. **To create a basic link, we wrap text or other content inside what element?** `<a>` tag
2. **The href attribute contains what information?** The website address.
3. **What are some ways we can ensure links on our pages are accessible to all readers?** Contrasting colors, use descriptive link text.


## CSS

1. **What is meant by “normal flow”?**  *"Normal flow"* refers to the default way that elements are positioned on a webpage before any additional layout techniques like floating, positioning, or flexbox/grid are applied.
2. **What are a few differences between block-level and inline elements?**  
Block-level element: 
- Take up the full container width, stacking vertically.
- Allow width, height, margin, and padding on all sides.
- Used for large structural components (e.g., `<div>`, `<p>`, `<h1>`).
Inline Elements:
- Only take up as much space as their content, lining up horizontally.
- *width* and *height* can’t be set, and only horizontal margin/padding applies.
- Used for smaller content within text, like links or styled words (e.g., `<span>`, `<a>`).
3. Static positioning is the default for every html element.
4. Name a few advantages to using absolute positioning on an element.
- Precise Control: Allows exact placement of elements within a container.
- Independent of Flow: Positioned independently of surrounding elements, making it great for overlays.
- Layering: Works well with z-index for stacking order control.
- Responsive Design: Useful for UI components that need to adapt to different screen sizes.
- Custom Layouts: Ideal for complex layouts needing precise element arrangement.
5. What is a key difference between fixed positioning and absolute positioning?
- Fixed Positioning: Positions an element relative to the viewport, so it stays in the same place on the screen even when the page is scrolled. It’s unaffected by any parent elements.
- **Example use:** *Sticky navigation bars or floating action buttons.*
- Absolute Positioning: Positions an element relative to its nearest positioned ancestor (an ancestor with a position other than static). If no such ancestor exists, it positions relative to the viewport.
- **Example use:** *Tooltips or specific content placements within containers.*

## JS

1. Describe the difference between a function declaration and a function invocation.
- Function Declaration: This is when you create or define a function, giving it a name and specifying the code it will execute. The declaration itself doesn’t run the function; it just makes the function available for use.
`function greet() { console.log("Hello!"); }`
In this example, `greet` is a function declaration.
- Function Invocation: This is when you call or execute the function to run the code inside it. To invoke a function, you use its name followed by parentheses.
`greet();` // This runs the code in the greet function and outputs "Hello!"
2. What is the difference between a parameter and an argument?
The terms parameter and argument are often used interchangeably, but they refer to different concepts in the context of functions in programming:
- Parameter: A parameter is a variable in the function declaration or definition that acts as a placeholder for the value that will be passed to the function. Parameters specify what kind of data the function can accept.
`function add(a, b)` { // 'a' and 'b' are parameters 
`return a + b;` }
- Argument: An argument is the actual value that you pass to a function when you invoke it. Arguments are the real data that gets assigned to the parameters.
`let result = add(5, 10);` // 5 and 10 are arguments	
**Parameter:** The variable in the function definition (e.g., a and b in the add function).
**Argument:** The actual values passed to the function when called (e.g., 5 and 10 when calling add(5, 10)).

## MISC.

**Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey.**
*Roles:* There are two roles— *Driver* (the one typing) and *Navigator* (the one guiding the Driver and focusing on the bigger picture).
- *Learning from Peers:* I can learn from others who are learning and applying the same code as I am where I can get a different perspective than my own.
- *Greater Efficiency:* Anything that saves me time on cleaning up my code or debugging, I am for it.






