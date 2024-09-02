# Overview
Welcome to my analysis of the data job market, focusing on data analyst roles. This project was created out of a desire to navigate and understand the job market more effectively. It delves into the top-paying and in-demand skills to help find optimal job opportunities for data analysts.

# Technology Used
 **Python**: The backbone of my analysis, allowing me to analyze the data and find critical insights.I also used the following Python libraries:
        `**Pandas Library:** This was used to analyze the data.  
        `**Matplotlib Library:** I visualized the data.  
        `**Seaborn Library:** Helped me create more advanced visuals.  
    **Jupyter Notebooks:** The tool I used to run my Python scripts which let me easily include my notes and analysis.  
    **Visual Studio Code:** My go-to for executing my Python scripts.  
    **Git & GitHub:** Essential for version control and sharing my Python code and analysis, ensuring collaboration and project tracking.
 
# Data Preparation and Cleanup
```python
# Importing Libraries
import ast
import pandas as pd
import seaborn as sns
from datasets import load_dataset
import matplotlib.pyplot as plt  

# Loading Data
dataset = load_dataset('lukebarousse/data_jobs')
df = dataset['train'].to_pandas()

# Data Cleanup
df['job_posted_date'] = pd.to_datetime(df['job_posted_date'])
df['job_skills'] = df['job_skills'].apply(lambda x: ast.literal_eval(x) if pd.notna(x)
