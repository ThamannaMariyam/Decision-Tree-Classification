#  Decision Tree Classification

This project demonstrates a simple **Decision Tree Classifier** built using the `scikit-learn` library in Python. It predicts whether a person should "Go" based on features like Age, Experience, Rank, and Nationality using data from a `drama.csv` file.

---

##  Dataset Overview

The dataset contains the following columns:

- **Age**: Age of the person  
- **Experience**: Years of experience  
- **Rank**: Job or status rank  
- **Nationality**: Categorical (UK, USA, N)  
- **Go**: Target variable (YES/NO)

The categorical columns `Nationality` and `Go` are mapped to numerical values for model training:
- Nationality: {'UK': 0, 'USA': 1, 'N': 2}  
- Go: {'YES': 1, 'NO': 0}

---

##  Project Workflow

### 1. Data Preparation
- Run CSV file using `pandas`
- Mapped categorical values to numerical using `dict` and `map()`
- features: `['Age', 'Experience', 'Rank', 'Nationality']`
- Target variable: `Go`

### 2. Model Training
- Used `DecisionTreeClassifier` from `scikit-learn`
- Trained the model on the entire dataset
- Visualized the decision tree using `tree.plot_tree()`

### 3. Prediction
- Created a new sample input:
  ```python
  input_data = [[40, 10, 6, 1]]  # Age, Experience, Rank, Nationality (USA)
- Used the trained model to predict whether the person should "Go"
- Output is interpreted and printed as either "Go" or "No"

##  Sample Output

- Prediction: 1 (Go)
