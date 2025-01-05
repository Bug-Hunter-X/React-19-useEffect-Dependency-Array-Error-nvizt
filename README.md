# React 19 useEffect Dependency Issue

This repository demonstrates a common error in React 19 involving the `useEffect` hook and its dependency array.  Incorrectly specifying the dependency array can lead to unexpected behavior, such as infinite loops or stale closures.

## The Problem

The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the current count. However, the dependency array is missing `count`. This means the effect runs on every render, leading to excessive logging and potential performance issues.

## The Solution

The `bugSolution.js` file demonstrates the correct way to use `useEffect`. By including `count` in the dependency array, the effect only runs when the value of `count` changes.