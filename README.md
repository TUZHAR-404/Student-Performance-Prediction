# Student Performance Prediction

[Project Overview](#project-overview) • [Objective](#objective) • [Process](#process) • [Tools Used](#tools-used) • [Analysis / Procedure](#analysis--procedure) • [Outcomes](#outcomes) • [Learning and Difficulties](#learning-and-difficulties) • [Future Aspects](#future-aspects)

---

## Project Overview

This project predicts a student's performance score using a small machine learning workflow built in Python. It starts with a synthetic student dataset and uses features such as study hours, attendance, assignments completed, and sleep hours to estimate performance.

<details>
<summary>What this project demonstrates</summary>

- Data creation and exploration
- Feature selection and preprocessing
- Model training with a pipeline
- Cross-validation for more reliable evaluation
- Prediction for a new student profile

</details>

## Objective

The objective of the project is to build a simple but more advanced prediction system that can estimate academic performance from student behavior and study habits.

<details>
<summary>Primary goals</summary>

- Understand which factors influence performance
- Compare training and cross-validated results
- Produce a reusable prediction workflow
- Show the result clearly in a notebook and README

</details>

## Process

```mermaid
flowchart LR
    A[Create dataset] --> B[Explore data]
    B --> C[Select features]
    C --> D[Train-test split]
    D --> E[Pipeline: PolynomialFeatures + StandardScaler + Ridge]
    E --> F[Cross-validation]
    F --> G[Evaluate results]
    G --> H[Predict new student score]
```

<details>
<summary>Step-by-step workflow</summary>

1. A student dataset is created with academic and lifestyle features.
2. The target variable, performance score, is generated from the input features.
3. The dataset is split into training and testing subsets.
4. A machine learning pipeline is built with polynomial feature expansion, scaling, and Ridge regression.
5. Five-fold cross-validation is used to check how stable the model is.
6. The model is evaluated on the holdout test set.
7. A new student profile is passed into the model to generate a predicted score.

</details>

## Tools Used

<details>
<summary>Development tools</summary>

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- scikit-learn

</details>

<details>
<summary>Machine learning methods</summary>

- Train/test split
- Polynomial feature engineering
- Standardization
- Ridge regression
- K-fold cross-validation
- Evaluation using MAE and R-squared

</details>

## Analysis / Procedure

The notebook follows a clear ML pipeline:

1. Create a dataset with student-related inputs.
2. Visualize the relationship between study hours and performance.
3. Train a regression model using a pipeline.
4. Measure performance with cross-validation and holdout testing.
5. Predict the score for a new student.

### Screenshots

<table>
    <tr>
        <td align="center">
            <strong>Dataset Preview</strong><br>
            <img src="Screenshot%202026-08-04%20171913.png" alt="Dataset preview table" width="320">
        </td>
        <td align="center">
            <strong>Study Hours vs Performance</strong><br>
            <img src="Screenshot%202026-08-04%20171924.png" alt="Scatter plot of study hours versus performance score" width="320">
        </td>
    </tr>
    <tr>
        <td align="center">
            <strong>Model Evaluation</strong><br>
            <img src="Screenshot%202026-08-04%20171932.png" alt="Cross-validated and holdout performance metrics" width="320">
        </td>
        <td align="center">
            <strong>Final Prediction</strong><br>
            <img src="Screenshot%202026-08-04%20171941.png" alt="Predicted score and final dataset output" width="320">
        </td>
    </tr>
</table>

<details>
<summary>Why the model is more advanced now</summary>

Instead of a plain linear regression baseline, the notebook now uses a pipeline with:

- PolynomialFeatures to capture non-linear patterns
- StandardScaler to normalize feature values
- Ridge regression to reduce overfitting
- KFold cross-validation for better evaluation

</details>

## Outcomes

The notebook now produces:

- A trained prediction model
- Cross-validated MAE and R-squared values
- Holdout test-set metrics
- A score prediction for a new student

<details>
<summary>Example result</summary>

The upgraded pipeline returns a strong fit on the small synthetic dataset and generates a predicted performance score for the sample student profile.

</details>

## Learning and Difficulties

<details>
<summary>What I learned</summary>

- How to structure a full ML notebook from data creation to prediction
- How preprocessing improves model quality
- How cross-validation gives a better estimate than a single train/test split
- How to package the workflow with a pipeline

</details>

<details>
<summary>Challenges faced</summary>

- Keeping the notebook organized while adding more advanced steps
- Making sure the pipeline still worked with the prediction cell
- Interpreting evaluation metrics on a very small dataset
- Formatting the README so it is clear and presentation-ready

</details>

## Future Aspects

<details>
<summary>Possible improvements</summary>

- Use a real student dataset instead of synthetic data
- Add more features such as exam history, participation, and parent support
- Compare multiple models such as Random Forest, SVR, and XGBoost
- Save the trained model for reuse
- Build a simple web app for live predictions
- Add screenshots and charts directly into the README

</details>

---

## Quick Summary

This project predicts student performance using a more advanced regression workflow and presents the process in a simple, readable format for both README and presentation use.
