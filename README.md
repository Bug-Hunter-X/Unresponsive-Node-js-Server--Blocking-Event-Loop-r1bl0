# Unresponsive Node.js Server: Blocking Event Loop

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, making the server unresponsive. The `server.js` file contains the buggy code, while `serverSolution.js` provides a solution using asynchronous operations.

## Bug Description
The server uses a `while` loop to simulate a 5-second delay. During this time, the event loop is blocked, and no other requests can be processed.  This leads to unresponsiveness and poor performance.

## Solution
The solution involves using asynchronous operations to avoid blocking the event loop.  Asynchronous operations allow other tasks to continue while the long-running task is in progress.