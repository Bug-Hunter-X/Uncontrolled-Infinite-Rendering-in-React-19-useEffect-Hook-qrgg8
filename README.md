# Uncontrolled Infinite Rendering in React 19 useEffect Hook

This repository demonstrates a common error in React 19 applications involving the `useEffect` hook.  Improper use of dependencies in `useEffect` can lead to uncontrolled infinite re-renders, causing performance issues and application crashes.

The `bug.js` file contains code exhibiting this issue.  The `bugSolution.js` file provides a corrected version.

## Problem

The `useEffect` hook in `bug.js` lacks dependencies. This means it runs after every render, causing an infinite loop if it modifies state or performs actions that trigger further renders. The console log continuously shows that this component rerenders.

## Solution

The `bugSolution.js` file demonstrates the correct usage of the `useEffect` hook.  By specifying dependencies (`[count]`), the effect only runs when the `count` variable changes.