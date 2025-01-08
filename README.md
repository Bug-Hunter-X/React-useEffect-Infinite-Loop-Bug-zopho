# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop due to missing dependencies in the useEffect's dependency array.

## Bug Description
The provided `MyComponent` utilizes `useEffect` to log the current count to the console after every render.  However, the dependency array is empty (`[]`), leading to the effect running on every render. The effect triggers a re-render which triggers the effect again resulting in an infinite loop.

## Solution
The solution involves correctly specifying the dependencies in the useEffect's dependency array,  Specifically, in this case we should include the 'count' state variable to ensure that the effect only runs when the count changes. This prevents the infinite loop.
