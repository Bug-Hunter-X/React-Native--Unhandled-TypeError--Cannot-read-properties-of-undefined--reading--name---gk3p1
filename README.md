# React Native Unhandled TypeError: Cannot read properties of undefined (reading 'name')

This repository demonstrates a common React Native error and its solution. The error, "Unhandled TypeError: Cannot read properties of undefined (reading 'name')", occurs when a component attempts to access a property of an object that is null or undefined.  This often happens when asynchronous data hasn't loaded yet.

## Problem
The `bug.js` file shows how attempting to access the `name` property of the `user` object before it's populated leads to this error.  This is particularly relevant when fetching data from an API or database.

## Solution
The `bugSolution.js` file presents a corrected version. It utilizes optional chaining (`?.`) and nullish coalescing (`??`) to safely access the `name` property.  These operators prevent the error by short-circuiting the access if `user` or `user.name` is null or undefined.