# React setInterval Memory Leak

This repository demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook: forgetting to clear the interval when the component unmounts. This leads to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component is unmounted, resulting in a memory leak.

## Solution

The `bugSolution.js` file shows the corrected version.  The `setInterval` function is assigned to a variable, and the `clearInterval` function is used in the cleanup function of the `useEffect` hook to stop the interval when the component unmounts.