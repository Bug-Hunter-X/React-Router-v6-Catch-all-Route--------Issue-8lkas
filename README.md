# React Router v6 Catch-all Route Issue

This repository demonstrates an unexpected behavior in React Router DOM v6 related to the catch-all route ("/*").  The issue is that the catch-all route appears to override more specific routes, preventing them from being matched correctly.

## Problem Description

The `App.js` file contains a basic React Router setup with three routes: a home route ("/"), an about route ("/about"), and a catch-all route ("/*").  The expectation is that the catch-all route should only match if no other route matches. However, in this example, the catch-all route always matches, regardless of whether a more specific route exists.

## How to Reproduce

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install the dependencies.
4. Run `npm start` to start the development server.
5. Observe that navigating to "/about" displays the "404 Not Found" page instead of the "About" page.

## Solution

The solution involves correctly ordering the routes. The catch-all route must be placed at the end of the `Routes` component's children.