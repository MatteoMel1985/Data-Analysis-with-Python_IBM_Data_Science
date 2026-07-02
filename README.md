![Skills_Network](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMSkillsNetwork-PY0221EN-Coursera/images/image.png)  

<h1 align="center">IBM Data Analysis with Python</h1>

This repository contains a structured collection of Jupyter Notebooks developed while working through the IBM **Data Analysis with Python** learning path. The notebooks demonstrate the complete analytical workflow: importing datasets, cleaning and transforming raw data, exploring relationships between variables, building predictive regression models, and evaluating model performance.

The main notebook, **Exploratory Data Analysis – Cars**, is placed in the root folder as the central project file. The remaining notebooks are organised inside the `Jupyter Notebooks` folder as supporting labs and practice exercises.

<h1 align="center"><i>Repository Structure</i></h1>

```text
.
├── Exploratory_data_analysis_cars.ipynb
├── README.md
└── Jupyter Notebooks/
    ├── DA0101EN-Review-Introduction.ipynb
    ├── DA0101EN-2-Review-Data-Wrangling.ipynb
    ├── DA0101EN-4-Review-Model-Development.ipynb
    ├── House_Sales_in_King_Count_USA(1).ipynb
    ├── Model_Evaluation_and_Refinement_cars.ipynb
    ├── Practice_data_loading.ipynb
    ├── practice_data_wrangling.ipynb
    ├── parctice_Exploratory_data_analysis.ipynb
    ├── practice_model_development_laptops.ipynb
    └── practice_model_evaluation.ipynb
```

<h1 align="center"><i>Notebooks Overview</i></h1>

* [**Exploratory Data Analysis – Cars**](Exploratory_data_analysis_cars.ipynb)

This is the main notebook of the repository. It analyses an automobile dataset to identify the variables that most strongly influence car prices. The notebook applies descriptive statistics, visual exploration, grouping, pivot tables, correlation analysis, Pearson correlation tests, and ANOVA to study relationships between car features and price.

* [**Introduction to Data Analysis with Python**](Jupyter%20Notebooks/DA0101EN-Review-Introduction.ipynb)

This notebook introduces the first stage of the data analysis workflow: importing data into pandas. It covers reading CSV files, assigning meaningful column headers, replacing missing-value placeholders, saving datasets, inspecting data types, and generating basic descriptive summaries.

* [**Data Wrangling – Cars Dataset**](Jupyter%20Notebooks/DA0101EN-2-Review-Data-Wrangling.ipynb)

This notebook focuses on transforming raw automobile data into a clean and analysis-ready format. It includes identifying missing values, replacing missing numerical values with the mean, handling categorical missing values, correcting data types, standardising units, normalising numerical variables, binning continuous data, and creating indicator variables.

* [**Model Development – Cars Dataset**](Jupyter%20Notebooks/DA0101EN-4-Review-Model-Development.ipynb)

This notebook introduces predictive modelling for car prices. It develops and compares simple linear regression, multiple linear regression, polynomial regression, and pipeline-based models. It also uses visual evaluation methods such as regression plots, residual plots, and distribution plots, together with numerical metrics such as R-squared and mean squared error.

* [**Model Evaluation and Refinement – Cars Dataset**](Jupyter%20Notebooks/Model_Evaluation_and_Refinement_cars.ipynb)

This notebook extends the modelling workflow by focusing on model validation and refinement. It covers training and testing splits, cross-validation, overfitting and underfitting, polynomial model selection, Ridge Regression, and Grid Search for hyperparameter tuning.

* [**House Sales in King County, USA**](Jupyter%20Notebooks/House_Sales_in_King_Count_USA(1).ipynb)

This final project applies the full data analysis workflow to housing prices in King County, USA. It includes data loading, data wrangling, exploratory analysis, correlation study, feature-based price prediction, linear regression, multiple regression, polynomial transformation, Ridge Regression, pipelines, train-test splitting, and cross-validation.

