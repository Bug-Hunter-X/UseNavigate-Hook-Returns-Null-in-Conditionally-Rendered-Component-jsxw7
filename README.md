# React Router Dom v6 useNavigate Hook Bug

This repository demonstrates a subtle bug in React Router Dom v6 involving the `useNavigate` hook and conditionally rendered components.  The problem arises when `useNavigate` is used within a component that isn't initially mounted, causing it to return `null` and preventing navigation.

## Problem

The `useNavigate` hook in React Router Dom v6 requires the component using it to be mounted before it can function correctly. If the component is conditionally rendered and isn't rendered initially, `useNavigate` will return `null`.

## Solution

The solution involves checking if `useNavigate` returns a value before attempting to use it for navigation.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe that clicking the button before the delay elapses will not navigate as expected.