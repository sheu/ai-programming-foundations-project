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