# React Router Wildcard Route Bug

This repository demonstrates a common issue in React Router v6 where a wildcard route (`path="*"`) placed before more specific routes prevents those specific routes from ever being matched.  The solution shows how to correctly order routes to ensure correct path matching.

## Bug
The provided `bug.js` file shows an example where the `NotFound` component (wildcard route) always matches, even when navigating to paths like `/` or `/about`. 

## Solution
The `bugSolution.js` file corrects this by placing the wildcard route last.  This ensures that only when no other routes match, the wildcard route is used. 

## How to reproduce the bug
1. Clone this repo.
2. Run `npm install`
3. Run `npm start`
4. Observe that navigating to `/about` still shows the `NotFound` page. 

## How to fix
Use the corrected code in `bugSolution.js`