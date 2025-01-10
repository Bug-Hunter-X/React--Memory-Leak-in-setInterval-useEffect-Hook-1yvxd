# React: Memory Leak in setInterval useEffect Hook

This repository demonstrates a common mistake when using the `setInterval` function within the `useEffect` hook in React.  Forgetting to include a cleanup function to clear the interval results in a memory leak.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it's missing the cleanup function within the `useEffect`'s return statement. This means the interval continues to run even after the component is unmounted, leading to a memory leak.

## Solution
The `bugSolution.js` file shows the corrected version. The `clearInterval` function is used in the return statement of the `useEffect` hook to properly stop the interval when the component unmounts, fixing the memory leak.