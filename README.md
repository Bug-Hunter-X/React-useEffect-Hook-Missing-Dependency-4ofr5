# React useEffect Hook Missing Dependency

This repository demonstrates a common error in React applications involving the `useEffect` hook: a missing dependency in the dependency array.  This can lead to unexpected behavior, such as infinite loops or incorrect component updates.

## The Problem

The `bug.js` file contains a component that uses the `useEffect` hook to log the current count to the console. However, the `count` variable is missing from the dependency array. This means the effect runs after every render, regardless of whether the `count` value has actually changed.

This can lead to performance issues and unexpected behavior.

## The Solution

The `bugSolution.js` file shows the correct implementation. By including `count` in the dependency array, the effect now only runs when the value of `count` changes.