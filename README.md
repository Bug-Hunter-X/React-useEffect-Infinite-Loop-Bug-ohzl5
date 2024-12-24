# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug causes an infinite loop because of a missing dependency in the `useEffect` dependency array.

## The Bug
The `MyComponent` component uses the `useEffect` hook to log the current value of the `count` state variable to the console. However, the dependency array `[count]` is missing, causing the effect to run after every render, leading to an infinite loop. 

## The Solution
The solution involves adding `count` to the dependency array of `useEffect`. This ensures that the effect only runs when the `count` state variable changes.