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

## How This Project Connects to Future AI Work

### ML Workflow Changes
This project focuses on reproducible data ingestion, cleaning, exploratory analysis, and visualization. If extended into a machine learning project, the workflow would shift from descriptive analysis to predictive modeling. That would require defining a target variable, selecting input features, splitting the data into training, validation, and test sets, encoding categorical variables, handling potential data leakage, and evaluating performance using appropriate metrics such as accuracy, precision, recall, and F1-score.

### Neural Network Preparation
To prepare this dataset for a neural network, additional preprocessing would be required. All input variables would need to be converted into numeric form, categorical columns would need encoding, and continuous features would likely need scaling or normalization. Missing values would need to be handled carefully because placeholder values such as `-1` may distort learning. The cleaned data would then need to be transformed into tensor-ready arrays for use in frameworks such as TensorFlow or PyTorch.

### Agentic Automation Potential
This workflow also creates a foundation for future agentic automation. An automated system could ingest new data files, validate schema consistency, apply cleaning rules, regenerate summary statistics and visualizations, and produce updated reports without manual repetition. A more advanced agentic workflow could monitor data quality issues, detect unusual changes in distributions, and recommend updates to the preprocessing pipeline when new data differs from previous versions.