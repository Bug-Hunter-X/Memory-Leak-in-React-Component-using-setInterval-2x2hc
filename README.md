# React setInterval Memory Leak
This repository demonstrates a common React bug involving memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.  The `bug.js` file shows the flawed implementation, while `bugSolution.js` provides the corrected version.

## Problem
The original code uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, leading to continued updates even after the component is no longer displayed. This results in a memory leak and potential performance issues.

## Solution
The solution utilizes the return value of `useEffect` to implement cleanup.  The interval ID is stored and returned. This ensures that `clearInterval` is called when the component is unmounted, preventing the memory leak.

## How to run
Clone this repo and run `npm install` to install the necessary packages. Then run `npm start` to see the buggy component, and `npm run solution` to see the corrected one.