# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user inputs.  Specifically, this example shows a route that retrieves a user by ID but fails to handle cases where the ID is not a valid number.

The `bug.js` file contains the erroneous code. The `bugSolution.js` provides a corrected version with robust error handling.

## Bug

The primary issue is the lack of error handling around `parseInt(userId)`. If `userId` is not a number (e.g., a string or null), `parseInt` will return `NaN`, leading to incorrect results or application crashes.  The code should explicitly check for and handle such scenarios.

## Solution

The solution involves adding checks to ensure that `userId` is a valid number before attempting to find the user.  The improved code includes error handling for invalid input, returning appropriate error responses to the client.