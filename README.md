# React Router Catch-All Route Issue

This repository demonstrates a common issue with React Router's catch-all route (`/*`). When placed incorrectly, this route can prevent other, more specific, routes from being matched, leading to unexpected rendering of the 404 page.

## Issue Description
The problem arises because the catch-all route is extremely general.  The `/*` path matches *any* URL.  If it is placed above other routes, it effectively intercepts all requests, rendering the NotFound component regardless of the requested URL.

## Solution
The solution is to place the catch-all route *last* in the route definition. This ensures that it only matches URLs that do not match any of the other routes, resulting in a proper 404 page only when appropriate.

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to `/`, `/about` or any other URL; you'll see the 404 page even for valid routes.

Now look at AppSolution.js to see the solution.