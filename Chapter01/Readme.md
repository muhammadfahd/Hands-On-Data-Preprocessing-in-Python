The codes and the datasets used for Chapter 1 of the book Hands-on Data Preprocessing using Python are in this folder. 


# ⭐ **Chapter 1 – Quick Revision Sheet (NumPy + Pandas Basics)**

* **Chapter 1.ipynb** - Detailed Notebook for practising & learning using adult.csv

## For **quick review**, **easy memory**, and **future practice**.
---

# **1. NumPy Basics**

## 📌 **NumPy Functions Overview**

| Concept / Function  | Purpose                 | Explanation                               | Example                                      |
| ------------------- | ----------------------- | ----------------------------------------- | -------------------------------------------- |
| **`.dtype`**        | Check data type         | Shows type of elements inside NumPy array | `arr.dtype`                                  |
| **`.mean()`**       | Average value           | Computes the mean of the array            | `np.array([1,2,3]).mean()`                   |
| **`np.arange()`**   | Create a sequence       | Creates array with a range of numbers     | `np.arange(1, 10, 2)`                        |
| **`np.zeros()`**    | Create array of zeros   | Useful for initializing arrays            | `np.zeros((3,3))`                            |
| **`np.ones()`**     | Create array of ones    | Similar to zeros — filled with 1s         | `np.ones(5)`                                 |
| **`enumerate()`**   | Loop with index + value | Gives both position and value in loop     | `for i, val in enumerate(arr):`              |
| **`np.linspace()`** | Evenly spaced numbers   | Creates numbers between a start and end   | `np.linspace(0,1,5)` → `[0,0.25,0.5,0.75,1]` |

---

#  **2. Pandas Basics**

## **CSV Handling**

| Function        | Purpose            | Example                        |
| --------------- | ------------------ | ------------------------------ |
| `pd.read_csv()` | Load dataset       | `df = pd.read_csv("file.csv")` |
| `.head()`       | Preview first rows | `df.head(5)`                   |
| `.shape`        | Dataset size       | `(rows, columns)`              |
| `.columns`      | List column names  | `df.columns`                   |
| `.describe()`   | Summary stats      | Numerical statistics           |

---

#  **3. Accessing Data in Pandas**

| Concept           | Purpose               | Explanation                        | Example              |
| ----------------- | --------------------- | ---------------------------------- | -------------------- |
| **Access column** | View a column         | Use column name                    | `df['age']`          |
| **`.loc`**        | Label-based selection | Access by row labels, column names | `df.loc[0:5, 'age']` |
| **`.iloc`**       | Index-based selection | Access by row/column numbers       | `df.iloc[0:5, 2]`    |

---

#  **4. Exploring Dataset (EDA Basics)**

| Function          | Purpose                    | Example                       |
| ----------------- | -------------------------- | ----------------------------- |
| `.shape`          | Show number of rows & cols | `df.shape`                    |
| `.columns`        | List all column names      | `df.columns`                  |
| `.info()`         | Data types + null values   | `df.info()`                   |
| `.describe()`     | Statistical summary        | `df.describe()`               |
| `.value_counts()` | Count unique values        | `df['gender'].value_counts()` |

---

#  **5. Visualization Basics (Using Pandas Plot)**

| Plot Type            | Purpose             | Example                                           |
| -------------------- | ------------------- | ------------------------------------------------- |
| `.plot(kind='hist')` | Histogram           | `df['age'].plot(kind='hist')`                     |
| `.plot(kind='bar')`  | Bar chart           | `df['education'].value_counts().plot(kind='bar')` |
| `.plot(kind='box')`  | Box plot (outliers) | `df['income'].plot(kind='box')`                   |

> Pandas uses **Matplotlib** internally.

---

# **6. Grouping and Aggregation**

| Function     | Purpose                   | Example                                 |                                  |
| ------------ | ------------------------- | --------------------------------------- | -------------------------------- |
| `.groupby()` | Group by a column         | `df.groupby('gender')['income'].mean()` |                                  |
| Aggregation  | Calculate stats per group | `.sum(), .mean(), .count()`             | `df.groupby('education').size()` |

---

#  **7. Custom Functions in Pandas**

You can define your own function and apply it:

### Example:

```python
def convert(x):
    return x * 2

df['salary_doubled'] = df['salary'].apply(convert)
```

Purpose:

* Custom transformations
* Feature engineering
* Cleaning text
* Scaling values

---

# ⭐ **Summary Sheet (for quick glance)**

| Area                 | Key Tools                                                                                   |
| -------------------- | ------------------------------------------------------------------------------------------- |
| **NumPy**            | `.dtype`, `.mean()`, `np.arange()`, `np.zeros()`, `np.ones()`, `enumerate`, `np.linspace()` |
| **Pandas I/O**       | `read_csv()`, `.head()`, `.shape`, `.columns`, `.describe()`                                |
| **Data Access**      | `df['col']`, `.loc`, `.iloc`                                                                |
| **EDA**              | `.info()`, `.value_counts()`, `.describe()`                                                 |
| **Plotting**         | `hist`, `bar`, `box`                                                                        |
| **Grouping**         | `.groupby()`, `mean`, `size`, `count`                                                       |
| **Custom Functions** | `.apply(function)`                                                                          |

---


