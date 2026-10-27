# Static Code Analysis Issues

The following issues were identified in the original pharmacy_system.py.

| Issue | Type | Line(s) | Description | Fix Approach |
|---|---|---|---|---|
| Possible SQL injection | Security - Medium | 21 | Patient input was inserted directly into an SQL query. | Used a parameterized query with WHERE name = ? and (name,). |
| Broad exception handling | Error handling - Low | 38, 58 | Broad exception handling could hide errors. | Replaced it with more appropriate explicit handling. |
| File handling issues | Resource handling | 50, 57 | Files were opened without context managers or explicit encoding. | Used with open(..., encoding="utf-8"). |
| Mutable default argument | Code quality | 24 | A default list could be shared between function calls. | Changed the default to None and initialized the list inside the function. |
| Unused import | Code quality | 3 | The os module was imported but not used. | Removed the unused import. |
| Missing docstrings | Documentation | Multiple | The module and functions lacked documentation. | Added module and function docstrings. |
| Naming convention | Style | 61 | printStock did not follow snake_case. | Renamed it to print_stock. |
| Long lines and formatting | Style | Multiple | Some lines were too long or inconsistently formatted. | Improved line breaks and formatting. |

## Final Tool Results

- Pylint: 10.00/10
- Bandit: No issues identified
- Flake8: No style violations reported

Note: Line numbers refer to the original version and may differ in the corrected version.
