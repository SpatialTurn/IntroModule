---
title: "Jupyter Notebook"
teaching: 30 # teaching time in minutes
exercises: 15 # exercise time in minutes
---

# Introduction to Jupyter Notebooks
*A Beginner’s Guide for New Data Scientists (Python)*

---

## 1. What Is a Jupyter Notebook?

A **Jupyter Notebook** is an interactive computing environment that allows you to combine:

- Code (Python)
- Text explanations
- Mathematical equations
- Tables and visualizations
- Results and outputs

—all in a single document.

Jupyter Notebooks are especially useful for:

- Data exploration and analysis  
- Teaching and learning Python  
- Prototyping models  
- Sharing reproducible research  

Instead of writing a script and running it all at once, you work in **small, executable blocks called cells**.

---

## 2. Why Data Scientists Use Jupyter Notebooks

Jupyter Notebooks support an **iterative workflow**:

1. Write a few lines of code  
2. Run them immediately  
3. Inspect the output  
4. Modify and rerun as needed  

### Key Advantages

- Immediate visualization of data  
- Easy experimentation  
- Built-in documentation using Markdown  
- Reproducible analysis  
- Simple sharing with collaborators  

---

## 3. Getting Started: Opening a Notebook

You can launch Jupyter Notebooks in several ways:

- Through **Anaconda Navigator**
- From the command line using:
  ```bash
  jupyter notebook
```
- Through **Google Collab**

## 4. Understanding Cells
A Jupyter Notebook is composed of cells. Each cell performs a specific role.

### 4.1 Code Cells
- Used to write and execute Python code
- Output appears directly below the cell

```python
x = 10
y = 5
x + y
```

### 4.2 Markdown Cells

- Used for formatted text, headings, lists, and links
- Supports standard Markdown syntax

Example:

### 4.3 Raw Cells

-Used infrequently
-Mostly for advanced formatting or export purposes

**Note:** This is not too important for our case. 

## 5. Running Cells

You can execute cells using keyboard shortcuts:

* `Shift + Enter` → Run cell and move to next

* `Ctrl + Enter` → Run cell and stay in place

* `Alt + Enter` → Run cell and insert a new one below

**Important:** Cells do not need to be run from top to bottom, but execution order matters.

## 6. The Notebook Kernel

The kernel is the computational engine that runs your code.

For Python notebooks, the kernel:

* Executes Python code

* Stores variables in memory

* Can be restarted or interrupted

### Common Kernel Actions

`Restart Kernel` – Clears all variables

`Interrupt Kernel` – Stops long-running code

Best practice:
Restart the kernel and run all cells before sharing a notebook.

## 7. Variables and Statefulness

Jupyter Notebooks are stateful, meaning variables persist across cells.

```python
a = 5
```

Later in another cell:
```python
a * 2
```
The variable `a` still exists as long as the kernel is running. 

**Running cells out of order can lead to confusing results.**

## 8. Working with Data in Jupyter

Most data science workflows start by importing libraries and loading data.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

### Loading Data
```python
df = pd.read_csv("data.csv")
df.head()
```

## 9. Visualization Inside Notebooks
Plots are displayed inline, directly below the code cell.

Example:
```python
plt.plot([1, 2, 3, 4], [10, 20, 25, 30])
plt.xlabel("X values")
plt.ylabel("Y values")
plt.title("Simple Line Plot")
plt.show()
```
This makes exploratory analysis fast and interactive.

## 10. Using Markdown for Documentation

Well-written notebooks tell a **story**.

Use Markdown cells to:

- Explain your approach
- Describe datasets
- Interpret results
- Organize sections

### Example Notebook Structure:
1. Title: Exploratory Data Analysis
2. Dataset Overview
3. Data Cleaning
4. Visualization
5. Key Findings

This improves readability for both technical and non-technical audiences.

## 11. Common Beginner Mistakes

- Running cells out of order
- Forgetting to restart the kernel before sharing
- Treating notebooks like long scripts
- Skipping Markdown documentation
- Overloading one notebook with multiple tasks

## 12. Best Practices for Newcomers

-Keep notebooks focused on a single task
-Use clear section headers
-Restart and run all cells before finalizing
-Save notebooks frequently
-Use descriptive file names
-Move reusable code into `.py` files as projects grow

