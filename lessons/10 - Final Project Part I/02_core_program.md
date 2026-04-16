# Building the Core Program

> **Source:** New content
>
> **Notes for content development:** Phase 1. Students are applying skills they already have (requests, try/except, functions) in the context of their own chosen project. The challenge here is integration, not any single new concept. Cover:
> - Writing the `fetch_data()` function: `requests.get()`, `response.raise_for_status()`, `response.json()`
> - Parsing the response into a list of dicts: navigating nested JSON, extracting relevant fields, using `.get()` for fields that might be missing
> - Wrapping the fetch call in `try/except` at the right level (around the network call, not around the whole program)
> - Testing incrementally: print the raw response first, then the parsed list, before writing any CLI logic
> - A note on PokeAPI specifically: making multiple requests in a loop (since PokeAPI is one-resource-per-request) and how that changes the fetch function
>
> Include a collapsible hint box: "Stuck on parsing the response? Click here." The hint should show the pattern for navigating one level of nesting — e.g., `data = response.json()` → `records = data["results"]` → `[{...} for r in records]` — without being API-specific.

TBD
