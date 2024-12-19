# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js applications: unhandled promise rejections.  The `bug.js` file shows an HTTP server that performs an asynchronous operation.  If the operation fails, the error is logged to the console, but the promise rejection is not handled, potentially leading to application instability. The `bugSolution.js` file shows the correct way to handle this situation.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node bug.js`.
4. Refresh the page multiple times until the server crashes. You should see the following error message:
    `UnhandledPromiseRejectionWarning: Error: Something went wrong!`

## Solution

The solution is provided in `bugSolution.js`.  It demonstrates the proper way to handle promise rejections using `.catch()` block within an asynchronous function and adding an unhandledRejection event listener in order to handle uncaught promise rejections. 
