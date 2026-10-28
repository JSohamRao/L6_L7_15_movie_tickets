# Lab 6: Code and Branch Coverage Analysis

Jamula Soham Rao | PES2UG24CS202 | Section D

Assignment 15: Movie Tickets. Fork of
[SETAPESU26/L6_L7_15_movie_tickets](https://github.com/SETAPESU26/L6_L7_15_movie_tickets).
The supplied application and starter tests are unchanged.

## Code coverage stage

The original two tests cover 19/38 application statements (50%). The expanded
code coverage suite has 14 passing test cases and covers 38/38 statements
(100%), exceeding the handout's 90% target. Coverage is restricted to
`movie_tickets.py` so test code does not inflate the result.

- [Code coverage tests](Lab%206/CodeCoverageTest_movie_tickets_application.py)
- [Terminal screenshot](Lab%206/screenshots/code_coverage.png)
- [Measured report](Lab%206/evidence/line/coverage.txt)
- [Machine-readable report](Lab%206/evidence/line/coverage.json)
- [Original baseline reports](Lab%206/evidence/baseline/)

## Reproduce

From the repository root in PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r '.\Lab 6\requirements.txt'
Set-Location '.\Lab 6'
..\.venv\Scripts\python.exe -m coverage run --source=movie_tickets -m pytest -q CodeCoverageTest_movie_tickets_application.py
..\.venv\Scripts\python.exe -m coverage report -m --fail-under=90
```

Line coverage shows executed statements. It does not by itself establish that
both outcomes of every decision or every combination of decisions were tested.
Full coverage also does not prove the absence of bugs.
