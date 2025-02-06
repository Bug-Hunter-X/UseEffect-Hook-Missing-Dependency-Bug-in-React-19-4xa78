# useEffect Hook Missing Dependency Bug in React 19

This repository demonstrates a common bug in React 19 involving the `useEffect` hook.  The bug arises from a missing dependency in the `useEffect` call, leading to unexpected re-renders and potential performance problems. The solution shows the corrected code, fixing the issue.

## Bug Description

The `useEffect` hook is used to perform side effects, such as data fetching or DOM manipulation, after a component renders.  A common mistake is forgetting to include all relevant state variables or props in the dependency array.  This can result in infinite loops or unexpected behavior.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs in your browser's developer tools.  You'll see that the 'Count changed' message is logged more frequently than expected, demonstrating the unnecessary re-renders.

## Solution

The solution involves adding the `count` variable to the dependency array of the `useEffect` hook. This ensures that the effect only runs when the `count` value changes. 