# React Native useEffect Async State Update Bug

This repository demonstrates a common bug in React Native applications involving the `useEffect` hook and asynchronous state updates.  The bug causes inconsistencies in the UI due to stale closures.

## Bug Description

The `useEffect` hook is used to perform side effects, but if the side effect involves an asynchronous operation that updates the state, the UI may not reflect these changes immediately. This is because the closure created by the `useEffect` hook may contain outdated values.

## Solution

The solution involves using either a `ref` or a functional state update to ensure that the state update is correctly reflected in the UI. Using a functional update ensures that the update is based on the latest state value, avoiding potential inconsistencies.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the behavior and compare it with the fixed version.