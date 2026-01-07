# Python project
## overview
Hi, here you can see some of my work while learning python (and other necessary hard skills for data analysis in Python)

## The Questions

Below are the questions I want to answer in my project:

1. [What are the skills most in demand for the top 3 most popular data roles?](project_cv\2_skill_demand.ipynb)
2. [How are in-demand skills trending for Data Analysts?](project_cv\3_trending_skills.ipynb)
3. [How well do jobs and skills pay for Data Analysts?](project_cv\4_salary_analysis.ipynb)
4. [What are the optimal skills for data analysts to learn? (High Demand AND High Paying)](project_cv\5_optimal_skills.ipynb)

# Tools I Used

For my deep dive into the data analyst job market, I harnessed the power of several key tools:

- **Python:** The backbone of my analysis, allowing me to analyze the data and find critical insights.I also used the following Python libraries:
    - **Pandas Library:** This was used to analyze the data. 
    - **Matplotlib Library:** I visualized the data.
    - **Seaborn Library:** Helped me create more advanced visuals. 
- **Jupyter Notebooks:** The tool I used to run my Python scripts which let me easily include my notes and analysis.
- **Visual Studio Code:** My go-to for executing my Python scripts.
- **Git & GitHub:** Essential for version control and sharing my Python code and analysis, ensuring collaboration and project tracking.
## Import & Clean Up Data

I start by importing necessary libraries and loading the dataset, followed by initial data cleaning tasks to ensure data quality.
(that code i always used before analysing the data-set)
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
df['job_skills'] = df['job_skills'].apply(lambda x: ast.literal_eval(x) if pd.notna(x) else x)
```
### **All of the project you can see in the file: 'project_cv'**

(p.s. As well in the [basic_codes](project_cv\1_basic_codes.ipynb) file you can see a couple of additional basic codes (I started executing them before designing other projects, so they are not so readable))