# Test info

- Name: add() >> adds positive numbers
- Location: /Users/weyvern/Documents/WBS/javascript-self-assessment-001/tests/studentFunctions.test.js:5:7

# Error details

```
Error: expect(received).toBe(expected) // Object.is equality

Expected: 5
Received: undefined
    at /Users/weyvern/Documents/WBS/javascript-self-assessment-001/tests/studentFunctions.test.js:6:23
```

# Test source

```ts
   1 | import { test, expect } from '@playwright/test';
   2 | import { add, fibonacci, isPrime } from '../src/studentFunctions.js';
   3 |
   4 | test.describe('add()', () => {
   5 |   test('adds positive numbers', () => {
>  6 |     expect(add(2, 3)).toBe(5);
     |                       ^ Error: expect(received).toBe(expected) // Object.is equality
   7 |   });
   8 |
   9 |   test('adds negative numbers', () => {
  10 |     expect(add(-4, -6)).toBe(-10);
  11 |   });
  12 | });
  13 |
  14 | test.describe('fibonacci()', () => {
  15 |   test('first six numbers', () => {
  16 |     expect(fibonacci(6)).toEqual([0, 1, 1, 2, 3, 5]);
  17 |   });
  18 | });
  19 |
  20 | test.describe('isPrime()', () => {
  21 |   const cases = [
  22 |     [2, true],
  23 |     [3, true],
  24 |     [4, false],
  25 |     [17, true],
  26 |     [21, false]
  27 |   ];
  28 |
  29 |   for (const [n, expected] of cases) {
  30 |     test(`isPrime(${n}) → ${expected}`, () => {
  31 |       expect(isPrime(n)).toBe(expected);
  32 |     });
  33 |   }
  34 | });
  35 |
```