# Lab 5: Static Code Analysis

## Issues Identified and Fixed

| Issue                    | Type            | Severity | Description                                                                                | Fix                                                    |
| ------------------------ | --------------- | -------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------ |
| Unsafe eval()            | Security        | High     | The original promo function used eval(), which could execute arbitrary Python expressions. | Replaced eval() with a restricted AST-based evaluator. |
| Broad exception handling | Reliability     | Medium   | A bare except block hid unexpected errors.                                                 | Added explicit validation and logging.                 |
| Mutable default argument | Correctness     | Medium   | The original receipts=[] argument shared a list between function calls.                    | Changed the default to None.                           |
| Negative quantities      | Correctness     | High     | Negative quantities could create negative bills.                                           | Added quantity validation.                             |
| Invalid tax rate         | Correctness     | Medium   | Negative tax rates could cause incorrect billing.                                          | Restricted tax rates to the range 0–1.                 |
| Unsafe file handling     | Reliability     | Low      | The original receipt file was opened without guaranteed closure.                           | Used a context manager and UTF-8 encoding.             |
| Inconsistent naming      | Maintainability | Low      | The original printSales() function did not follow snake_case naming.                       | Renamed it to print_sales().                           |
| Floating-point display   | Correctness     | Low      | Monetary totals could display unnecessary decimal places.                                  | Rounded totals to two decimal places.                  |

## Conclusion

Static analysis helped identify security, correctness, reliability,
and maintainability problems. The code was updated to improve input
validation, promo-code handling, exception management, and file handling.
