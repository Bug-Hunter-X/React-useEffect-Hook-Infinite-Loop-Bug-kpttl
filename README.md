# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook and its dependency array.  The bug causes an infinite render loop, leading to poor performance or crashes.

## Bug Description

The `useEffect` hook is designed to perform side effects after a component renders.  However, if the dependency array is missing or incorrect, the effect will run repeatedly, leading to an infinite loop.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console logs and the rapid counter increments. 

## Solution

The solution involves correctly specifying the dependencies in the `useEffect` hook's dependency array. By including `count` in the array, the effect only runs when the value of `count` changes. This prevents the infinite loop.