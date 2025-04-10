# 301-Read_10

## Questions

1. What is a 'call'?
The *call stack* is a data structure used by the JavaScript engine to keep track of function calls (aka "execution context").
It works like a stack of plates — **Last In, First Out (LIFO)**:
*The last function that’s called is the first one to finish and get removed from the stack.*

**What is a “call” in this context?**
A *“call”* is simply the **execution of a function**. When a function is called:
* It's pushed onto the call stack.
* JavaScript executes it.
* Once done, it's popped off the stack. 

2. How many ‘calls’ can happen at once?
❗ Only ONE function call can happen at a time in the JavaScript call stack.

3. What does LIFO mean?
LIFO stands for Last In, First Out — it’s a way of organizing and accessing data, kind of like a stack of pancakes or plates.

4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
function one() {
  two();
}
function two() {
  three();
}
function three() {
  console.log("Hello from three!");
}
one();

The Call Stack at the moment console.log runs:
|--------------------|
| console.log        | 👈 Last in
|--------------------|
| three              |
|--------------------|
| two                |
|--------------------|
| one                | 👈 First in
|--------------------|
(main/global context)

This shows the Last In, First Out structure.
The global context is always there.
**Each function that gets called goes on top.**
**As functions complete, they’re removed from the top.**

5. What causes a Stack Overflow?
A stack overflow happens when the call stack gets too full — in other words, too many function calls get stacked up, and JavaScript runs out of space to keep track of them.
🧱 Think of it like this:
Imagine stacking plates in a tower. If you keep stacking without ever taking any off, eventually the stack gets too tall and…
💥 BOOM! It topples over — that’s a stack overflow.

### Javascript Errors
1. What is a ‘reference error’?
A ReferenceError happens when you try to use a variable or function that hasn’t been defined.

2. What is a ‘syntax error’?
A SyntaxError happens when you write code that breaks the rules of the language — kind of like making a grammar mistake when writing a sentence.
🧠 JavaScript reads your code and says:
 “I don’t understand this — it’s not valid JavaScript.”

3. What is a ‘range error’?
A RangeError happens when a number or value is outside the allowed range for a function or operation.
🧠 JavaScript is saying:
 “That value is technically the right type, but it’s too big, too small, or just not allowed here.”

4. What is a ‘type error’?
A TypeError happens when you try to do something with a value that isn’t allowed for its type.
🧠 JavaScript is basically saying:
 “Hey! That value exists, but you're trying to use it in the wrong way.”

 5. What is a breakpoint?
A breakpoint is a tool used while debugging code — it tells the browser:
“⏸️ Pause here! Let me take a look before this next line runs.”

🔍 Why use it?
Breakpoints let you:
- Pause the code mid-run
- Inspect variables and values
- See what the code is doing step by step
- Find bugs more easily

6. What does the word ‘debugger’ do in your code?
The debugger statement is a built-in tool in JavaScript that tells the browser:
🛑 “Pause execution here like a breakpoint — even if no breakpoint is set.”

⚠️ **Important:**
If DevTools aren’t open, the debugger line is just ignored — it won’t break anything.




