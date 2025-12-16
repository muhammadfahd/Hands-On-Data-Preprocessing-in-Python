
# **Chapter 5 – Advanced Visualization & Figures (Quick Revision Sheet)**

## **1) Purpose of Chapter 5**

This chapter teaches you how to **visualize data effectively** using Python tools like **Matplotlib** and **Pandas plotting**, helping you explore and understand your dataset before preprocessing or modeling. Visualization is essential for spotting:

* patterns and trends
* differences between groups
* outliers
* relationships between attributes ([GitHub][2])

---

## **2) Summarizing Numerical Attributes**

For every **numerical column**, you typically want:

* a **histogram** — to see distribution and skewness
* a **boxplot** — to check the spread and detect outliers

Example approach:

```python
for att in numerical_attributes:
    plt.subplot(2,1,1)
    adult_df[att].plot.hist()
    plt.subplot(2,1,2)
    adult_df[att].plot.box(vert=False)
    plt.tight_layout()
    plt.savefig('{}.png'.format(att), dpi=600)
    plt.show()
```

**Key takeaways:**

* **Histogram:** shows how values are distributed
* **Boxplot:** shows median, quartiles, and outliers
* **Subplots:** place hist and box together for easy comparison
* **Saving figures:** good for reports or portfolios 

---

## **3) Visualizing Categorical Attributes**

For **categorical data** (like workclass, education, marital status), use **bar charts**:

```python
for att in categorical_attributes:
    adult_df[att].value_counts().plot.barh()
    plt.title(att)
    plt.tight_layout()
    plt.savefig(f"{att}.png", dpi=600)
    plt.show()
```

**Takeaways:**

* Bar charts help compare counts across categories
* Horizontal bars (`barh`) improve readability for long category names 
---

##  **4) Comparing Populations**

### ✔ Comparing distributions by group

You can visualize differences between subpopulations, e.g., comparing numerical values across groups using boxplots:

```python
income_possibilities = adult_df.income.unique()
dataForBox_dic= {}
for poss in income_possibilities:
    mask = adult_df.income == poss
    dataForBox_dic[poss] = adult_df[mask]['education-num']

plt.boxplot(dataForBox_dic.values(), vert=False)
plt.yticks([1,2], income_possibilities)
plt.show()
```

**Meaning:**

* You get side-by-side boxplots for each income group
* This makes group differences obvious (spread, medians, outliers) ([GitHub][2])

---

## **5) Comparing Distributions (Two Ways)**

### ✔ Histograms by Group

Overlay or separate histograms to compare distributions for each group:

```python
for poss in income_possibilities:
    subset = adult_df[adult_df.income == poss]['age']
    subset.plot.hist(alpha=0.5, label=poss)
plt.legend()
plt.show()
```

**Why useful:**

* Understand how attributes are distributed differently across groups

---

## **6) Matplotlib Techniques You’ll Use**

| Technique                      | Purpose                         |
| ------------------------------ | ------------------------------- |
| `plt.title()`                  | Add title to plot               |
| `plt.xlabel()`, `plt.ylabel()` | Label axes                      |
| `plt.legend()`                 | Show legend for multiple series |
| `plt.tight_layout()`           | Better spacing between subplots |
| `plt.savefig()`                | Save figure to file             |
| `plt.show()`                   | Display plot                    |

These form the backbone for creating publication-quality figures. ([Scribd][1])

---

## **7) Why This Matters**

* Helps you *understand patterns and problems* before modeling
* Visual checks can catch:

  * skewed distributions
  * different behaviors between groups
  * strange outliers
* Essential step in preprocessing before applying machine learning

> “Visualization is the backbone of data analysis… it allows us to compare, analyze, and see patterns.” ([Packt][3])

---

## 📄 Summary Table (Revision)

| Visualization      | Used For                              | Typical Syntax                       |
| ------------------ | ------------------------------------- | ------------------------------------ |
| Histogram          | Distribution of numeric values        | `df[col].plot.hist()`                |
| Boxplot            | Spread and outliers of numeric values | `df[col].plot.box()`                 |
| Bar Chart          | Counts of categorical values          | `df[col].value_counts().plot.barh()` |
| Group Comparison   | Compare distributions by group        | `plt.boxplot(...); plt.yticks()`     |
| Overlaid Histogram | Compare multiple groups               | `subset.plot.hist(alpha=…, label=…)` |

---

