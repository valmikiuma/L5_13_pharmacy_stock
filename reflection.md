# Static Code Analysis Reflection

## 1. What issues did Pylint identify, and how were they fixed?

Pylint identified an unused import, missing docstrings, a mutable default argument, naming convention problems, and formatting issues. I removed the unused import, added docstrings, corrected the default argument, renamed printStock to print_stock, and improved formatting. The Pylint score improved from 6.90/10 to 10.00/10.

## 2. What security issues did Bandit identify, and how were they fixed?

Bandit identified a possible SQL injection vulnerability because patient input was inserted directly into an SQL query. I fixed it using a parameterized query. I also improved exception handling. After the changes, Bandit reported no issues identified.

## 3. What style issues did Flake8 identify, and how were they fixed?

Flake8 identified formatting problems, including long lines and an unused import. I removed the unused import, corrected the formatting, and split long lines. After rerunning Flake8, no style violations were reported.

## 4. What did you learn from static code analysis?

I learned that static code analysis tools identify potential problems without running the program. Pylint checks code quality, Bandit identifies common security risks, and Flake8 checks coding style. These tools helped improve my program's quality, security, and readability.
