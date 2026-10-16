# Lab 5: Static Code Analysis — School Transport

## Issues Identified and Fixed

| No. | Issue | Tool | Fix Applied |
|---:|---|---|---|
| 1 | SQL injection risk from constructing SQL queries with f-strings | Bandit B608 | Replaced string interpolation with parameterized SQL queries. |
| 2 | Unsafe subprocess execution using `shell=True` | Bandit B602 | Removed shell execution and displayed the dispatch alert using `print()`. |
| 3 | Bare exception handler | Pylint W0702 / Flake8 E722 | Replaced the bare exception with a specific `sqlite3.Error` handler. |
| 4 | File opened without a context manager | Pylint R1732 | Used `with open(...)` to ensure proper file closure. |
| 5 | File encoding not specified | Pylint W1514 | Specified UTF-8 encoding when writing the roster file. |
| 6 | Function names did not follow snake_case | Pylint C0103 | Renamed functions using the standard Python naming convention. |
| 7 | Missing module and function docstrings | Pylint C0114 / C0116 | Added docstrings describing the module and functions. |
| 8 | Long lines and formatting violations | Pylint / Flake8 | Reformatted statements and improved code readability. |

## Verification

- Pylint score: 10.00/10 (previously 4.00/10).
- Bandit: No issues identified.
- Flake8: No issues reported in the generated report.

The updated code was checked using all three static analysis tools.
