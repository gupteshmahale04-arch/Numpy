
---


# 📊 NumPy Mastery: Full Assignment Series (Explained Simply)

This repository contains a complete hands-on guide and homework tracking for **NumPy**, breaking down how to organize, cut, shape, and calculate data using real-world rules.

---

## 📦 What is NumPy? (The Storage Organizer)
Imagine a standard Python list is a **loose duffel bag**. You can throw a book, an apple, a shoe, and a laptop in there all at once. It’s flexible, but if you want to find something quickly or pack things tightly, it’s messy and slow.

A **NumPy array** is like a **custom ice cube tray** or a **divided bento box**. Every slot is exactly the same size, and everything inside *must* be the same thing (e.g., all water, or all rice). Because it is so structured, computer memory can store it perfectly in a row, making it lightning-fast to use.

---

## 🛠️ Concepts & Real-World Analogies

### 1. Array and Matrix Creation

* **1D Array — A Tape Measure:**
  Think of a simple tape measure or a row of houses on a street. You are just looking at a single line of items.
  ```python
  import numpy as np
  arr = np.array()

```

* **2D Array (Matrix) — A Parking Lot:**
Think of a parking lot grid with **Rows** and **Columns**. To find your car, you need two pieces of information: *"Row C, Spot 4"*.
```python
matrix = np.array([, 
                 , 
                 ])

```





### 2. Special Initialization Functions (Pre-filling Slots)

* **`np.zeros()` — Reserving Seats at a Theater:**
You place "Reserved" signs on empty chairs before people arrive. You are creating empty slots that you plan to fill with numbers later.
```python
zeros_1d = np.zeros(5)        # Gives 5 empty placeholders: [0. 0. 0. 0. 0.]
zeros_2d = np.zeros((2, 4))   # A grid of 2 rows and 4 columns of zeros

```


* **`np.ones()` — Handing Out Blank Paper:**
A teacher handing out a blank sheet of paper to every student. Every single slot starts with the exact same baseline item.
```python
ones_arr = np.ones(6)         # [1. 1. 1. 1. 1. 1.]

```


* **`np.full()` — Stocking a Vending Machine Row:**
A vending machine restocker filling a display shelf entirely with the exact same soda can flavor (e.g., filling every slot with the number 9).
```python
filled_matrix = np.full((3, 3), 9)

```



---

### 3. Generating Numerical Ranges & Random Values

* **`np.arange()` — Skipping Steps on a Staircase:**
Walking up a flight of stairs, but you choose to step **every 2 steps** (0, 2, 4, 6...). You stop *just before* you hit the top floor limit (the end number is excluded).
* **Key Focus:** You care about the **size of the step** you take.


```python
even_arr = np.arange(0, 20, 2)

```


* **`np.linspace()` — Slicing a Loaf of Bread:**
You have a loaf of bread, and you want to slice it so that you get exactly **6 equal pieces**. You don't care how thick the slices are mathematically; you just want 6 identical portions from start to finish.
* **Key Focus:** You care about the **total number of pieces** you end up with.


```python
linear_space = np.linspace(0, 1, 6)

```


* **Random Grids (`randint`, `rand`, `randn`) — Rolling Dice:**
Generating completely unpredictable numbers. Like rolling a 20-sided die to fill a grid, or pulling values from a balanced bell-curve distribution (`randn`).
```python
random_matrix = np.random.randint(1, 21, size=(3, 3))

```



---

### 4. X-Raying an Array (Attributes)

Before working with a tray of data, you can check its label to understand its layout structure:

* **`.shape` (The Blueprint):** Tells you the exact rows and columns (e.g., `(3, 3)`).
* **`.ndim` (The Dimensions):** Tells you if it is flat 1D street line or a 2D box layout.
* **`.size` (The Inventory Count):** Tells you the total number of items stored inside.
* **`.dtype` (The Material Type):** Tells you what kind of data is locked inside, like integers (`int64`) or decimals (`float64`).

