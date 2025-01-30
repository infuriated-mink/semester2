# Week 1 - Introduction to JavaScript: Variables and Loops

## Overview

In this lesson, we'll learn about JavaScript variables, loops, and basic operations. These are the building blocks of programming, helping us store information, repeat tasks, and make decisions. Understanding these concepts is essential for web development, as they are used in features like dynamic content updates, user interactions, and data processing.

## 1. Variables in JavaScript

A variable is like a labeled storage box where we keep information. We can store different types of values in variables, like numbers, text, or even lists of data.

### Example: Storing a User's Information for a Website Profile

```javascript
let username = "Alice";
let userAge = 25;
console.log("User: " + username);
console.log("Age: " + userAge);
```

### Explanation:

1. `let username = "Alice";` 
   - This line creates a variable named `username`.
   - It assigns the text value "Alice" to this variable.
   - The `let` keyword is used to declare the variable.

2. `let userAge = 25;` 
   - Similarly, this creates a variable named `userAge`.
   - It assigns the numeric value 25 to this variable.

3. `console.log("User: " + username);` 
   - This line prints to the console.
   - It combines the string "User: " with the value stored in the `username` variable.
   - The `+` operator is used for string concatenation.

4. `console.log("Age: " + userAge);` 
   - This also prints to the console.
   - It combines "Age: " with the value in the `userAge` variable.
   - Note that JavaScript automatically converts the number to a string for concatenation.

💡 **Real-World Use Case:** This code snippet demonstrates how you might store and display user details on a website profile page.

## 2. Using Loops

A loop allows us to repeat a task multiple times without writing the same code over and over. It continues until a specified condition is met.

### Example: Displaying Product Listings on a Webpage

```javascript
for (let i = 1; i <= 5; i++) {
    console.log("Product " + i + " is available");
}
```

### Explanation:

1. `for (let i = 1; i <= 5; i++) {`
   - This is a `for` loop declaration.
   - `let i = 1;` initializes a counter variable `i` with the value 1.
   - `i <= 5;` is the condition: the loop continues as long as `i` is less than or equal to 5.
   - `i++` is the increment: after each iteration, `i` increases by 1.

2. Inside the loop: `console.log("Product " + i + " is available");`
   - This line executes for each iteration of the loop.
   - It prints a message to the console, incorporating the current value of `i`.
   - As `i` changes from 1 to 5, it creates five different product messages.

#### Output:

```
Product 1 is available
Product 2 is available
Product 3 is available
Product 4 is available
Product 5 is available
```

💡 **Real-World Use Case:** This loop could be used to dynamically display a list of products on an e-commerce website, where each product has a unique number.

## 3. While Loop Example

A while loop keeps running as long as its condition remains true. It's useful when you don't know in advance how many times the loop should run.

### Example: Checking for New Messages on a Website

```javascript
let newMessages = 3;
while (newMessages > 0) {
    console.log("You have " + newMessages + " new messages.");
    newMessages--;
}
```

### Explanation:

1. `let newMessages = 3;`
   - Initializes a variable `newMessages` with the value 3.
   - This represents starting with 3 unread messages.

2. `while (newMessages > 0) {`
   - This starts a while loop.
   - The loop will continue as long as `newMessages` is greater than 0.

3. Inside the loop:
   - `console.log("You have " + newMessages + " new messages.");`
     - This line prints the current number of new messages.
   - `newMessages--;`
     - This decrements `newMessages` by 1 after each iteration.
     - It simulates reading or removing a message.

#### Output:

```
You have 3 new messages.
You have 2 new messages.
You have 1 new message.
```

💡 **Real-World Use Case:** This type of loop could be used in a chat application to update and display the count of unread messages, reducing the count as messages are viewed.

## 4. Using Conditional Statements with Loops

We can combine loops with conditions to make decisions during each iteration of the loop.

### Example: Checking for VIP Users on a Website

```javascript
let users = ["Alice", "Bob", "Charlie", "David", "Eve"];
for (let i = 0; i < users.length; i++) {
    if (users[i] === "Charlie") {
        console.log(users[i] + " is a VIP user!");
    } else {
        console.log(users[i] + " is a regular user.");
    }
}
```

### Explanation:

1. `let users = ["Alice", "Bob", "Charlie", "David", "Eve"];`
   - Creates an array `users` containing five names.

2. `for (let i = 0; i < users.length; i++) {`
   - Starts a for loop that will iterate through each element in the `users` array.
   - `users.length` gives the number of elements in the array (5 in this case).

3. Inside the loop:
   - `if (users[i] === "Charlie") {`
     - Checks if the current user (accessed with `users[i]`) is "Charlie".
   - If true: `console.log(users[i] + " is a VIP user!");`
     - Prints a VIP user message.
   - If false: `console.log(users[i] + " is a regular user.");`
     - Prints a regular user message.

#### Output:

```
Alice is a regular user.
Bob is a regular user.
Charlie is a VIP user!
David is a regular user.
Eve is a regular user.
```

💡 **Real-World Use Case:** This code could be used on a membership website to identify and highlight VIP users, giving them special treatment or access to exclusive features.

## 5. Summing Numbers in a Loop

Loops are excellent for performing repetitive calculations, such as summing a series of numbers.

### Example: Calculating the Total Price of Items in a Shopping Cart

```javascript
let prices = [10, 20, 15, 5, 30];
let total = 0;
for (let i = 0; i < prices.length; i++) {
    total += prices[i];
}
console.log("Total Price: $" + total);
```

### Explanation:

1. `let prices = [10, 20, 15, 5, 30];`
   - Creates an array `prices` containing five different prices.

2. `let total = 0;`
   - Initializes a variable `total` to store the sum, starting at 0.

3. `for (let i = 0; i < prices.length; i++) {`
   - Starts a for loop that will iterate through each price in the array.

4. Inside the loop:
   - `total += prices[i];`
     - Adds the current price (`prices[i]`) to the `total`.
     - `+=` is a shorthand for `total = total + prices[i]`.

5. After the loop:
   - `console.log("Total Price: $" + total);`
     - Prints the final total price.

#### Output:

```
Total Price: $80
```

💡 **Real-World Use Case:** This code demonstrates how you might calculate the total cost of items in an online shopping cart, summing up individual item prices to get the total.

## Final Thoughts

- **Variables** are essential for storing and manipulating data in your programs.
- **Loops** provide an efficient way to repeat actions or process collections of data.
- **Conditions** within loops allow for more complex logic and decision-making in your code.

## Practice Questions

### Easy

1. Create a variable called `myName` and assign it your name. Then print it to the console.

2. Write a for loop that prints the numbers 1 to 5.

3. Create a variable called `count` with an initial value of 0. Use a while loop to increment it to 5, printing its value each time.

### Medium

4. Create an array of 5 fruits. Use a for loop to print each fruit to the console.

5. Write a loop that prints all even numbers from 0 to 10.

6. Create a variable called `password` with the value "secret123". Write an if statement that checks if the password is correct and prints "Access granted" if it is, and "Access denied" if it's not.

### Hard

7. Write a loop that calculates the sum of all numbers from 1 to 100.

8. Create an array of numbers. Write a loop that finds the largest number in the array.

9. Write a nested loop that creates a multiplication table for numbers 1 through 5.

### Expert

10. Write a function that takes a number as input and returns true if it's a prime number, and false if it's not. Then use this function in a loop to print all prime numbers between 1 and 50.

