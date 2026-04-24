# Reading and Writing .txt and .csv Files

> **Source:** Ported from Python Essentials — PE 2.2 (File Handling)
>
> **Porting notes:** Take PE 2.2 largely as-is. Cover `open()` modes (`r`, `w`, `a`), the `with` statement and why it's preferred, reading line by line with `.readlines()`, writing with `.write()` and newline handling, then CSV with `csv.reader` and `csv.writer`. Also bring in `csv.DictReader` and `csv.DictWriter` — they set up the list-of-dicts pattern that the next section builds on. Wrap file operations in `try/except` (connecting back to Week 8's upcoming content — or forward-reference it here).

In Python, reading from and writing to text files is handled with the `open()` function. Text files are simple, containing plain text data, making them ideal for storing simple logs, configuration data, or notes.

#### Reading a Text File

To read a file, use `open()` with the `"r"` (read) mode and call `.read()`, `.readline()`, or .`readlines()` to get the content.

```python
with open('example.txt', 'r') as file:
    content = file.read()  # Read entire file
    print(content)
```

The python above uses the `with` statement.  This is a way to keep your code looking clean.  You always want to close the file when you are done.  The `with` statement closes it for you on exit from the block.  The file is closed even if there is an exception, but the exception is still passed on to you.  Later in the course, you will also use the `with` statement for a database connection, and it serves the same purpose.

File operations, including the open(), can raise exceptions.  To make your code robust, you put them in a try block, as follows:

```python
try:
    with open('example.txt', 'r') as file:
        content = file.read()  # Read entire file
        print(content)
except Exception as e:
    print(f"An error occurred reading the file: {e}")
else:
    print("The file was read ok.")
```
If your `with` block is longer, you may have other try blocks inside it for more granular exception handling.

#### Writing to a Text File

To write to a file, open it in `"w"` (write) or `"a"` (append) mode. Writing mode will overwrite the file if it exists, while append mode will add to the file.

```python
with open('example.txt', 'w') as file:
    file.write("Hello, World!")  # Write to the file
```

The `write()` method does not add a newline after the string which is provided.  The special character `'\n'` can be added to the end of the string to add a newline.

#### Additional Modes

* `"r+"`: Read and write
* `"a"`: Append to the file (keeps existing content).

### Reading and Writing CSV Files

CSV (Comma-Separated Values) files are commonly used to store tabular data, where each row is a new line, and each value is separated by a comma. Python’s built-in `csv` module makes it easy to work with these files.

#### Reading a CSV File

To read a CSV file, use `csv.reader()` and iterate through the rows.

```python
import csv

with open('example.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

#### Writing to a CSV File

To write to a CSV file, use `csv.writer()`. Each row should be a list or tuple representing a row in the CSV.

```python
import csv

with open('example.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(['Name', 'Age', 'City'])  # Write header row
    writer.writerow(['Jazmine', 30, 'New York'])  # Write a data row
```

#### Additional Options

* `csv.DictReader()` and `csv.DictWriter()`: Use dictionaries to work with row data, which can make reading and writing more convenient when you have headers.

### 2.2 Video: Reading and Writing a CSV File

In this video, we'll demonstrate reading and writing to a real CSV file. After the video, practice reading and writing to a CSV file using the W3 Resource tutorial [here](https://www.w3resource.com/python-exercises/csv/index.php).

**[View the video here](https://youtu.be/MWYRGLKMzAQ?feature=shared).**

### 2.2 Check for Understanding

**Question**: What does the `"w"` mode do when opening a file in Python?

* A) Reads the file without making changes.
* B) Appends new data to the end of the file.
* C) Overwrites the file with new data, creating it if it doesn’t exist.
* D) Opens the file for reading and writing without overwriting.

<details>

<summary>Answer</summary>

**Answer**: C) Overwrites the file with new data, creating it if it doesn’t exist.

</details>

### 2.2 AI Prompt: Retrieval Practice

Now that you have explored File Handling and different file modes, let's check your knowledge:
1. Open your AI chatbot.
2. Explain the difference between opening a file in "w" (write) mode versus "a" (append) mode.
3. Ask the AI: "In what specific scenario would I accidentally lose data if I used the wrong mode?"

**Example prompt:** "I am learning about Python file modes. I think 'w' mode is for [your explanation] and 'a' mode is for [your explanation]. Is this correct? Also, can you explain the risk of using 'w' on an existing file?"
