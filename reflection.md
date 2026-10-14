# Lab 5: Reflection

## 1. What did you learn from static code analysis?

I learned that static analysis tools can identify potential code-quality,
style, and security problems without requiring the program to be run
for every possible input.

## 2. What problems did you find?

The original program contained unsafe promo-code evaluation, broad
exception handling, a mutable default argument, invalid quantity
handling, and insufficient tax-rate validation.

## 3. How did you improve the program?

I restricted promo expressions, validated quantities and tax rates,
improved error handling, corrected the mutable default argument,
and used safer file handling.

## 4. What would you improve in the future?

I would add automated unit tests, implement actual inventory tracking,
store transactions persistently, and test additional invalid inputs.
