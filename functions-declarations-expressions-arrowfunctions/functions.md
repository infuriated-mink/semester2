# Week 2 – JavaScript Functions: Declarations, Expressions, and Arrow Functions

## Function Declarations

Function declarations are a fundamental way to define reusable blocks of code in JavaScript.

### Example:

```javascript
function greet(name) {
    return "Hello, " + name + "!";
}

console.log(greet("Alice")); // Output: Hello, Alice!
```

### Explanation:

1. `function greet(name) {`: 
   - Declares a function named `greet` that takes one parameter `name`.
   - The `function` keyword is used to start the declaration.

2. `return "Hello, " + name + "!";`:
   - Constructs a greeting message using the provided `name`.
   - The `+` operator is used for string concatenation.
   - `return` sends this greeting back when the function is called.

3. `console.log(greet("Alice"));`:
   - Calls the `greet` function with the argument "Alice".
   - The returned greeting is then printed to the console.

Function declarations are hoisted, meaning they can be called before they are defined in the code.

## Function Expressions

Function expressions define functions as part of a larger expression, typically by assigning them to variables.

### Example:

```javascript
const multiply = function(a, b) {
    return a * b;
};

console.log(multiply(4, 5)); // Output: 20
```

### Explanation:

1. `const multiply = function(a, b) {`:
   - Creates an anonymous function and assigns it to the variable `multiply`.
   - `const` ensures the function reference can't be reassigned.

2. `return a * b;`:
   - Multiplies the two parameters and returns the result.

3. `console.log(multiply(4, 5));`:
   - Calls the function stored in `multiply` with arguments 4 and 5.
   - The result (20) is then printed to the console.

Function expressions are not hoisted, so they must be defined before they can be used.

## Arrow Functions

Arrow functions provide a concise syntax for writing function expressions, introduced in ES6.

### Example:

```javascript
const square = (x) => x * x;

console.log(square(6)); // Output: 36
```

### Explanation:

1. `const square = (x) => x * x;`:
   - Defines an arrow function that takes one parameter `x`.
   - The function body `x * x` is implicitly returned because it's a single expression.
   - No need for `function` keyword, `return` statement, or curly braces.

2. `console.log(square(6));`:
   - Calls the arrow function with argument 6.
   - The result (36) is printed to the console.

Arrow functions are particularly useful for short, simple functions and have a lexical `this` binding.

## Practice Questions

### Easy

1. Write a function declaration called `addFive` that takes a number and returns that number plus 5.

2. Create a function expression named `isEven` that returns true if a number is even, and false otherwise.

3. Write an arrow function called `double` that takes a number and returns it multiplied by 2.

### Medium

4. Write a function `calculateBMI` that takes weight (in kg) and height (in meters) and returns the BMI rounded to one decimal place.

5. Create an arrow function `reverseString` that takes a string and returns its reverse.

6. Write a function expression `isPalindrome` that checks if a given string is a palindrome (reads the same forwards and backwards, ignoring spaces and capitalization).

### Hard

7. Create a function `fibonacci` that returns the nth number in the Fibonacci sequence.

8. Write an arrow function `sortByProperty` that takes an array of objects and a property name, and returns a new array sorted by that property.

9. Create a function expression `debounce` that takes a function and a delay time, and returns a new function that can only be executed once per that time period.

### Expert

10. Implement a function `curry` that takes a function as an argument and returns a curried version of that function. The curried function should accept arguments one at a time, and return a new function for each argument until all arguments are supplied, at which point it should return the result.
