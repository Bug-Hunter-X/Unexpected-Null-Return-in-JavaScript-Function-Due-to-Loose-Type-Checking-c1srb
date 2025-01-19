# Unexpected Null Return in JavaScript Function

This repository demonstrates a common, yet subtle, bug in JavaScript related to loose type checking and null values. The `foo` function aims to add two numbers but returns `null` prematurely if either input is `null`.

## Bug Description

The primary issue lies in the use of `===` (strict equality) in the condition `if (a === null || b === null)`. While this check ensures that only strict null values are considered, it can lead to unexpected behavior when working with values that might be coerced to 0 (like empty strings or even undefined in some cases).

## Solution

A more robust solution involves explicit type checking and handling of null or undefined values by converting them to 0 before addition. This approach prevents unexpected null returns.

## How to Run

1. Clone the repository.
2. Open `bug.js` to see the problematic code.
3. Open `bugSolution.js` to view the improved implementation.
4. Run each file with a Node.js environment to observe the output differences.