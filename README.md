# React useEffect Dependency Array Bug

This repository demonstrates a common error in React's `useEffect` hook:  incorrectly specifying the dependency array.  The provided `bug.js` file contains code with this error; `bugSolution.js` shows the corrected version.

## Problem

The counter in `bug.js` only increments once because the dependency array is empty (`[]`).  This means the `useEffect` is only called once when the component mounts.  It should be called every time the `count` changes to update the display correctly.

## Solution

`bugSolution.js` demonstrates the corrected code, where `count` is included in the dependency array. This ensures that `useEffect` runs whenever `count` updates, thereby achieving the desired continuous counter behavior.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the counter's behavior in both versions.