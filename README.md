# Infinite Rendering Bug in React

This repository demonstrates a common bug in React applications: infinite rendering caused by improper use of the `useEffect` hook.  The `MyComponent` initially renders correctly, but the `useEffect` hook, without proper dependency array handling, triggers re-renders endlessly.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console output and the rapid updates in the UI, indicating the infinite loop.

## Solution

The solution involves correctly specifying the dependency array in the `useEffect` hook. By listing `count` as a dependency, the effect only runs when `count` changes and stops this infinite rendering issue.