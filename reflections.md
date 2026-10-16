# Lab 5: Static Code Analysis — Reflection

## 1. Which issues were the easiest to fix, and which were the hardest? Why?

The easiest issues to fix were formatting problems, long lines, missing docstrings, and function naming conventions because they required straightforward changes. The hardest issues were the SQL injection risk and unsafe subprocess execution because they required understanding security risks and changing how the program handled database queries and dispatch alerts.

## 2. Did the static analysis tools report any false positives? If so, describe one example.

In this run, I did not identify a confirmed false positive. The tools reported potential issues that were useful to review and correct. Bandit's initial warning about subprocess usage required examining how the command was executed before deciding on the appropriate fix.

## 3. How would you integrate static analysis tools into your actual software development workflow?

I would run Pylint, Bandit, and Flake8 regularly while developing Python applications. I would execute them before committing changes and integrate them into a continuous integration pipeline so that code-quality, security, and formatting issues could be detected early.

## 4. What tangible improvements did you observe in the code quality, readability, or potential robustness after applying the fixes?

The code became more readable and consistent through better naming, docstrings, and formatting. Parameterized SQL queries reduced the risk of SQL injection, the dispatch function no longer used shell execution, and context-managed file handling improved resource management. The Pylint score improved from 4.00/10 to 10.00/10, while Bandit and Flake8 reported no issues in the final run.
