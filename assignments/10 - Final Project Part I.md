# Assignment 10 — Final Project Part I

## Project Requirements

> Insert final project narative, including pointing to next week's extension work.

### Phase 1: Core Program

Complete Phase 1 before moving to Phase 2.

- Connect to your chosen public API using the `requests` library
- Parse the JSON response into a list of dictionaries with relevant fields extracted
- Handle connection errors and bad status codes with `try/except`
- Organize all fetching and parsing logic into functions with clear parameters and return values

### Phase 2: CLI Tool

Complete after Phase 1.

- Accept at least one form of user input (via `input()` prompts or `argparse` arguments)
- Implement at least one meaningful interaction: filter by a field, look up a specific record, or compare two results
- Display results in a readable, formatted way
- Handle unexpected input without crashing

### Submission

TBD — describe PR requirements, required files (main.py, requirements.txt, README.md), and any demo requirements.

---

## Rubric

> Note that this only is the final project part I rubric. Next week contains the extension rubric.

| Category | Does Not Meet | Meets | Exceeds |
|---|---|---|---|
| **API Integration** | Program fails to connect to the API, or the call is broken and does not run. | Fetches data from the chosen API using `requests`. URL and parameters are clearly organized. | API call is in a dedicated function. Query parameters are passed as arguments rather than hard-coded. |
| **Data Transformation** | JSON response is not parsed, or program crashes when accessing data fields. | JSON is parsed into a list of dicts with relevant fields accessible by key. | Transformation is in a dedicated function. `.get()` is used to handle missing keys without crashing. |
| **CLI Tool** | No user interaction — program prints raw output with no input. | Accepts at least one form of user input and returns formatted results. At least one meaningful interaction is implemented. | Multiple interaction modes available. Output is clearly formatted. Unexpected input is handled without crashing. |
| **Error Handling** | No error handling — connection errors cause unhandled tracebacks. | `try/except` catches connection errors and bad status codes. User sees a clear error message instead of a traceback. | Errors are caught at the right level of the code. Program continues or exits gracefully with a helpful message. |
| **Code Organization** | All logic in one long script with no functions, or functions without parameters and return values. | Logic is split into functions with clear names, parameters, and return values. Each function has one responsibility. | Fetching, parsing, and display are cleanly separated. Code is readable without requiring comments to understand. |
| **Version Control** | Work submitted in a single commit or without a pull request. | Multiple commits show incremental progress. Work submitted via pull request. | Commit messages are descriptive and reflect meaningful stages of development. |
