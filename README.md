# React useEffect causing unnecessary re-renders

This example demonstrates an issue with the React `useEffect` hook, where it causes unnecessary re-renders due to missing dependencies. 

The `useEffect` hook is used to perform side effects after the component renders.  In this case, the effect logs a message to the console each time the component renders.  However, without a dependency array, the effect runs after every render, even if the `count` state doesn't change.

The solution shows how to fix this by passing the `count` state as a dependency.

## Bug
The `bug.js` file contains the buggy code, which causes the `console.log` message to appear on every render. 

## Solution
The `bugSolution.js` file demonstrates the corrected code. The dependency array `[count]` ensures that the `useEffect` runs only when the `count` state changes. This prevents unnecessary re-renders and improves performance.