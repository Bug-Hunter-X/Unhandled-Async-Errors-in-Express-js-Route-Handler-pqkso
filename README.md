# Unhandled Async Errors in Express.js Route Handler

This repository demonstrates a common error in Express.js applications where asynchronous operations within route handlers are not properly handled, leading to silent failures.  The server might continue running but fail to respond to requests if an error occurs within an asynchronous function. 

The `bug.js` file shows the problematic code. The `bugSolution.js` provides the corrected implementation.

## Problem

The original code uses `.then()` and `.catch()` to handle an asynchronous operation but only logs the error to the console instead of sending an appropriate error response to the client.