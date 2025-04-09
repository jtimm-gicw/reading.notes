# 301-Read_09

## Questions
### Functional Programming Concepts
1. What is functional programming? 
Functional programming is a programming paradigm based on the idea of building software by composing pure functions and avoiding shared state, mutable data, and side effects. It treats computation as the evaluation of mathematical functions.
2. What is a pure function and how do we know if something is a pure function?
*Pure Functions*
A pure function always produces the same output for the same input and doesn’t modify anything outside its scope.
- Immutability
- First-Class and Higher-Order Functions
- Avoiding Side Effects
- Function Composition

3. What are the benefits of a pure function?
Pure functions come with several powerful benefits that make code easier to understand, test, and maintain. 
- Predictability / Reliability
- Easy to Test
- Reusability
- Easier to Understand
- Makes Debugging Simpler
- Supports Concurrency and Parallelism
- Great for Functional Composition

4. What is immutability?
Immutability means that once a value is created, it cannot be changed. Instead of modifying the original data, you create and use a new copy with the updated data.

5. What is Referential transparency?
Referential transparency is a core concept in functional programming. *It means:*
- An expression can be replaced with its value without changing the program's behavior.

* If a function is referentially transparent, calling it with the same arguments will always give the same result, and you can swap the call for its result anywhere in the code without breaking anything.

### Videos
*Node JS Tutorial for Beginners #6 - Modules and require()*
1. What is a module? 
JS file.
2. What does the word ‘require’ do? 
Global object on node.js. *require(‘./’)* to say we want a file in the current directory, then the file name like *require(‘./count.js’)*. It automatically finds that js file. 
3. How do we bring another module into the file that we are working in? 
Use the `require()` on the file you want to use it(the function or whatever) on and module.export = fileName
4. What do we have to do to make a module available?  
Whatever we want to be made available outside the module(js file) we use `module.export` = functionName(or const or whatever) to allow it to be used in another js file.  Then, we use the `require()` with the file name that you want to use that piece of code, function, variable, etc.



