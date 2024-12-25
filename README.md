# React useEffect: Accessing State Before Initialization

This repository demonstrates a common error in React applications: attempting to access a state variable within the `useEffect` hook before it has been initialized. This can lead to unexpected behavior or errors during the initial render.

## Problem

The `bug.js` file contains a component that uses the `useState` hook to manage a counter.  The `useEffect` hook attempts to log the initial value of `count` before `useState` has had a chance to assign a value to it. This results in `count` being `undefined`.

## Solution

The `bugSolution.js` file shows how to correctly handle this situation.  The initial log is moved inside a conditional to only access `count` after it has been initialized.