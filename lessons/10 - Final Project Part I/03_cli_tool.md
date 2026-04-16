# Building the CLI

> **Source:** New content
>
> **Notes for content development:** Phase 2. Students add user interaction to the core program they built in Phase 1. Cover:
> - Two approaches to user input: `input()` prompts (simpler, good for interactive use) vs. `argparse` (more professional, good for script-style invocation). Students can choose either; brief pros/cons of each.
> - What "at least one meaningful interaction" looks like in practice: filtering a list by a field value, looking up a record by name/id, or comparing two records side by side
> - Formatting output for readability: using f-strings, simple column alignment, or separator lines — not just printing a raw dict
> - Handling unexpected input: what happens if the user types a region that doesn't exist, or leaves the prompt blank? The program should not crash.
> - The role of `main()`: this is where the interaction loop lives — call `fetch_data()`, call `process_data()`, ask for input, call `display_results()`; all the pieces from Phase 1 come together here
>
> Include a collapsible hint box: "Stuck on formatting output? Click here." Show a simple example of iterating over a list of dicts and printing selected fields with f-strings, without being API-specific.

TBD
