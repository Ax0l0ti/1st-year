# Python
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to.
> > *Date :* 22-06-2024
> > *Module :* 
> > *Teacher*: 
> > *Resources :* #Chatted

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Python Syntax]]
> [[#Data Structures]]
> [[#Object-Oriented Programming]]
> [[#Libraries and Frameworks]]
---
### Speed Run

> [!danger]+  Speed Run
> > $a)$ Python Syntax - Python syntax refers to the set of rules that define the structure of a Python program, including the use of indentation to define blocks of code.
> $b)$ Data Structures - Python data structures include lists, dictionaries, sets, and tuples, which are used to store collections of data.
> $c)$ Libraries and Frameworks - Python has a rich ecosystem of libraries and frameworks, such as NumPy for numerical computing, Pandas for data analysis, and Django for web development.
---

### Detailed Explanation

#### Python Syntax
Python syntax refers to the set of rules that define the structure of a Python program, including the use of indentation to define blocks of code.

#### Data Structures
Python data structures include lists, dictionaries, sets, and tuples, which are used to store collections of data.

### Python in Machine Learning (ML)

1. **Libraries**:
    
    - **NumPy**: For numerical operations.
    - **Pandas**: For data manipulation and analysis.
    - **Matplotlib/Seaborn**: For data visualization.
    - **Scikit-learn**: For classical ML algorithms.
    - **TensorFlow/PyTorch**: For deep learning.
2. **Example: Linear Regression with Scikit-learn**
    
```Python
import numpy as np from sklearn.model_selection 
import train_test_split from sklearn.linear_model import LinearRegression 
# Sample data 
X = np.array([[1], [2], [3], [4], [5]]) 
y = np.array([1, 3, 5, 7, 9])  
# Split data 
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)  
# Train model 
model = LinearRegression() model.fit(X_train, y_train)  
# Predict 
predictions = model.predict(X_test)`
```

### Python in Scientific Computing

1. **Libraries**:
    
    - **NumPy**: For array computing.
    - **SciPy**: For scientific and technical computing.
    - **Matplotlib**: For plotting and visualization.
    - **SymPy**: For symbolic mathematics.
    
1. **Example: Numerical Integration with SciPy**

```python
import numpy as np from scipy.integrate import quad  
# Define function to integrate 
def integrand(x):     
	return np.sin(x)  
# Integrate from 0 to pi result, 
error = quad(integrand, 0, np.pi)  
print(f"Integral result: {result}")
```
 

Python's syntax is straightforward, making it ideal for rapid development in machine learning and scientific computing. Its vast ecosystem of libraries supports various tasks, from basic data manipulation to complex machine learning models and scientific computations.

#### Libraries and Frameworks
Python has a rich ecosystem of libraries and frameworks, such as NumPy for numerical computing, Pandas for data analysis, and Django for web development.

---
