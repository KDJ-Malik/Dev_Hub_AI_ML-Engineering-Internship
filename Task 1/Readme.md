# Task 1: Exploring and Visualizing the Iris Dataset

## Objective
The objective of this task is to load, inspect, and visualize the Iris dataset. This was done to understand its structure, feature distributions, relationships between variables, and identify patterns or outliers using exploratory data analysis (EDA).

---

## Dataset Used
**Dataset:** Iris Dataset

The Iris dataset is a classic machine learning dataset containing measurements of iris flowers from three species:

- Setosa
- Versicolor
- Virginica

### Features
- **Sepal Length (cm)**
- **Sepal Width (cm)**
- **Petal Length (cm)**
- **Petal Width (cm)**

### Target Variable
- **Species**

### Dataset Size
- **Rows:** 150
- **Columns:** 5

The dataset was loaded directly using Seaborn's built-in dataset loader.

---

## Tools and Libraries Used
- Python
- Pandas
- Matplotlib
- Seaborn

---

## Data Exploration Performed

### 1. Dataset Inspection
The dataset was inspected using:

- `.shape`
- `.columns`
- `.head()`
- `.info()`
- `.describe()`

This provided information about:
- Data dimensions
- Feature names
- Data types
- Missing values
- Statistical summaries

---

### 2. Visualizations Created

#### Scatter Plot
A scatter plot was used to examine relationships between sepal length and petal length across species.

**Observation:**  
Species form distinct clusters, especially Setosa.

---

#### Pair Plot
A pairplot was generated to visualize all pairwise feature relationships.

**Observation:**  
Petal-related features provide strong species separation.

---

#### Histograms
Histograms were used to inspect feature distributions.

**Observation:**  
Petal measurements show clearer separation between species than sepal measurements.

---

#### Box Plots
Box plots were used to detect spread and possible outliers.

**Observation:**  
Some minor outliers exist, especially in sepal width.

---

#### Correlation Heatmap
A correlation matrix was visualized.

**Observation:**  
Petal length and petal width are highly positively correlated (> 0.96).

---

## Models Applied
No predictive models were applied in this task.

This task focused entirely on exploratory data analysis and visualization.

---

## Key Results and Findings

### Strong Feature Correlation
Petal length and petal width are strongly correlated.

### Clear Species Separation
Setosa is easily distinguishable from the other species.

### Useful Predictive Features
Petal-related measurements appear more useful for classification tasks.

### Minimal Outliers
The dataset is relatively clean and well-structured.

---

## Conclusion
The Iris dataset demonstrates clear separability among flower species, particularly using petal measurements.

Exploratory analysis revealed strong feature relationships and validated that this dataset is highly suitable for machine learning classification tasks.