* [**Practice Lab – Data Loading: Laptops Dataset**](Jupyter%20Notebooks/Practice_data_loading.ipynb)

This practice notebook introduces dataset acquisition and first inspection using a laptop pricing dataset. It covers loading data into a pandas DataFrame, assigning headers, replacing missing-value symbols with `NaN`, inspecting data types, generating statistical summaries, and reviewing general dataset information.

* [**Practice Lab – Data Wrangling: Laptops Dataset**](Jupyter%20Notebooks/practice_data_wrangling.ipynb)

This notebook applies data cleaning and transformation techniques to the laptop pricing dataset. It includes missing-value evaluation, mean and mode imputation, data type correction, unit standardisation, numerical normalisation, binning, and creation of dummy variables for categorical features.

* [**Practice Lab – Exploratory Data Analysis: Laptops Dataset**](Jupyter%20Notebooks/parctice_Exploratory_data_analysis.ipynb)

This notebook explores the laptop pricing dataset through visual and statistical analysis. It uses regression plots, boxplots, descriptive statistics, value counts, group-by operations, pivot tables, heatmaps, Pearson correlation coefficients, and p-values to identify relationships between laptop features and price.

* [**Practice Lab – Model Development: Laptops Dataset**](Jupyter%20Notebooks/practice_model_development_laptops.ipynb)

This notebook develops predictive models for laptop prices. It covers simple linear regression, multiple linear regression, polynomial regression, model pipelines, feature scaling, polynomial feature expansion, and model evaluation using R-squared and mean squared error.

* [**Practice Lab – Model Evaluation: Laptops Dataset**](Jupyter%20Notebooks/practice_model_evaluation.ipynb)

This notebook focuses on validating and refining laptop price prediction models. It introduces cross-validation, train-test splitting, overfitting analysis, Ridge Regression, and Grid Search to identify stronger and more stable predictive models.

<h1 align="center"><i>Technical Methodologies and Mathematical Foundations</i></h1>

## 1. Data Acquisition and Initial Inspection

The notebooks begin by importing structured datasets into pandas DataFrames. This stage includes assigning column names, checking dimensions, inspecting data types, and reviewing the first rows of the dataset. These operations are essential because predictive modelling depends on the correct interpretation of variables as numerical, categorical, ordinal, or textual data.

From a mathematical perspective, a dataset can be represented as a matrix:

$$
X = \begin{bmatrix}
x_{11} & x_{12} & \dots & x_{1p} \\
x_{21} & x_{22} & \dots & x_{2p} \\
\vdots & \vdots & \ddots & \vdots \\
x_{n1} & x_{n2} & \dots & x_{np}
\end{bmatrix}
$$

where each row represents an observation and each column represents a feature. In supervised learning tasks, the target variable, such as car price, laptop price, or house price, is represented as a vector:

$$
y = \begin{bmatrix} y_1 & y_2 & \dots & y_n \end{bmatrix}^T
$$

## 2. Data Cleaning and Missing-Value Treatment

The data wrangling notebooks show how to identify and handle missing values. Missing numerical values are commonly replaced with the mean of the available observations:

$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n}x_i
$$

For categorical variables, missing values can be replaced with the most frequent category, also known as the mode. These techniques help preserve the size of the dataset while reducing the risk of errors during analysis and modelling.

## 3. Data Standardisation and Normalisation

Several notebooks apply unit conversion, standardisation, and normalisation. Unit standardisation ensures that measurements are expressed consistently, such as converting fuel consumption, weight, or screen size into the desired unit.

Normalisation rescales numerical variables so they become easier to compare. A common min-max transformation is:

$$
x' = \frac{x - x_{min}}{x_{max} - x_{min}}
$$

The modelling notebooks also use standardisation through `StandardScaler`, which transforms a variable into a distribution centred around zero with unit variance:

$$
z = \frac{x - \mu}{\sigma}
$$

