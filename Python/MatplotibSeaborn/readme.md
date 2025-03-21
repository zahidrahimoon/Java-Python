### 🔥 **Seaborn (sns) Plot Types & Their Uses** 🎨  

Seaborn is a **powerful data visualization library** built on top of Matplotlib, specifically designed for **statistical plotting**. Below is a **detailed guide** to all the important plots, categorized by their purpose.  

---

## 📌 **1. Distribution Plots (To Analyze Data Spread)**  
Used to **visualize the distribution of data** (e.g., salary, age, sales, etc.).

### ✅ **Histogram (sns.histplot)**
📌 **Use it when**: You want to see the frequency distribution of a single variable.
```python
sns.histplot(data=df, x="Salary", bins=30, kde=True)
```
🔹 Shows how salaries are distributed.

### ✅ **Kernel Density Plot (sns.kdeplot)**
📌 **Use it when**: You want a smooth curve of data distribution.
```python
sns.kdeplot(data=df, x="Salary", shade=True)
```
🔹 Works best for continuous numeric data.

### ✅ **Box Plot (sns.boxplot)**
📌 **Use it when**: You want to see **outliers, quartiles, and median**.
```python
sns.boxplot(x="Department", y="Salary", data=df)
```
🔹 Helps in **detecting outliers** in salary distributions.

### ✅ **Violin Plot (sns.violinplot)**
📌 **Use it when**: You want to combine box plot + KDE plot.
```python
sns.violinplot(x="Department", y="Salary", data=df)
```
🔹 Shows **distribution + density** of salary across departments.

---

## 📌 **2. Categorical Plots (To Compare Categories)**  
Used to **compare groups** (e.g., gender vs salary, department vs experience).

### ✅ **Count Plot (sns.countplot)**
📌 **Use it when**: You want to **count occurrences of a category**.
```python
sns.countplot(x="Department", data=df)
```
🔹 Shows the number of employees in each department.

### ✅ **Bar Plot (sns.barplot)**
📌 **Use it when**: You want to **compare averages** between categories.
```python
sns.barplot(x="Department", y="Salary", data=df)
```
🔹 Shows the **average salary per department**.

### ✅ **Strip Plot (sns.stripplot)**
📌 **Use it when**: You want to see individual data points.
```python
sns.stripplot(x="Department", y="Salary", data=df, jitter=True)
```
🔹 Good for **showing distribution** of individual salaries.

### ✅ **Swarm Plot (sns.swarmplot)**
📌 **Use it when**: You want a combination of a strip plot and jitter.
```python
sns.swarmplot(x="Department", y="Salary", data=df)
```
🔹 Provides a **better view of overlapping data points**.

---

## 📌 **3. Relationship Plots (To See How Variables Are Related)**  
Used to **visualize relationships between two numeric variables**.

### ✅ **Scatter Plot (sns.scatterplot)**
📌 **Use it when**: You want to **see correlations between two variables**.
```python
sns.scatterplot(x="Age", y="Salary", data=df)
```
🔹 Shows if **age affects salary**.

### ✅ **Line Plot (sns.lineplot)**
📌 **Use it when**: You want to **see trends over time**.
```python
sns.lineplot(x="Experience", y="Salary", data=df)
```
🔹 Helps understand **how experience impacts salary**.

---

## 📌 **4. Heatmaps (For Correlation & Matrix Data)**  
Used to **visualize correlations and large datasets**.

### ✅ **Correlation Heatmap (sns.heatmap)**
📌 **Use it when**: You want to **see correlations between numeric columns**.
```python
sns.heatmap(df.corr(), annot=True, cmap="coolwarm")
```
🔹 Helps in **feature selection**.

### ✅ **Pivot Heatmap**
📌 **Use it when**: You want to **visualize grouped data**.
```python
pivot = df.pivot_table(values="Salary", index="Department", columns="Gender", aggfunc="mean")
sns.heatmap(pivot, annot=True, cmap="Blues")
```
🔹 Compares **salary differences by gender**.

---

## 📌 **5. Pair Plot (Multiple Relationships in One Go)**  
### ✅ **Pair Plot (sns.pairplot)**
📌 **Use it when**: You want to **see all relationships at once**.
```python
sns.pairplot(df)
```
🔹 **Best for exploratory analysis**.

---

## 🔥 **Which Plot to Use When?**
| **Task** | **Best Plot** |
|----------|-------------|
| See data distribution | Histogram, KDE Plot, Box Plot |
| Compare categories | Bar Plot, Count Plot, Violin Plot |
| Detect outliers | Box Plot, Swarm Plot |
| See relationships | Scatter Plot, Pair Plot |
| Analyze correlation | Heatmap |
| See trends over time | Line Plot |

---

## **🚀 Next Steps?**
Try running these plots on **your employee dataset** in Jupyter Notebook. Let me know if you need **custom visualizations**! 🎨📊
