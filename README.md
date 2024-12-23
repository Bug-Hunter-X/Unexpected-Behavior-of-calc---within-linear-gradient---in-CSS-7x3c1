# Unexpected Behavior of calc() within linear-gradient() in CSS

This repository demonstrates an uncommon bug related to the interaction between the CSS `calc()` function and the `linear-gradient()` function.  The bug occurs when attempting to calculate a percentage-based value (with pixel subtraction) for color stop positions within a linear gradient.

## Bug Description
The `calc()` function, when used to determine the position of color stops in a `linear-gradient()`, behaves unexpectedly when combining percentage and pixel values.  Specifically, subtracting pixels from a percentage value does not always produce the expected result, leading to misaligned or incorrect color transitions.

## How to Reproduce
1. Clone this repository.
2. Open `bug.css` and observe the unexpected behavior of the gradient in the `.element` class.
3. Open `bugSolution.css` to see the corrected implementation.

## Solution
The solution involves avoiding the use of pixel subtraction directly within the percentage-based calculation in `linear-gradient()`.  Alternative approaches, such as pre-calculating the value or using only percentage values, provide reliable results.