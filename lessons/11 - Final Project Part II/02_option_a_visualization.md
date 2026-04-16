# Option A — Data Visualization with matplotlib

> **Source:** New content
>
> **Notes for content development:** Students choosing this track have never used matplotlib. The lesson needs to do two things: teach the library mechanics, then connect those mechanics to their project data. Keep these two phases clearly separate — students should run the standalone example and get a chart before they touch their project code. Avoid covering subplots, multiple chart types, or styling beyond labels and rotation. The goal is one good, labeled bar chart — not a matplotlib tutorial. Cover:
> - Installing matplotlib and what it does at a high level
> - A minimal standalone example (~12 lines, fake data) students can run immediately
> - The six matplotlib calls they'll actually use, with a quick-reference table
> - How to go from a list of dicts to separate label/value lists (list comprehensions from Week 5)
> - What makes a chart readable: axis labels, title, tick label rotation for long names
> - Saving to PNG with `plt.savefig()` and the order-of-operations gotcha with `plt.show()`
> - The written explanation requirement and what it should address

---

## What matplotlib Does

`matplotlib` is Python's most common library for creating charts. You give it data, tell it what kind of chart to make, and it produces an image you can display or save to a file.

You don't need to know much about it to complete this track — the same five or six function calls cover everything you need.

Install it:

```bash
pip install matplotlib
pip freeze > requirements.txt   # update your requirements file
```

---

## A Minimal Working Example

Run this before you touch your project. It uses fake data — the goal is to see a chart and understand the pattern, separately from your API data.

```python
import matplotlib.pyplot as plt

# Fake data — you'll replace this with your API data later
labels = ["Category A", "Category B", "Category C", "Category D"]
values = [42, 78, 31, 55]

plt.bar(labels, values)
plt.xlabel("Category")
plt.ylabel("Count")
plt.title("Sample Bar Chart")
plt.tight_layout()
plt.savefig("sample_chart.png")
plt.show()
```

Run it. A window should open showing a bar chart, and a file called `sample_chart.png` should appear in your project folder.

If that works, you've learned the core pattern. Everything from here is adapting it.

---

## The Calls You'll Use

| Call | What it does |
|---|---|
| `plt.bar(labels, values)` | Creates a bar chart. `labels` is a list of strings; `values` is a list of numbers. |
| `plt.xlabel("text")` | Labels the x-axis. |
| `plt.ylabel("text")` | Labels the y-axis. |
| `plt.title("text")` | Adds a title to the chart. |
| `plt.tight_layout()` | Adjusts spacing so labels don't get cut off at the edges. |
| `plt.savefig("filename.png")` | Saves the chart as a PNG. Call this *before* `plt.show()`. |

> **Note:** `plt.show()` is optional when saving to a file. If you call both, call `plt.savefig()` first — `plt.show()` clears the figure, so anything saved after it will be blank.

---

## From API Data to a Chart

Once the standalone example works, the next step is to pull labels and values from your actual API data instead of the hardcoded lists.

Your data is already a list of dicts — for example:

```python
records = [
    {"region": "Africa", "count": 54},
    {"region": "Asia", "count": 48},
    {"region": "Europe", "count": 44},
]
```

Use list comprehensions (from Week 5) to extract the two lists you need:

```python
labels = [r["region"] for r in records]
values = [r["count"] for r in records]
```

Then pass them to `plt.bar()` exactly as before. The rest of the chart code doesn't change.

> **Before you extract:** Make sure your data is already cleaned and processed through your `process_data()` function. Don't do filtering or transformation inside your visualization code — keep those concerns separate.

---

## Making It Readable

A chart without labels is just a picture. Before submitting, check:

- Does the x-axis label describe what the categories represent?
- Does the y-axis label include units if relevant (e.g., "Population (millions)")?
- Does the title state the question the chart answers (e.g., "Top 10 Countries by Population")?
- If your category labels are long and overlapping, add this line after `plt.bar()`:
  ```python
  plt.xticks(rotation=45, ha="right")
  ```

---

## Writing Your Explanation

Your submission requires a brief written explanation of what your visualization shows and why you chose it. Add it to your `README.md` under a `## Visualization` heading.

It should be 3–5 sentences that answer:

1. What question does this chart answer?
2. What does the data show — what's the main takeaway a reader should leave with?
3. Why did you choose this chart type for this data?
