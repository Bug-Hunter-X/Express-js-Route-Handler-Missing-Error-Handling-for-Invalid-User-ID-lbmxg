# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the code lacks checks to ensure that the user ID passed in the route parameters is a valid number.  This can lead to unexpected behavior or application crashes.

## Bug Description
The provided `bug.js` file contains an Express.js route handler that fetches a user based on their ID. However, it fails to handle cases where the `userId` is not a number. This can occur if a non-numeric value is passed as the ID in the URL.

## Solution
The `bugSolution.js` file shows the corrected code, which includes proper error handling. It checks whether the `userId` can be parsed as an integer before attempting to find the user. If the parsing fails, a corresponding error response is sent back to the client. This approach ensures that the application handles invalid inputs gracefully without crashing.