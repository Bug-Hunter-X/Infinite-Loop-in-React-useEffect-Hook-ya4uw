# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example shows an infinite loop caused by omitting the dependency array in `useEffect`, leading to continuous re-renders.

## Bug Description

The `useEffect` hook is used to perform side effects in functional components.  However, if the dependency array is missing, the effect runs after every render, creating an infinite render loop. This specific example involves a counter that increments, causing the component to perpetually re-render, overwhelming the browser.

## Solution

The solution involves correctly specifying the dependency array.  By including `count` in the dependency array, the effect only runs when `count` changes. This prevents the infinite loop.