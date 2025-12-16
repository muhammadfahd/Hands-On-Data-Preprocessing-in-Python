# Chapter 2:  Data Visualization
Summary — Data Visualization (Matplotlib + Pandas)

![alt text](285d68dd-charts-1024x581.jpg)
----

Matplotlib is a popular Python library for data visualization.
It allows you to create graphs, charts, and plots to understand data better.

> Matplotlib is a Python library used to create static, animated, and interactive visualizations such as line charts, bar charts, histograms, scatter plots, and more.

* [Understand plots & its types](2.%20Types%20of%20plots%20&%20charts.md)
* [Matplotlib Quick Revision Sheet](1.Matplotlib%20Quick%20Revision%20Sheet.md)


###  Key Features of Matplotlib
| Feature                          | Explanation                                             |
| -------------------------------- | ------------------------------------------------------- |
| **Easy to use**                  | A few lines of code create beautiful charts             |
| **Highly customizable**          | Colors, labels, styles, sizes—everything can be changed |
| **Works with NumPy & Pandas**    | Great for ML, statistics, and data analysis             |
| **Supports many types of plots** | Line, bar, scatter, histogram, pie, etc.                |

###  Summary 

| **Plot Type**               | **Library**                  | **Purpose / What It Shows**                  | **When to Use (Examples)**                     | **Python Code Example**                              |
| --------------------------- | ---------------------------- | -------------------------------------------- | ---------------------------------------------- | ---------------------------------------------------- |
| **Line Plot**               | Matplotlib / Pandas          | Shows trends & changes over continuous data  | Stock price, temperature change, training loss | `py import matplotlib.pyplot as plt; plt.plot(x, y)` |
| **Bar Plot**                | Matplotlib / Pandas          | Compares categories with heights             | Sales per product, students per class          | `py df.plot.bar()`                                   |
| **Horizontal Bar Plot**     | Matplotlib / Pandas          | Same as bar, easier for long labels          | Country names, movie titles                    | `py df.plot.barh()`                                  |
| **Scatter Plot**            | Matplotlib                   | Shows relationships between 2 variables      | GPA vs Study Hours, Age vs Salary              | `py plt.scatter(x, y)`                               |
| **Histogram**               | Matplotlib / Pandas          | Distribution of a continuous variable        | Age distribution, salary bins                  | `py df['age'].plot.hist()`                           |
| **Boxplot**                 | Matplotlib / Pandas          | Detects outliers, shows median and quartiles | Income spread, height variability              | `py df.boxplot(column='age')`                        |
| **Violin Plot**             | Matplotlib (seaborn usually) | Combines boxplot + distribution shape        | Salary distribution with density               | `py plt.violinplot(data)`                            |
| **Subplot (Grid of Plots)** | Matplotlib                   | Multiple plots in the same figure            | Compare multiple variables                     | `py fig, ax = plt.subplots(2,2)`                     |
| **Area Plot**               | Pandas                       | Visualize cumulative totals                  | Stacked energy usage, expenses                 | `py df.plot.area()`                                  |
| **Pie Chart**               | Matplotlib / Pandas          | Parts of a whole                             | Market share, budget breakdown                 | `py df.plot.pie(y='col')`                            |
| **KDE Plot**                | Pandas                       | Smooth distribution curve                    | Probability density, continuous spread         | `py df['age'].plot.kde()`                            |
| **Heatmap**                 | Matplotlib                   | Correlation matrix / intensity map           | Feature correlations, confusion matrix         | `py plt.imshow(data)`                                |
| **Hexbin Plot**             | Pandas                       | Density of scatter points                    | Large scatter datasets                         | `py df.plot.hexbin(x='A', y='B', gridsize=25)`       |
| **Scatter Matrix**          | Pandas                       | Pairwise relationships across columns        | EDA for ML, multivariate analysis              | `py pd.plotting.scatter_matrix(df)`                  |
| **Time Series Plot**        | Pandas                       | Date-indexed trends                          | Sales over time, temperature daily             | `py df['value'].plot()`                              |




| Topic                 | Functions                                     | Purpose                         |
| --------------------- | --------------------------------------------- | ------------------------------- |
| **Matplotlib Basics** | `figure`, `title`, `xlabel`, `ylabel`, `show` | Create basic plots              |
| **Histogram**         | `plt.hist`, `df.plot(kind='hist')`            | Distribution of numeric values  |
| **Boxplot**           | `plt.boxplot`, `df.plot(kind='box')`          | Detect outliers                 |
| **Scatter Plot**      | `plt.scatter`, `df.plot(kind='scatter')`      | Relationships between variables |
| **Line Plot**         | `plt.plot`, `df.plot(kind='line')`            | Trends & sequences              |
| **Bar Plot**          | `plt.bar`, `value_counts().plot(kind='bar')`  | Category comparison             |
| **Subplots**          | `plt.subplot`, `df.plot(subplots=True)`       | Multiple charts in one figure   |
| **Pandas Plotting**   | `df.plot()`                                   | Quick & simple visualization    |
