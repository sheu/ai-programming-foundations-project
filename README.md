# AI Programming Foundations Project

A project for Udacity's **AI Programming with Python Nanodegree**.  
This repository demonstrates a complete, **reproducible data workflow** using Python's core  
data-science stack — no machine-learning models yet.  It builds the foundation that later  
ML, Deep Learning, Generative AI, and Agentic AI projects will build upon.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Workflow Steps](#workflow-steps)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Notebook](#running-the-notebook)
- [Technologies Used](#technologies-used)
- [References](#references)
- [License](#license)

---

## Project Overview

`data_workflow.ipynb` loads a synthetically generated dataset of **urban quality-of-life  
indicators** for 20 cities across four geographic regions over six years (2018–2023), then  
cleans, transforms, explores, and visualizes it in a reproducible notebook.

The synthetic dataset was chosen so the project runs end-to-end without any external  
downloads, making it trivially reproducible on any machine — a practice recommended by  
Wilson et al. (2017).

---

## Workflow Steps

| Step | Description |
|---|---|
| **1 — Setup** | Import libraries; fix `RANDOM_SEED = 42` for full reproducibility |
| **2 — Data generation** | Create a 120-row dataset (20 cities × 6 years) with NumPy |
| **3 — Data inspection** | `.info()`, `.describe()`, dtype audit |
| **4 — Data cleaning** | Cap AQI outlier; regional-median imputation; correct dtypes |
| **5 — Feature engineering** | Composite `wellbeing_score`; ordinal `income_bracket` |
| **6 — EDA** | Summary statistics; Pearson correlation matrix |
| **7 — Visualization** | Distributions, boxplots, heatmap, scatter + OLS trend, time series |
| **8 — Key findings** | Narrative summary of five major insights |
| **9 — References** | Two scholarly sources + Jupyter citation |

---

## Project Structure

```
ai-programming-foundations-project/
├── data_workflow.ipynb   # Main notebook (load → clean → explore → visualize → communicate)
├── requirements.txt      # Python dependencies
└── README.md
```

---

## Prerequisites

- Python 3.9+  (uses `numpy.random.default_rng`, available since Python 3.9 / NumPy 1.17)

---

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/sheu/ai-programming-foundations-project.git
   cd ai-programming-foundations-project
   ```

2. **Create and activate a virtual environment** (recommended)

   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

---

## Running the Notebook

```bash
jupyter notebook data_workflow.ipynb
```

or, to execute non-interactively and verify reproducibility:

```bash
jupyter nbconvert --to notebook --execute --inplace data_workflow.ipynb
```

Every cell output is deterministic because all random operations use `RANDOM_SEED = 42`.

---

## Technologies Used

| Tool | Purpose |
|---|---|
| **Python 3** | Core language |
| **NumPy** | Synthetic data generation; numerical operations |
| **pandas** | DataFrame manipulation, cleaning, groupby EDA |
| **Matplotlib** | Base charting and axis formatting |
| **Seaborn** | Statistical visualizations (histplot, boxplot, heatmap) |
| **Jupyter Notebook** | Literate-programming environment |
| **Git & GitHub** | Version control and collaboration |

---

## References

1. Wilson, G., Bryan, J., Cranston, K., Kitzes, J., Nederbragt, L., & Teal, T. K. (2017).
   Good enough practices in scientific computing.
   *PLOS Computational Biology*, 13(6), e1005510.
   <https://doi.org/10.1371/journal.pcbi.1005510>

2. Wickham, H. (2014). Tidy data.
   *Journal of Statistical Software*, 59(10), 1–23.
   <https://doi.org/10.18637/jss.v059.i10>

---

## License

This project is submitted as part of the Udacity AI Programming with Python Nanodegree.  
Code and assets follow the [Udacity Honor Code](https://udacity.com/legal/community-guidelines).
