# Assignment 11 — Final Project Part II

Choose one extension track and complete its requirements. Both tracks share the same universal requirements.

---

## Universal Requirements

Apply to both options.

- **Modular design:** All extension logic in reusable functions with clear parameters and return values
- **Standard library usage:** Use at least one standard library module beyond `csv` (e.g., `os`, `datetime`)
- **Version control:** All work committed and submitted via pull request; commit history shows incremental progress across both weeks
- **Video demo:** A screen-recorded video (2–4 min) walking through your running project and explaining one technical decision you made

---

## Option A Requirements

- Use `matplotlib` to create at least one chart that answers a specific question you pose about your data
- Label your chart: axis labels, a descriptive title, and readable tick labels
- Save the chart as a PNG file
- Include a written explanation in `README.md` (under `## Visualization`) describing what the chart shows, what the main takeaway is, and why you chose that chart type

## Option B Requirements

- Clean the data: handle missing values, normalize field types, and filter invalid records using the per-field decision framework
- Export the cleaned data to a well-structured CSV file using `csv.DictWriter`
- Include a written explanation in `README.md` (under `## Data Cleaning Decisions`) describing which fields you included, what you did with missing or invalid values, and any type coercion applied

---

## Submission

TBD — describe final PR requirements, video upload instructions, and any showcase details.

---

## Rubric

> Note that this is the Part II rubric. Can also point to the full [final project rubric](https://github.com/Code-the-Dream-School/intro-to-python-v1/blob/main/resources/final-project-overview.md).

| Category | Does Not Meet | Meets | Exceeds |
|---|---|---|---|
| **Extension Track** | Extension not attempted, or broken and does not run. | Extension requirements met: chart answers a stated question with appropriate labels (A), or CSV exported with cleaned data and written explanation (B). | Chart is polished and well-labeled (A), or data cleaning handles multiple edge cases with clear reasoning (B). Written explanation reflects genuine decision-making, not just a description of the code. |
| **Modular Design** | Extension logic mixed into existing functions or written as one monolithic block. | Extension logic is in dedicated functions with clear parameters and return values. | Functions are well-named and single-purpose. The extension integrates cleanly with the Week 10 codebase. |
| **Standard Library** | No standard library module used beyond `csv`. | At least one standard library module used appropriately. | Standard library usage is well-chosen and adds real value (e.g., `datetime` for timestamps, `os.path` for file handling). |
| **Version Control** | All extension work in a single commit. | Multiple commits show incremental progress. Work submitted via pull request. | Commit messages are descriptive and reflect meaningful stages of development across both weeks. |
| **Video Demo** | No video submitted, or video does not show the running program. | 2–4 minute video walks through the running project and explains one technical decision. | Technical explanation goes beyond what the code says to *why* the decision was made. |
