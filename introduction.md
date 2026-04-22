---
title: "Jupyter Notebook"
teaching: 30 # teaching time in minutes
exercises: 15 # exercise time in minutes
---

## 1. What Is a Jupyter Notebook?

A **Jupyter Notebook** is an interactive computing environment that allows you to combine:

- Code (Python)
- Text explanations
- Mathematical equations
- Tables and visualizations
- Results and outputs

All in a single document.

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

You can use Jupyter Notebooks in several ways:

- Through [Anaconda Navigator](https://www.anaconda.com/products/navigator). Install the application, create an account, and launch *Jupyter Notebook*.

- Through [Google Collab](https://colab.research.google.com). You would need a google account for this. Then create a new notebook in Drive. 

### Quick Start in Google Colab (easiest for beginners)

1. Go to https://colab.research.google.com
2. Click **File → New notebook**
3. You're ready! No installation needed.

Colab runs in the cloud → you only need a Google account and internet.

**Tip:** The interface looks almost identical to classic Jupyter. 

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

### 4.3 Raw Cells

- Used infrequently
- Mostly for advanced formatting or export purposes

**Note:** This is not too important for our case. 

#### Try it now (in a new notebook):

**Code cell 1**
```python
message = "Hello, welcome to Jupyter!"
print(message)
```

```python
print(message + " We're going to have fun!")
```

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

**Best practice:**
Restart the kernel and run all cells before sharing a notebook.

## 7. Variables and Statefulness – The Most Important Concept

Jupyter remembers variables **across cells** as long as the kernel is running.

This is very powerful… but also the source of most beginner frustration.

### Demo – run these cells one by one

**Cell A**
```python
temperature = 20
print("Temperature is", temperature, "°C")
```

**Cell B**
```python
temperature = temperature + 5
print("New temperature:", temperature, "°C")
```

**Cell C**
```python
print("What is the temperature now?", temperature)
```

:::::::::::::::::::::::::::::::::::: challenge

Challenge — Variable Values State

1. Create 3 new code cells
2. In cell 1: `count = 0`
3. In cell 2: `count = count + 1; print(count)`
4. In cell 3: `print("Final count:", count)`
5. Run all → should print 1
6. Now run **only cell 2** five times
7. Run cell 3 again → what happened?

→ You just experienced statefulness live!

::::::::::::::::::::::::::::::::::::::::::::::::

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

| Do this                              | Why it helps newcomers                     |
|--------------------------------------|---------------------------------------------|
| Restart & Run All often              | Eliminates "ghost variable" bugs           |
| One import block at the top          | Avoids mysterious NameError                 |
| Markdown headers + short comments    | Makes notebook readable like a story       |
| Small cells (5–15 lines max)         | Easier to find & fix mistakes              |


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

## 11. Common Beginner Mistakes & How to Avoid Them

1. **Running cells out of order**  
   → Variables get unexpected values  
   **Fix:** Kernel → Restart & Run All often

2. **Forgetting to import libraries in a fresh kernel**  
   → "NameError: name 'pd' is not defined"  
   **Fix:** Put all `import` statements in the first code cell

3. **One giant code cell with 200 lines**  
   → Hard to debug, hard to fix mistakes  
   **Fix:** Break logic into small cells (one logical step per cell)

4. **No Markdown explanations**  
   → Nobody (including future you) understands what you did  
   **Fix:** Add a Markdown cell before/after important code blocks

5. **Sharing notebook without restarting & running all**  
   → Collaborator sees missing variables or wrong results  
   **Fix:** Always do Kernel → Restart & Run All before sharing/exporting

6. **Assuming outputs are permanent**  
   → Outputs disappear on kernel restart  
   **Fix:** Rely on code, not on saved output images

## 12. Best Practices for Newcomers

- Keep notebooks focused on a single task
- Use clear section headers
- Restart and run all cells before finalizing
- Save notebooks frequently
- Use descriptive file names
- Move reusable code into `.py` files as projects grow


## Exercise 1: Variable Handling

This exercise teaches you how to data is stored and updated for a given variable in python Jupyter notebook. 

Proceed to the activity: <a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Variables_Intro.ipynb" target="_blank">Here</a>

## Exercise 2: Python Coding

This exercise teaches you how to do basic coding in python Jupyter notebook. 

Proceed to the activity: <a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Introduction_Python.ipynb" target="_blank">Here</a>

## Exercise 3: Python Plotting

This exercise teaches you how to perform plotting in python Jupyter notebook. 

Proceed to the activity: <a href="https://colab.research.google.com/github/SpatialTurn/DataCollection-Notebooks/blob/main/Census/Intro_Ploting.ipynb" target="_blank">Here</a>

