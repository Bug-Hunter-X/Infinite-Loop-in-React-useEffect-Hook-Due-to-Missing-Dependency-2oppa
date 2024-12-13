# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by missing dependencies in the dependency array.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version. 

**Bug:** The original component attempts to log the updated count. However, without the `count` variable in the dependency array, the effect runs on every render, leading to an infinite loop of state updates and re-renders.

**Solution:** Adding `count` to the dependency array resolves the issue.  The effect will now only run when `count` changes, preventing the infinite loop. 

This example highlights the importance of carefully considering and correctly specifying the dependencies within the `useEffect` hook to avoid unexpected behavior and performance issues.