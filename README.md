# Incorrect Content-Type Header in Node.js HTTP Response

This repository demonstrates a common error in Node.js HTTP servers where the `Content-Type` header is missing or incorrect, leading to client-side issues.  The bug showcases a server that sends a response without specifying the `Content-Type`, causing browsers to misinterpret the response.

## Bug

The `bug.js` file contains a simple Node.js HTTP server that sends a text response without setting the `Content-Type` header. This can lead to unexpected behavior on the client-side because the browser might not render the response correctly.

## Solution

The `bugSolution.js` file shows the corrected version of the server, where the `Content-Type` header is explicitly set to `text/plain` which appropriately tells the client that the response is plain text.

## How to reproduce

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `node bug.js`.
4. Open a browser and access `http://localhost:3000`. Observe the behavior.
5. Run `node bugSolution.js`.
6. Open a browser and access `http://localhost:3000` again. Compare the behaviour.