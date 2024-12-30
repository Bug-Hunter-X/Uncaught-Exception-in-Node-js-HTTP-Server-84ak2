# Uncaught Exception in Node.js HTTP Server

This repository demonstrates a common error in Node.js: improper error handling in an HTTP server.  Unhandled exceptions can lead to server crashes, data loss, and degraded user experience.  The solution showcases best practices for handling errors gracefully.

## Bug

The `bug.js` file contains a Node.js HTTP server that throws an uncaught exception when the `/error` route is accessed. This causes the server to terminate abruptly without proper cleanup or notification.

## Solution

The `bugSolution.js` file presents an improved version of the server.  It uses a `try...catch` block to handle the potential exception, ensuring the server remains operational even in the face of errors.  It also logs the error for debugging purposes and sends a meaningful error response to the client.