# Housing Price Prediction Using Machine Learning
This project focuses on predicting house sale prices using machine learning techniques. Housing datasets typically contain a mix of numerical and categorical features that describe various characteristics of a property, such as area, number of rooms, quality rating, location, and more. By learning patterns from this data, machine learning models can forecast the value of a house with considerable accuracy.

## 📘 Introduction

House price prediction is a regression task where the goal is to estimate a continuous numerical value (Sale Price). Machine Learning helps identify complex relationships between house attributes and their market value, allowing both buyers and sellers to make informed decisions.

This project uses **data preprocessing, exploratory data analysis (EDA), encoding techniques, scaling, and regression algorithms** to build a robust predictive system.

## 🎯 Objective

- Understand dataset features

- Analyze relationships between variables

- Handle missing values

- Convert categorical information into numerical format

- Normalize numerical values

- Train multiple machine learning algorithms

- Compare their performance

- Identify the best model for price prediction

## 📂 Dataset

**The dataset used:**
📄 HousePricePrediction.xlsx

**Contains columns such as:**

- Lot area

- Ground living area

- Overall quality

- Garage info

- Year built

- Number of rooms

- SalePrice (target)

## 🔍 Understanding the Steps
### 📍 1. Data Cleaning & Missing Values

Real-world housing datasets often contain missing values.
We handle them by:

- Removing rows where the target value is missing

- Replacing missing numerical values using median

- Replacing missing categorical values using the most frequent category

This ensures the dataset is consistent and ready for analysis.

### 📍 2. Exploratory Data Analysis (EDA)

EDA helps understand the distribution of features and their relationships with the target.

#### Correlation Heatmap

Shows how strongly numerical features relate to each other and to Sale Price.
For example:

- Higher living area correlates strongly with higher price

- Overall quality often has the strongest positive correlation

- Features like year built or garage area may also influence price

#### Categorical Feature Analysis

Counting unique categories helps determine:

- How many labels exist

- Which features have high cardinality
Features with too many categories may need more careful encoding.

## ⚙️ Preprocessing Techniques Used
### 📍 1. Encoding Categorical Data

Since ML algorithms cannot understand text labels, categorical data is converted into numerical form using:

#### One-Hot Encoding

Creates a binary column for each category.
Example:
RoofStyle = ['Gable', 'Hip'] becomes:

RoofStyle_Gable: 0/1

RoofStyle_Hip: 0/1

This helps the model learn patterns without imposing false ordering.

### 📍 2. Scaling Numerical Features

Different features have different ranges (e.g., area vs. number of rooms).
Scaling brings them onto a similar scale, improving model performance.

#### Standard Scaling

- Converts data so that mean = 0 and variance = 1

- Prevents large-valued features from dominating the model

## 🤖 Machine Learning Models Used

The project evaluates multiple regression algorithms:

### 1️⃣ Linear Regression

A simple and fast algorithm that assumes a linear relationship between features and the price.

#### Strengths

- Easy to interpret

- Good baseline model

#### Limitations

- Cannot learn non-linear relationships

- Sensitive to outliers

### 2️⃣ Decision Tree Regressor

A non-linear model that splits the dataset based on feature values.

#### Strengths

- Captures complex relationships

- Works well on mixed data types

- Easy to visualize

#### Limitations

- Can overfit

- Sensitive to noise in data

### 3️⃣ Random Forest Regressor

An ensemble of multiple decision trees.

#### Strengths

- More stable than a single tree

- Reduces overfitting

- Handles non-linearity well

#### Limitations

- Less interpretable

- Training time increases with data size

### 4️⃣ Gradient Boosting Regressor

A powerful boosting algorithm that builds trees sequentially, each correcting errors from the previous one.

#### Strengths

- High predictive accuracy

- Learns patterns missed by earlier models

- Often performs best on structured/tabular data

#### Limitations

- More complex

- Training time is higher

## 🧮 Model Comparison Summary

Based on the MAE, MSE, and R² metrics:

- Linear Regression → Moderate performance

- Decision Tree → Improved performance but risk of overfitting

- Random Forest → Strong performance

- Gradient Boosting → ⭐ Best overall performance

Gradient Boosting shows the highest accuracy and best generalization.

## 📊 Visual Outputs
### 1️⃣ Feature Importance Plot

Shows which features contribute most to price prediction.
Examples of highly influential features:

- Overall quality

- Living area

- Garage area

- Number of rooms

### 2️⃣ Actual vs Predicted Plot

Shows model accuracy visually.
The closer the points lie to the diagonal line, the more accurate the predictions.

## 📁 Project Structure

├── House_Price_Prediction.ipynb  

├── HousePricePrediction.xlsx  

├── feature_importance.png  

├── actual_vs_predicted.png  

└── README.md

## 🔮 Future Improvements

- Add more advanced models like XGBoost or LightGBM

- Improve accuracy using hyperparameter tuning

- Create new features to capture more patterns

- Remove outliers to make predictions more stable

- Build a simple web app for user-friendly predictions

- Deploy the model online for real-time use

- Use cross-validation for more reliable results

- Add better visualizations to understand trends

## 🏁 Conclusion

This project demonstrates how machine learning can be effectively used to predict house prices. Gradient Boosting emerged as the best-performing model, showing that ensemble techniques often provide superior accuracy on structured data.

## 👩‍💻 Author

Madhavi Thatha

## 🤝 Need Help or Want to Contribute?

If anyone needs help understanding this project or wants guidance on improving it, feel free to reach out anytime — I’m happy to help!

### 💡 Contributions

Contributions, suggestions, and improvements are always welcome.

I will review and merge PRs that add value to the project.

## 📜 License

MIT License
