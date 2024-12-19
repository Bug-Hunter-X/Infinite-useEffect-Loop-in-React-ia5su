# Infinite useEffect Loop in React

This repository demonstrates a common error in React applications: an infinite loop caused by an incorrectly used `useEffect` hook.

## The Bug
The `useEffect` hook in `bug.js` is designed to log the current count to the console.  However, it lacks a dependency array, causing it to re-run after every render. This creates an infinite loop because updating the console is considered a re-render, leading to high CPU usage and potential crashes.

## The Solution
The `bugSolution.js` file contains the corrected code. By including `[count]` as the dependency array, the `useEffect` hook only re-runs when the `count` value changes.

## How to Reproduce
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console for the infinite log and potential performance issues in `bug.js`.
6. Switch to the `bugSolution.js` file to see how the dependency array fixes the problem.