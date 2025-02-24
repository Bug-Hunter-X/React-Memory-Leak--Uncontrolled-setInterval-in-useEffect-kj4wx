# React Memory Leak: Uncontrolled setInterval in useEffect

This repository demonstrates a common React bug involving memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.  The provided `bug.js` file showcases the problematic code, while `bugSolution.js` offers the corrected implementation.

## Problem

The original code uses `setInterval` inside `useEffect` without a cleanup function.  This means that every time the component renders (even if it unmounts), a new interval is created. This leads to accumulating intervals, consuming memory, and potentially causing performance issues.

## Solution

The solution involves using the cleanup function provided by the `useEffect` hook's return value.  This cleanup function clears the interval when the component unmounts or when the effect dependencies change, preventing memory leaks.

## How to Run

1. Clone this repository.
2. Navigate to the project directory using your terminal.
3. Run `npm install` (or `yarn install`) to install dependencies.
4. Run `npm start` (or `yarn start`) to start the React development server. 