---

### 5. Indexing, Slicing & Filtering

* **2D Indexing — Finding a Parking Spot:**
Targeting an exact location using `[row, column]` coordination markers.
```python
# To extract '50' from a grid, find its row index and column index
value = matrix 

```


* **Slicing — Cropping a Picture:**
Cutting out a smaller section from a large grid using `[start:stop]` range selectors.
```python
# Crop out only the first two rows from a larger table
top_rows = matrix[0:2, :] 

```


* **Boolean Indexing — The VIP Bouncer:**
Filtering through an array by setting up a strict checklist condition. Only values that match your criteria are allowed through.
```python
# Check an array and only keep numbers that are greater than 15
filtered = arr[arr > 15] 

```



---

### 6. Reshaping, Flattening & Structural Stacking

* **Reshaping — Playing with Lego Blocks:**
Rearranging your array's data points into a brand-new grid dimension without changing the numbers inside.
```python
# Take a flat line of 6 numbers and rearrange them into a 2x3 box
box = arr.reshape(2, 3) 

```


* **Flattening — Squashing a Box Flat:**
Taking a 2D spreadsheet layout and crushing it back down into a single continuous 1D straight line using `.flatten()`.
* **Stacking (`vstack` & `hstack`) — Adding Train Cars or Building Floors:**
* **`vstack` (Vertical Stacking):** Glue arrays on top of each other like building floors.
* **`hstack` (Horizontal Stacking):** Glue arrays side-by-side like attaching train carriages.


```python
stacked_up   = np.vstack((arr1, arr2))
stacked_side = np.hstack((arr1, arr2))

```



---

### 7. Mathematics & The Magic of Broadcasting

* **Element-wise Math — Teamwork Calculations:**
Unlike regular Python lists, performing math on two NumPy arrays pairs up matching index coordinates and calculates them directly side-by-side.
```python
# Adds matching items up: + becomes
total = arr1 + arr2 

```


* **Broadcasting — The Instant Copy-Paste Machine:**
If you try to add or multiply a single isolated number (a scalar like `5`) to a huge matrix array, NumPy will instantly copy-paste and stretch that single number out across the entire shape behind the scenes so the math can happen instantly.
```python
# Automatically adds 5 to every single number in the array
plus_five = arr + 5 

```



---

### 8. Aggregates & Target Axis Calculations

Instead of manually counting through items, you can instantly run stats across your data:

* **`np.sum()` / `np.mean()**`: Total sum or averages.
* **`np.max()` / `np.min()**`: Find highest and lowest values.
* **Using `axis` direction controls:**
* `axis=0` calculates **Column-wise** (Vertically down columns).
* `axis=1` calculates **Row-wise** (Horizontally across rows).



---

### 9. Fancy Indexing & Sorting Maps

* **Fancy Indexing — Custom Grocery Lists:**
Instead of slicing things in a perfect sequence, you pass a custom list of specific slot locations to pull exact, non-consecutive items instantly.
```python
# Grab the elements at index 0, 2, and 5 out of line
picked = arr[] 

```


* **Sorting Maps (`np.sort()` vs `np.argsort()`):**
* `np.sort()` returns a clean, fully rearranged version of your numbers.
* `np.argsort()` leaves the array alone but gives you the **index roadmap** showing where the smallest-to-largest items are originally sitting.



---

## 📂 Repository Notebook Files Breakdown

* `numpy_assignment_1.ipynb`: Fundamental creation methods (`zeros`, `ones`, `arange`, `linspace`, etc.).
* `numpy_assig..2.ipynb`: Matrix geometry blueprints, advanced index slicing, and truth filter bounds.
* `Numpy_3_Assign....ipynb`: Matrix computational additions, broadcasting stretching, and axis controls.
* `Numpy_4_Assign...ipynb`: Dynamic index picking lists, data sorting tools, and stacking blocks.

```

```