where $\mu$ is the mean and $\sigma$ is the standard deviation. This is especially useful when models use polynomial features or regularisation.

## 4. Binning and Indicator Variables

Binning converts continuous variables into categorical intervals. For example, horsepower, screen size, or price-related variables can be grouped into levels such as low, medium, and high. This simplifies interpretation and can reveal non-linear patterns.

Categorical variables are also transformed into numerical indicator variables using one-hot encoding. For a categorical feature with $k$ possible categories, one-hot encoding creates $k$ binary variables, where each variable takes the value 1 if the observation belongs to that category and 0 otherwise.

## 5. Exploratory Data Analysis

The EDA notebooks use descriptive statistics, visualisation, grouping, and pivot tables to understand how individual features relate to price. Boxplots are used to compare price distributions across categories, scatterplots and regression plots are used to inspect relationships between continuous variables, and heatmaps are used to visualise correlation matrices.

The Pearson correlation coefficient measures the strength and direction of a linear relationship between two variables:

$$
r = \frac{\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n}(x_i - \bar{x})^2}\sqrt{\sum_{i=1}^{n}(y_i - \bar{y})^2}}
$$

A value close to 1 indicates a strong positive linear relationship, a value close to -1 indicates a strong negative linear relationship, and a value close to 0 indicates a weak linear relationship.

The notebooks also use p-values to evaluate whether an observed relationship is statistically meaningful. In general, a smaller p-value suggests stronger evidence against the null hypothesis that no relationship exists.

## 6. ANOVA for Categorical Feature Analysis

The car EDA notebook uses ANOVA to compare the average price across different categorical groups. ANOVA evaluates whether the variation between group means is large relative to the variation within the groups.

The F-statistic can be expressed conceptually as:

$$
F = \frac{\text{variance between groups}}{\text{variance within groups}}
$$

A larger F-statistic suggests that the categorical variable may have a stronger relationship with the target variable. In the automobile analysis, this helps evaluate whether features such as drive wheels or body style meaningfully affect car prices.

## 7. Simple Linear Regression

Simple Linear Regression models the relationship between one independent variable and one target variable. The model has the form:

$$
\hat{y} = b_0 + b_1x
$$

where $\hat{y}$ is the predicted value, $b_0$ is the intercept, $b_1$ is the slope, and $x$ is the input feature. The model estimates the line that minimises the sum of squared errors between the actual and predicted values:

$$
RSS = \sum_{i=1}^{n}(y_i - \hat{y}_i)^2
$$

In the notebooks, this technique is used to test whether individual variables, such as highway miles per gallon or engine size, can predict price.

## 8. Multiple Linear Regression

Multiple Linear Regression extends linear regression by using several input variables at once:

$$
\hat{y} = b_0 + b_1x_1 + b_2x_2 + \dots + b_px_p
$$

In matrix form, this can be written as:

$$
\hat{y} = X\beta
$$

where $X$ is the feature matrix and $\beta$ is the vector of model coefficients. This method is used when price depends on multiple characteristics simultaneously, such as horsepower, curb weight, engine size, and fuel economy.

## 9. Polynomial Regression

Polynomial Regression allows the model to capture curved relationships between features and the target variable. A second-degree polynomial model has the form:

$$
\hat{y} = b_0 + b_1x + b_2x^2
$$

A higher-degree polynomial can capture more complex patterns, but it may also overfit the training data. The notebooks therefore compare different polynomial degrees and inspect the resulting model behaviour.

Although polynomial regression creates non-linear curves, it is still linear in the model parameters. This means the model can still be estimated using linear regression after expanding the original features into polynomial terms.

## 10. Pipelines

The notebooks use scikit-learn pipelines to combine multiple modelling steps into a single workflow. A typical pipeline may include standardisation, polynomial feature generation, and linear regression:

```python
Input Data → StandardScaler → PolynomialFeatures → LinearRegression → Prediction
```

