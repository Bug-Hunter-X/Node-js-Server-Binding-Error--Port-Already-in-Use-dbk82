# Node.js Server Binding Error: Port Already in Use

This repository demonstrates a common error in Node.js: attempting to bind a server to a port that is already in use.  The `bug.js` file contains the erroneous code, while `bugSolution.js` provides a solution.

## Problem

The `bug.js` file creates an HTTP server and attempts to listen on port 8080. If another process (e.g., another Node.js server or a different application) is already using this port, the server will fail to start and throw an `ERR_SERVER_ALREADY_LISTEN` error.

## Solution

The `bugSolution.js` file addresses this issue by implementing error handling.  It attempts to bind to the port, and if the binding fails, it gracefully handles the error, potentially retrying after a delay or informing the user of the issue.  This prevents the application from crashing and provides a more robust solution.