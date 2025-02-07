# React useEffect setInterval memory leak
This example demonstrates a common mistake when using `setInterval` inside a React `useEffect` hook: forgetting to clear the interval in the cleanup function. This can lead to memory leaks and unexpected behavior.

## Bug
The `bug.js` file contains a component that uses `setInterval` to update a count every second. However, it fails to include a cleanup function to clear the interval when the component unmounts or the effect is replaced. This results in the interval continuing to run even after the component is no longer needed.

## Solution
The `bugSolution.js` file corrects the issue by adding a cleanup function that uses `clearInterval` to clear the interval before the component unmounts. This prevents memory leaks and ensures that the interval is properly managed.
