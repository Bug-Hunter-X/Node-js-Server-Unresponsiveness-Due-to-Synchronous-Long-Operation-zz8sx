# Node.js Server Unresponsiveness Bug

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can cause the server to hang or become unresponsive.  The `server.js` file contains the buggy code. The solution is provided in `serverSolution.js`.

## Problem

Node.js is single-threaded, and a long-running synchronous operation in the request handler blocks the event loop, preventing it from processing other requests or events. This leads to the server becoming unresponsive.

## Solution

The solution involves refactoring the long-running task to be asynchronous.  This allows the event loop to continue processing other requests while the long-running task executes in the background.