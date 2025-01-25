# React useEffect Hook with Missing Dependency

This repository demonstrates a common error when using the `useEffect` hook in React.  The example shows how omitting a dependency or including extra dependencies can lead to unexpected behavior and bugs.  This is crucial to understand for any React developer.  The solution demonstrates the correct usage of the `useEffect` hook.

## Bug Description:

The `useEffect` hook incorrectly only logs the initial count value instead of updating with each increment. This is because the dependency array `[]` is empty, meaning the effect only runs once when the component mounts and never again, despite `count` changing.

## Solution:

The solution adds `count` to the dependency array `[count]`. This ensures the effect runs whenever the `count` value changes, resulting in the expected behavior and logging updates to the console.