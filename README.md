# Closure Issue in setTimeout Loop

This repository demonstrates a common closure issue in JavaScript when using `setTimeout` within a loop.  The expected behavior is to log the numbers 0 through 9 with a one-second delay between each. However, due to the way closures work in JavaScript, the loop completes before the `setTimeout` callbacks fire, resulting in all callbacks logging the final value of `i` (which is 10). 

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop.