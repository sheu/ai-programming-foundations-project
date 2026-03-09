# ai-programming-foundations-project

# Data Analysis Workflow Project

## Project Description
This project demonstrates a complete and reproducible data analysis workflow using Python and Jupyter Notebook. It includes loading a real dataset, cleaning and transforming the data, performing exploratory data analysis, and summarizing findings in a structured way. The project is designed as a foundation for future machine learning and AI workflows.

## What I Built
I built a reproducible data workflow in `data_analysis_workflow.ipynb` that:
- loads the dataset
- cleans and transforms the data
- performs exploratory data analysis
- generates summary statistics, grouped views, and correlation checks
- documents findings clearly in notebook format

## Dataset Used
- **Dataset Name:** Titanic - Machine Learning from Disaster
- **Source:** [Kaggle Titanic Dataset](https://www.kaggle.com/competitions/titanic/data)

## How to Run the Project

### 1. Clone the repository
```bash
git clone <your-repository-url>
cd <your-repository-folder>
```
### 2. Create and activate a virtual environment
#### macOS / Linux
```bash 
python3 -m venv .venv
source .venv/bin/activate
```
#### Windows
```bash 
python -m venv .venv
.venv\Scripts\activate
```
### 3. Install dependencies
```bash
pip install -r requirements.txt
```
To save the dependencies you used to run the project
```bash
pip freeze > requirements.txt
```
### 4. Open and run the notebook

#### Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

`data_analysis_workflow.ipynb`

Run the notebook cells from top to bottom.

### Bias awareness
The clearest risk in this notebook is the handling of missing ages: filling missing `Age` values with `-1` preserves a numeric column but introduces an artificial value that lowers the mean age and can distort correlations, distributions, and any downstream interpretation of passenger age. 

## Future Integration: ML, Deep Learning & Agentic Workflows

### ML Workflow Changes

If this workflow were integrated into a machine learning pipeline, several modifications would be required. The cleaning functions would need to output feature matrices compatible with machine learning libraries such as **scikit-learn**, ensuring that all features are numeric and contain no missing values. The placeholder age imputation using `-1` would likely be replaced with more robust strategies such as **median imputation**, **group-based imputation**, or **model-based imputation**. Categorical variables such as `Sex` and `Embarked` would also need to be encoded using techniques such as **one-hot encoding** or **label encoding**. In addition, the dataset would need to be split into **training**, **validation**, and **test sets**, and feature selection would be performed to identify the most predictive variables.

### Neural Network Preparation

Preparing this dataset for a neural network would require additional preprocessing steps. Neural networks require numeric inputs on similar scales, so continuous features such as `Fare` and `Age` would likely need to be **normalized or standardized** using tools like `StandardScaler` or `MinMaxScaler`. Categorical variables such as `Sex` and `Embarked` would need to be converted into numerical representations using **one-hot encoding** or **learned embeddings**. Missing data would need to be handled more carefully because placeholder values such as `-1` could negatively affect network training. After preprocessing, the cleaned dataset would be converted into **tensor-ready arrays** suitable for frameworks such as **PyTorch** or **TensorFlow**.

### Agentic Automation Potential

Several stages of this workflow could benefit from automation through **AI agents** or intelligent pipelines. For example, an AI agent could automatically perform **exploratory data analysis (EDA)**, identifying statistical patterns, correlations, or anomalies in the dataset. Agents could also monitor incoming datasets for **data quality issues**, such as missing values, schema changes, or unusual distributions. In a more advanced system, agents could assist with **model selection**, **hyperparameter tuning**, and **automated report generation**, producing updated visualizations and summaries whenever new data is ingested. This type of **agent-assisted workflow** would reduce manual analysis time and help maintain consistent data quality and documentation.

### Professional and Reusable Workflow Design

This project was structured as a **reusable data workflow** rather than a one-time analysis notebook. The workflow separates **data ingestion**, **cleaning**, **exploratory analysis**, **visualization**, and **interpretation** into clear stages. Reusable helper functions were implemented to simplify repeated operations such as generating **summary statistics**, **grouping data**, and **checking correlations**. This modular design improves **maintainability**, encourages **reproducibility**, and provides a clean starting point for future **machine learning** and **deep learning** projects.