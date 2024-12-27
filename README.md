# Express.js Route Handler Missing Error Handling
This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Bug
The `/users/:id` route attempts to find a user based on the provided ID.  However, it lacks proper error handling. If the ID is not a number or if no user with the matching ID exists, the code will throw an error.

## Solution
The solution involves adding checks to ensure the ID is a valid number and handling the case where no user is found using `res.status(404).send('User not found');`.