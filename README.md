# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug is caused by omitting necessary dependencies in the `useEffect` hook's dependency array, leading to an infinite render loop. The solution involves correctly specifying the dependencies to control when the effect runs.

## Bug Description

The `bug.js` file contains a component with a `useEffect` hook that lacks the `count` variable in its dependency array.  This causes the effect to run on every render, triggering an update to the `count` state, which in turn triggers another render, and so on, creating an infinite loop.

## Solution

The `bugSolution.js` file demonstrates the corrected code. By adding `count` to the dependency array, the effect now only runs when the `count` variable changes.