# React setInterval Memory Leak

This repository demonstrates a common mistake in React: using `setInterval` within `useEffect` without proper cleanup. This leads to memory leaks and unexpected behavior.

## The Problem

The `bug.js` file shows a React component that uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component unmounts. This means the interval continues to run, even after the component is no longer in the DOM, leading to memory leaks and potential performance issues.

## The Solution

The `bugSolution.js` file demonstrates the correct way to handle `setInterval` within `useEffect`.  It uses the return value of `useEffect` to clear the interval before the component unmounts, preventing memory leaks.

## How to run

1. Clone this repo
2. `npm install`
3. `npm start`