Pipelines make modelling workflows cleaner, more reproducible, and less prone to mistakes, especially when the same transformations must be applied consistently to training and testing data.

## 11. Model Evaluation Metrics

The modelling notebooks evaluate predictions using metrics such as Mean Squared Error and R-squared.

Mean Squared Error measures the average squared difference between actual and predicted values:

$$
MSE = \frac{1}{n}\sum_{i=1}^{n}(y_i - \hat{y}_i)^2
$$

A lower MSE indicates that the model's predictions are closer to the actual values.

R-squared measures the proportion of variance in the target variable explained by the model:

$$
R^2 = 1 - \frac{\sum_{i=1}^{n}(y_i - \hat{y}_i)^2}{\sum_{i=1}^{n}(y_i - \bar{y})^2}
$$

A higher R-squared value generally indicates a better fit, although it must be interpreted carefully because a very complex model can achieve a high score by overfitting.

## 12. Training, Testing, and Cross-Validation

The model evaluation notebooks split data into training and testing sets. The training set is used to fit the model, while the testing set is used to estimate how well the model generalises to unseen data.

Cross-validation improves this process by dividing the dataset into several folds. The model is trained on some folds and tested on the remaining fold, rotating the test fold each time. The final score is usually the average across all folds:

$$
CV = \frac{1}{k}\sum_{i=1}^{k} score_i
$$

This gives a more reliable estimate of model performance than a single train-test split.

## 13. Overfitting and Underfitting

The notebooks examine the balance between overfitting and underfitting. Underfitting occurs when a model is too simple to capture the underlying pattern in the data. Overfitting occurs when a model is too complex and starts learning random noise instead of the general relationship.

Polynomial models are especially useful for demonstrating this trade-off: low-degree models may underfit, while high-degree models may overfit. The goal is to find a model that performs well both on training data and unseen testing data.

## 14. Ridge Regression

Ridge Regression is a regularised version of linear regression. It adds a penalty term to reduce the size of the coefficients and control overfitting:

$$
J(\beta) = \sum_{i=1}^{n}(y_i - \hat{y}_i)^2 + \alpha\sum_{j=1}^{p}\beta_j^2
$$

The parameter $\alpha$ controls the strength of the penalty. When $\alpha = 0$, Ridge Regression behaves like ordinary linear regression. As $\alpha$ increases, the coefficients are shrunk more strongly, which can improve generalisation when the model is too flexible.

## 15. Grid Search

Grid Search is used to test multiple hyperparameter values and select the best-performing model configuration. In these notebooks, it is mainly used to find an appropriate value of $\alpha$ for Ridge Regression.

Mathematically, Grid Search evaluates a set of candidate values:

$$
\alpha \in \{\alpha_1, \alpha_2, \dots, \alpha_m\}
$$

and selects the value that produces the best validation performance. When combined with cross-validation, Grid Search provides a systematic way to tune models and reduce arbitrary parameter selection.

<h1 align="center"><i>Skills Demonstrated</i></h1>

* Importing and inspecting datasets with pandas.
* Cleaning missing, inconsistent, and incorrectly typed data.
* Performing unit conversion, normalisation, binning, and one-hot encoding.
* Analysing numerical and categorical variables through visualisation.
* Using correlation, p-values, and ANOVA to evaluate feature relevance.
* Building simple, multiple, and polynomial regression models.
* Creating modelling pipelines with scikit-learn.
* Evaluating models using R-squared, MSE, train-test splits, and cross-validation.
* Reducing overfitting through Ridge Regression and hyperparameter tuning.
* Applying the full data analysis workflow to automobile, laptop, and housing datasets.

<h1 align="center"><i>Technologies Used</i></h1>

* Python
* Jupyter Notebook / JupyterLab
* pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* scikit-learn

# Author
# ***[Matteo Meloni](https://www.linkedin.com/in/matteo-meloni-40a357154/)***
