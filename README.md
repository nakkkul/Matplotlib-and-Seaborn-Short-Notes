# Matplotlib and Seaborn Visualization in Python

## Introduction
Matplotlib is a powerful library for creating static, animated, and interactive visualizations in Python. It provides extensive control over graph properties, making it a great tool for detailed visual customization. Additionally, Seaborn is a high-level interface built on Matplotlib, offering beautiful and informative statistical graphics with simpler syntax.

## Types of Visualization Libraries in Python
1. **Matplotlib** - Low-level, highly customizable plotting library.
2. **Pandas Visualization** - Simplified interface built on Matplotlib.
3. **Seaborn** - High-level visualization with great default styles.
4. **ggplot** - Inspired by R's ggplot2, follows the Grammar of Graphics.
5. **Plotly** - Interactive visualization library.

## Features of Matplotlib
- Used for 2D and 3D plotting.
- Customizable styles and themes.
- Supports multiple graph types.

## Common Graphs in Matplotlib
- **Line Plot**
- **Bar Plot**
- **Scatter Plot**
- **Histogram**
- **Box Plot**
- **Pie Chart**
- **Stem and Step Plots**
- **Fill Between Plots**

## Example: Bar Plot
```python
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd

x = ['Python', 'C', 'C++', 'Java']
y = [85, 70, 60, 82]
c = ['g', 'm', 'b', 'r']

plt.bar(x, y, width=0.4, color=c, edgecolor='r', linewidth=2, alpha=0.6, label='Popularity')
plt.xlabel('Language', fontsize=10)
plt.ylabel('Number')
plt.title('Programming Language Popularity')
plt.legend()
plt.show()
```

## Example: Scatter Plot
```python
x = [1, 2, 3, 4, 5, 6, 7]
y = [2, 3, 1, 4, 5, 4, 6]
sizes = [10, 20, 40, 50, 20, 10, 70]

plt.scatter(x, y, s=sizes, marker='*')
plt.colorbar().set_label('Color Intensity')
plt.title('Scatter Plot Example', fontsize=10)
plt.show()
```

## Example: Histogram
```python
import random
x = np.random.randint(10, 60, 50)
plt.hist(x, bins=10, rwidth=0.8, bottom=10)
plt.show()
```

---

## Seaborn: Advanced Statistical Visualization
Seaborn enhances Matplotlib by offering aesthetically pleasing statistical plots with simpler syntax.

### Common Graph Types in Seaborn
- **Line Plot**
- **Heatmap**
- **Histogram**
- **Bar Plot**
- **Box Plot**
- **Violin Plot**
- **Scatter Plot**

### Example: Line Plot
```python
import seaborn as sns
import pandas as pd

var = [1, 2, 3, 4, 5, 6, 7]
var_1 = [2, 3, 4, 1, 5, 6, 7]
x_1 = pd.DataFrame({'var': var, 'var_1': var_1})

sns.lineplot(x='var', y='var_1', data=x_1)
plt.show()
```

### Example: Histogram in Seaborn
```python
sns.histplot(data=x_1, x='var', bins=[1, 2, 3, 4, 5, 6, 7])
plt.show()
```

### Example: Bar Plot
```python
df = sns.load_dataset('penguins')
sns.barplot(x='island', y='bill_length_mm', data=df, hue='sex')
plt.show()
```

## Conclusion
- **Matplotlib** offers a flexible way to create custom plots.
- **Seaborn** simplifies statistical visualization with great default themes.
- **Combining Matplotlib and Seaborn** can produce powerful and informative visualizations.

Experiment with different parameters and customization options to create insightful graphs!

