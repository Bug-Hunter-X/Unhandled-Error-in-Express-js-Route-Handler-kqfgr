# Unhandled Error in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers:  failure to handle invalid input or missing resources gracefully.

The `bug.js` file contains the problematic code.  The `bugSolution.js` file provides a corrected version with improved error handling.

## Bug

The original code attempts to fetch a user from an array based on a user ID passed as a route parameter.  However, it lacks proper error handling for cases where:

1. The `userId` parameter is not a valid number.
2. No user with the given ID exists.

This leads to unhandled exceptions and unexpected application behavior.

## Solution

The solution adds checks to validate the `userId` and handle the case where a user is not found. It uses appropriate HTTP status codes (400 for bad request, 404 for not found) to communicate errors to the client.