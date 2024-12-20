# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common mistake when using the `useEffect` hook in React. The effect runs after every render, even if the data it depends on hasn't changed, causing unnecessary re-renders and potential performance issues.

## Bug
The provided code has an `useEffect` that runs on every render because it doesn't have any dependencies passed into the second argument. 

## Solution
The solution is to add the `count` state variable as a dependency to the `useEffect` hook.  This ensures the effect only runs when the `count` value changes. 