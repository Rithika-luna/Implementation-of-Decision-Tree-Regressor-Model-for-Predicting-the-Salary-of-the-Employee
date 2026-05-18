# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:

1. Hardware – PCs
 
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm


1. Import the required libraries and load the employee salary dataset using Pandas.
2. 
3. Preprocess the dataset by separating input features and target salary values, and convert categorical data into numerical format.
4. 
5. Create and train the Decision Tree Regressor model using the dataset.
6. 
7. Predict the employee salary using the trained model and display the performance metrics and decision tree visualization.

## Program:
```
/*



Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S Rithika
RegisterNumber:  212225040344
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor, plot_tree
from sklearn.metrics import accuracy_score, classification_report
data = pd.read_csv("Salary.csv")
X = data.drop("Salary", axis=1)
y = data["Salary"]
X = pd.get_dummies(X, drop_first=True)
#X_train, X_test, y_train, y_test = train_test_split(    X, y, test_size=0.2, random_state=42)
model = DecisionTreeRegressor(random_state=42)
model.fit(X, y)
y_pred = model.predict(X)
# Accuracy
print("\nAccuracy:", accuracy_score(y, y_pred)*100)

# Classification Report
print("\nClassification Report:")
print(classification_report(y, y_pred))

plt.figure(figsize=(25,12))
plot_tree(
    model,
    feature_names=X.columns,
    filled=True
)

plt.title("Decision Tree Regressor")
plt.show()
*/



```



## Output:
<img width="1847" height="612" alt="image" src="https://github.com/user-attachments/assets/aa9bc830-bf5b-452e-815e-bf360cd005e4" />
<img width="1828" height="846" alt="image" src="https://github.com/user-attachments/assets/0920c21c-829e-4a39-873e-d47f258b23ee" />




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
