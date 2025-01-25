# React Router Dom Unexpected Behavior with Catch-All Route

This repository demonstrates an unexpected behavior in React Router Dom v6 related to the catch-all route `/*`. The catch-all route is intended to handle any unmatched routes, but in this case, it's also matching other defined routes, leading to incorrect rendering.  The issue is resolved by rearranging the order of routes, placing the catch-all route last. 

## Bug Description

The `/*` route is unexpectedly matching all other routes before the intended routes can be matched. This results in the `NotFound` component being rendered instead of the other components. 

## How to reproduce

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Run the application using `npm start`.
4. Observe that navigating to `/` or `/about` renders the `NotFound` component.

## Solution
The solution involves reordering the routes so the catch-all route is placed at the end of the routes definition. 