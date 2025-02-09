# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections.  Asynchronous operations within request handlers often lack proper error handling, potentially causing the application to fail silently or unexpectedly.

## Bug Description
The `bug.js` file showcases an Express.js application with an asynchronous function (`doSomethingAsync`) inside a route handler. This function simulates an operation that might throw an error.  However, the code lacks a `catch` block to handle potential errors, leading to an unhandled promise rejection.

## Solution
The `bugSolution.js` file presents a corrected version with proper error handling.  It uses a `catch` block to handle errors gracefully, preventing unhandled rejections and providing more robust error management.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install Express.js.
3. Run `node bug.js`. You'll likely see a process crash or no output depending on how your system is set up.
4. Run `node bugSolution.js`.  This version correctly handles the error.

This example highlights the importance of comprehensive error handling in asynchronous JavaScript code to ensure application stability.