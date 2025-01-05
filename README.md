# Express.js JSON Body Parsing Error: req.body is undefined

This repository demonstrates a common error in Express.js applications where the request body (req.body) is undefined when attempting to parse JSON data. This often happens due to incorrect middleware configuration or missing middleware altogether.

## Bug

The `bug.js` file contains an Express.js application that attempts to parse JSON data from a POST request but fails due to a missing or incorrectly configured body-parser middleware.

## Solution

The `bugSolution.js` file demonstrates the corrected version, showcasing proper use of the built-in `express.json()` middleware to parse incoming JSON requests.

## How to Reproduce

1. Clone the repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `node bug.js`.
5. Send a POST request with JSON data to `http://localhost:3000/data` using a tool like Postman or curl.  Observe that `req.body` is undefined.
6. Run `node bugSolution.js`.
7. Send the same POST request.  This time, `req.body` will contain the parsed JSON data.

## Note

This example uses the built-in `express.json()` middleware.  Older versions of Express.js required separate body-parser middleware. Always ensure that the necessary middleware is correctly configured and included in your app's middleware stack.