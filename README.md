# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite rendering loop.  The bug occurs because the effect modifies state within the component, triggering another render and subsequently another execution of the effect.

## Bug Description
The provided `MyComponent` uses `useEffect` without proper dependency management. The effect runs after every render, leading to a continuous cycle of rendering and state updates.

## Solution
The solution introduces a dependency array to the `useEffect` hook. The dependency array specifies that the effect should only run when the `count` variable changes.  This breaks the infinite loop.