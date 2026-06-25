# 🔢 NumPy - Complete Mastery: From Basics to Advanced Operations

Welcome to the structured notes and assignments repository for the NumPy series. This document serves as a comprehensive, beginner-friendly guide covering foundational array mechanics, mathematical transformations, data manipulation pipelines, and advanced structural arrangement tools.

---

## 📋 Table of Contents

* [What is NumPy and Why Use It?](https://www.google.com/search?q=%231-what-is-numpy-and-why-use-it)
* [Installing & Importing NumPy](https://www.google.com/search?q=%232-installing--importing-numpy)
* [Understanding Vectors vs. Matrices](https://www.google.com/search?q=%233-understanding-vectors-vs-matrices)
* [Data Structural Setup & Creation](https://www.google.com/search?q=%234-data-structural-setup--creation)
* [From a Python List](https://www.google.com/search?q=%23a-from-a-python-list)
* [Special Initialization Functions](https://www.google.com/search?q=%23b-special-initialization-functions)
* [Generating Numerical Ranges](https://www.google.com/search?q=%23c-generating-numerical-ranges)
* [Random Grid Generators](https://www.google.com/search?q=%23d-random-grid-generators)


* [Array X-Ray (Attributes)](https://www.google.com/search?q=%235-array-x-ray-attributes)
* [Indexing, Slicing & Structural Modification](https://www.google.com/search?q=%236-indexing-slicing--structural-modification)
* [Mathematics & The Power of Broadcasting](https://www.google.com/search?q=%237-mathematics--the-power-of-broadcasting)
* [Statistical Calculations & Axis Target Controls](https://www.google.com/search?q=%238-statistical-calculations--axis-target-controls)
* [Advanced Query Maps & Structural Joining](https://www.google.com/search?q=%239-advanced-query-maps--structural-joining)
* [Summary](https://www.google.com/search?q=%2310-summary)

---

## 1. What is NumPy and Why Use It?

**NumPy** (Numerical Python) is the core foundational library optimized for high-performance scientific computing and multi-dimensional numerical processing in Python.

* **Duffel Bag vs. Ice Cube Tray:** A standard Python list is like a loose duffel bag—flexible, but slow to sort because it can store mixed data types. A NumPy array is like a custom ice cube tray—rigidly structured, requiring all elements to be the exact same type (`dtype`), allowing the computer's memory to pack it tightly and process it at lightning speed.
* **Vectorized Efficiency:** Eliminates the overhead of slow standard Python loops by executing calculations instantly in compiled C code.
* **Downstream Integration:** Serves as the computational engine driving major data tools like Pandas, Matplotlib, and Scikit-Learn.

---

## 2. Installing & Importing NumPy

To install the package dependency to your localized system environment, run the following terminal command:

```bash
pip install numpy

```

Once installed, include it within your project source code using the standard community-adopted alias:

```python
import numpy as np

```

---

## 3. Understanding Vectors vs. Matrices

NumPy manages spatial dimensions by categorizing array configurations cleanly:

| Structure | Dimensionality | Description / Analogy |
| --- | --- | --- |
| **Vector** | 1D Array | A single flat line of numbers with one axis (like a tape measure or a row of houses). |
| **Matrix** | 2D Table | A rectangular data grid arranged via rows and columns (like a parking lot grid or spreadsheet). |

---

## 4. Data Structural Setup & Creation

### A. From a Python List

You can transform native standard Python sequence arrays into highly efficient NumPy data structures using `np.array()`.

```python
# Instantiating a flat 1D Vector array
arr = np.array()
print(arr)  # Output: [10 20 30 40 50]

# Converting a nested list into a 2D Matrix grid
matrix = np.array([,,])
print(matrix)

```

### B. Special Initialization Functions

When reserving block spaces ahead of calculations, NumPy provides placeholder tools to populate allocations cleanly:

```python
# np.zeros() — Reserving Seats at a Theater
# Creates structures completely pre-filled with 0.0 decimal values
zeros_1d = np.zeros(4)         # Output: [0. 0. 0. 0.]
zeros_2d = np.zeros()    # A grid with 3 rows and 4 columns

# np.ones() — Handing Out Blank Paper
# Populates layouts entirely with baseline 1.0 elements
ones_matrix = np.ones()

# np.full() — Stocking a Vending Machine Row
# Fills a designated structural layout completely with a custom constant value
filled_grid = np.full(, 7)  # Generates a 3x3 matrix packed with 7s

```

### C. Generating Numerical Ranges

Generate long number sequences predictably without manual entry:

* **`np.arange()` — Skipping Steps on a Staircase:** Counts up from a starting index using a defined **step size** increment. *Note:* The stop parameter boundary value is **exclusive**.
```python
# Count from 0 up to (but excluding) 10 by 1 step
sequence = np.arange(0, 10, 1)  #

```


* **`np.linspace()` — Slicing a Loaf of Bread:** Divides a distance span into a specific **total number of equal segments**. *Note:* The stop boundary value is **inclusive**.
```python
# Cut the distance between 0 and 1 into exactly 5 equal pieces
linear_split = np.linspace(0, 1, 5)  # [0. , 0.25, 0.5 , 0.75, 1. ]

```



### D. Random Grid Generators

Simulate dice rolls or stochastic variables through randomized number models:

```python
# np.random.rand() — Uniform float distribution values bounded strictly between 0 and 1
float_rand = np.random.rand(2, 3)

# np.random.randint() — Rolling Dice
# Produces random integers within a custom range (stop value is exclusive)
int_rand = np.random.randint(1, 20, (3, 3))  # 3x3 grid filled with integers 1-19

# np.random.randn() — Balanced bell-curve distribution tracking normal variance
gaussian_rand = np.random.randn(5)

```

---

## 5. Array X-Ray (Attributes)

Before interacting with a data tray, you can inspect its structural traits using built-in properties:

```python
arr = np.array([,,])

print(arr.shape)  # (.shape) Blueprint dimensions -> Returns: (3, 3)
print(arr.ndim)   # (.ndim) Axis count -> Returns: 2 (2D Matrix layout)
print(arr.size)   # (.size) Inventory size -> Returns: 9 total entries
print(arr.dtype)  # (.dtype) Data type -> Returns: int64

```

> ⚠️ **Crucial Rule:** NumPy structures are strictly homogeneous. If even one data point is a text string, the entire array scales up ("coerces") into a string array.

---

## 6. Indexing, Slicing & Structural Modification

### A. Element Selection & Grid Navigation

Access spatial records precisely using basic indexing frameworks:

```python
# 1D Navigation (Identical to standard Python lists)
arr_1d = np.array()
print(arr_1d)   # Returns: 40

# 2D Navigation — Finding a Parking Spot
# Syntax format: array[row_index, column_index]
matrix = np.array([,,])
print(matrix)  # Target item intersection -> Returns: 5

```

### B. Slicing Subsections

Crop out specific physical segments from a parent data tray:

```python
# Extract intersections spanning rows 0-1 and columns 0-1
cropped_grid = matrix[0:2, 0:2]

# Pull everything from row 1 onward, but isolate only column index 1
sub_column = matrix[1:, 1:2]

```

### C. Boolean Filtering

* **The VIP Bouncer:** Apply logical parameters directly to your array. NumPy screens the array, yields a map of match truths (`True`/`False`), and isolates matching criteria.

```python
nums = np.array()

print(nums > 5)         # Yields index truth log: [False, False, ..., True]
print(nums[nums > 5])   # Isolates valid entries:

```

### D. Geometrical Shifts

Modify the organizational profile of arrays without altering their core components:

```python
# .reshape() — Playing with Lego Blocks
# Rearranges structural patterns cleanly (new math layout totals must match size)
flat_line = np.arange(12)
grid_box = flat_line.reshape(3, 4)  # Converts a flat length-12 line into a 3x4 grid

# .flatten() — Squashing a Box Flat
# Smashes a multi-dimensional matrix back into a 1D sequence line
flattened_line = grid_box.flatten()

```

---

## 7. Mathematics & The Power of Broadcasting

### A. Element-Wise Calculations

Unlike typical Python lists, mathematical operations applied to NumPy arrays pair matching entries instantly across matching index coordinates.

```python
a = np.array()
b = np.array()

print(a + b)  # Addition       ->
print(a - b)  # Subtraction    -> [ 9, 18, 27]
print(a * b)  # Multiplication ->

```

### B. Broadcasting Mechanics

* **The Copy-Paste Trick:** If you mix a single standalone value (a scalar) with a larger matrix array, NumPy copy-pastes and stretches that single factor across the entire operational plane automatically.

```python
scale_vector = np.array()
print(scale_vector * 5)  # Multiplies 5 against every single element ->

```

---

## 8. Statistical Calculations & Axis Target Controls

### A. Universal Statistical Analysis

Extract statistical indicators quickly using built-in high-performance aggregation math properties:

```python
dataset = np.array()

print(dataset.sum())  # Total combination value -> Returns: 293
print(dataset.mean()) # Average value point     -> Returns: 48.83
print(dataset.min())  # Absolute lowest mark    -> Returns: 4
print(dataset.max())  # Absolute highest mark   -> Returns: 100
print(dataset.std())  # Standard Deviation      -> Returns: 32.97
print(dataset.var())  # Variance tracking gap   -> Returns: 1087.47

```

### B. Directional Axis Adjustments

Isolate analysis to a specific directional orientation within 2D structures using the `axis` parameter:

* **`axis=0` (Column-Wise Calculation):** Runs calculations vertically down individual columns.
* **`axis=1` (Row-Wise Calculation):** Runs calculations horizontally across individual rows.

```python
grid = np.array([, 
                , 
                ])

print(np.sum(grid, axis=0))  # Column-wise sum combination -> Returns:
print(np.sum(grid, axis=1))  # Row-wise sum combination    -> Returns: [ 6, 15, 24]

```

---

## 9. Advanced Query Maps & Structural Joining

### A. Fancy Indexing (Custom Index Extraction)

Pass custom lists of coordinate tags to extract values instantly from exact, non-consecutive slots.

```python
# 1D Fancy Index Sorting Map
source = np.array()
print(source[])  # Directly picks entries at index 0, 2, and 4 ->

# 2D Fancy Indexing Matrix Extract
# Syntax matching pattern format: matrix[[rows], [columns]]
matrix_data = np.arange(1, 13).reshape(3, 4)
extracted = matrix_data[,]  # Picks position (1,0) and (2,2) ->

```

### B. Conditional Replacement Mapping

Locate precise index matching patterns using conditions and modify or replace matching elements on the fly.

```python
# np.where(condition, value_if_true, value_if_false)
scores = np.array()
cleansed = np.where(scores > 10, scores, 0)  # Replaces any element under 10 with 0
print(cleansed)  # Output:

```

### C. Sorting Arrays

* **`np.sort()`**: Rearranges values into sorted order. You can sort row-by-row (`axis=1`) or column-by-column (`axis=0`).
* **`np.argsort()`**: Keeps the array array intact but returns the **index map** showing where elements belong in sorted order.

```python
unordered = np.array()
print(np.sort(unordered))     # Sorted array values ->
print(np.argsort(unordered))  # Original index map  ->

```

### D. Structural Joining (`vstack` & `hstack`)

Glue separate distinct arrays together along vertical or horizontal boundaries:

```python
block1 = np.array([,])
block2 = np.array([,])

# Vertical Stacking (np.vstack) — Stack on top of each other like building floors
v_stacked = np.vstack([block1, block2])

# Horizontal Stacking (np.hstack) — Glue side-by-side like attaching train cars
h_stacked = np.hstack([block1, block2])

```

---

## 10. Summary

* NumPy delivers optimized mathematical matrix transformations over native Python list data workflows.
* Transition from creating simple baseline grids using `zeros()`, `ones()`, and range intervals (`arange`/`linspace`) to handling multi-dimensional structures.
* Master targeted matrix selection rules via index ranges, bouncer filters (Boolean indexing), and precision index lists (fancy indexing).
* Apply fast aggregate calculations across column paths or row spans using directional axis parameters.

---

## 📂 Homework & Lab Assignment Directory

* `numpy_assignment_1.ipynb`: Fundamental grid generation practices (`zeros`, `ones`, `arange`, etc.).
* `numpy_assig..2.ipynb`: Inherent data attribute verification metrics, targeted slicing windows, and logical filters.
* `Numpy_3_Assign....ipynb`: Matrix mathematical operations, broadcasting expansions, and mathematical directional weights.
* `Numpy_4_Assign...ipynb`: Dynamic index selection lookups, data sorting indices, and stacking arrays.
* `Class1file.ipynb` to `class4file.ipynb`: Sandbox logs containing laboratory exercises and instructional experiments.
