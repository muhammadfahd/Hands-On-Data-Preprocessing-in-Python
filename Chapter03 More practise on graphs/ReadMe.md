 # **Matplotlib Quick Revision Sheet** 
 in a clean, table-based format that is perfect for beginners and quick revision during practice.

---

##  Matplotlib Quick Sheet (Beginner Friendly)

Use this as a summary whenever you forget syntax or customization options.

---

### 1. Basic Plot Structure

| Concept       | Syntax                            | Meaning         |
| ------------- | --------------------------------- | --------------- |
| Import        | `import matplotlib.pyplot as plt` | Load Matplotlib |
| Create figure | `plt.figure(figsize=(7,5))`       | Set plot size   |
| Show plot     | `plt.show()`                      | Display graph   |

---

###  2. Line Plot

| What            | Syntax                           | Notes                     |
| --------------- | -------------------------------- | ------------------------- |
| Basic line plot | `plt.plot(x, y)`                 | Connects points in a line |
| Color           | `plt.plot(x, y, color='red')`    | Change color              |
| Line style      | `plt.plot(x, y, linestyle='--')` | Dashed, dotted, etc.      |
| Marker          | `plt.plot(x, y, marker='o')`     | Shows dots                |

---

###  3. Histogram

| What            | Syntax                              | Notes                   |
| --------------- | ----------------------------------- | ----------------------- |
| Basic histogram | `plt.hist(data)`                    | Distribution            |
| Bins            | `plt.hist(data, bins=20)`           | More bars = more detail |
| Color           | `plt.hist(data, color='green')`     | Bar color               |
| Edge            | `plt.hist(data, edgecolor='black')` | Outlines bars           |
| Transparency    | `plt.hist(data, alpha=0.6)`         | Overlapping histograms  |

---

### 4. Scatter Plot

| What          | Syntax                           | Notes                              |
| ------------- | -------------------------------- | ---------------------------------- |
| Basic scatter | `plt.scatter(x, y)`              | Relationship between two variables |
| Color         | `plt.scatter(x, y, color='red')` | Change dot color                   |
| Size          | `plt.scatter(x, y, s=50)`        | Dot size                           |
| Transparency  | `plt.scatter(x, y, alpha=0.7)`   | Helps reduce overlapping           |

---

### 5. Bar Chart

| What       | Syntax                               | Notes                |
| ---------- | ------------------------------------ | -------------------- |
| Basic      | `plt.bar(x, height)`                 | For categories       |
| Horizontal | `plt.barh(x, height)`                | Horizontal bars      |
| Color      | `plt.bar(x, height, color='purple')` | Bar color            |
| Width      | `plt.bar(x, height, width=0.3)`      | Thinner/thicker bars |

---

### 6. Box Plot

| What     | Syntax                                 | Notes                          |
| -------- | -------------------------------------- | ------------------------------ |
| Basic    | `plt.boxplot(data)`                    | Shows median, spread, outliers |
| Multiple | `plt.boxplot([data1, data2])`          | Compare columns                |
| Labels   | `plt.boxplot([...], labels=['A','B'])` | Add names                      |

---

### 7. Titles, Labels & Grid

| What    | Syntax                 | Notes                   |
| ------- | ---------------------- | ----------------------- |
| Title   | `plt.title("My Plot")` | Add title               |
| X label | `plt.xlabel("X-axis")` |                         |
| Y label | `plt.ylabel("Y-axis")` |                         |
| Grid    | `plt.grid(True)`       | Helpful for readability |

---

### 8. Styles

| What              | Syntax                     | Notes                 |
| ----------------- | -------------------------- | --------------------- |
| Change look/style | `plt.style.use('ggplot')`  | Many styles available |
| Restore default   | `plt.style.use('default')` | Reset                 |

---

### 9. Subplots (Multiple Plots)

| What         | Syntax                                         | Notes            |
| ------------ | ---------------------------------------------- | ---------------- |
| Create grid  | `fig, ax = plt.subplots(1, 2, figsize=(10,4))` | 1 row, 2 columns |
| Plot on axis | `ax[0].plot(data)`                             | First plot       |
|              | `ax[1].hist(data)`                             | Second plot      |

---

###  10. Saving Figures

| What      | Syntax                             | Notes                    |
| --------- | ---------------------------------- | ------------------------ |
| Save plot | `plt.savefig("plot.png")`          | Saves instead of showing |
| DPI       | `plt.savefig("plot.png", dpi=300)` | Higher quality           |

---
