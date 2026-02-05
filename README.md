# Job Market Data Analytics Project

A comprehensive data analytics project that analyzes job market trends, salary patterns, and employment characteristics using Python and machine learning techniques.

## 📊 Project Overview

This project provides an in-depth analysis of job market data to uncover insights about:

- Salary trends and correlations with experience
- Distribution of job titles and work types
- Most in-demand skills and qualifications
- Company size impact on compensation
- Predictive modeling for salary estimation
- Job market clustering and segmentation

## 🎯 Objectives

1. **Explore and clean** job market data from various sources
2. **Engineer features** to create meaningful analytical variables
3. **Visualize patterns** in job titles, salaries, skills, and qualifications
4. **Build predictive models** to estimate salaries based on job characteristics
5. **Cluster jobs** to identify market segments
6. **Provide actionable insights** for job seekers, employers, and recruiters

## 🔧 Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib & Seaborn** - Data visualization
- **Scikit-learn** - Machine learning (implied in model comparison)
- **Regular Expressions (re)** - Text parsing and extraction
- **Jupyter Notebook** - Interactive development environment

## 📁 Project Structure

```text
data analytics project/
│
├── job-market-data-analytics-project.ipynb    # Main analysis notebook
└── README.md                                   # Project documentation
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Running the Analysis

1. Clone or download this repository
2. Ensure the dataset is available at the specified path or update the path in the notebook
3. Open Jupyter Notebook:

   ```bash
   jupyter notebook job-market-data-analytics-project.ipynb
   ```

4. Run all cells sequentially to reproduce the analysis

## 📈 Analysis Workflow

### 1. Data Loading and Setup

- Import necessary libraries
- Load job descriptions dataset
- Create working copy for analysis

### 2. Initial Data Exploration

- Display dataset structure and dimensions
- Examine data types and distributions
- Identify missing values
- Generate statistical summaries

### 3. Exploratory Data Analysis (EDA)

- **Top Job Titles**: Identify most common positions
- **Work Type Distribution**: Analyze full-time, part-time, contract, etc.
- **Company Sizes**: Examine employer size distribution
- **Skills Analysis**: Extract and visualize most demanded skills
- **Qualifications**: Analyze educational requirements

### 4. Data Cleaning and Preprocessing

- Remove unnecessary columns (Role, Job Id, latitude, longitude, etc.)
- Handle missing values
- Sample data strategically (50% per country, company size, job title)
- Reduce dataset size while maintaining representativeness

### 5. Feature Engineering

Key transformations include:

- **Experience Normalization**: Convert experience ranges to numeric values
  - Categorical mapping (Internship=0, Entry level=1, Associate=3, etc.)
  - Parse ranges like "4 to 15 Years" → average value
  
- **Salary Normalization**: Extract midpoint from salary ranges
  - Handle various formats (e.g., "50k-70k", "$50000-$70000")
  
- **Company Size Grouping**: Categorize companies into size tiers
  - Small, Medium, Large, Enterprise
  
- **Categorical Encoding**: Convert text features to numeric codes
  - Work Type, Country, Qualifications

### 6. Data Visualization

**Feature Relationships**:

- Correlation heatmaps for numeric features
- Experience vs Salary scatter plots with trend lines
- Average Salary vs Experience by Company Size
- Jittered scatter plots for better visualization of overlapping points

### 7. Machine Learning Model Evaluation

Compared three regression models for salary prediction:

| Model | MAE ($) | RMSE ($) | Improvement |
| ----- | ------- | -------- | ----------- |
| Linear Regression | 5,420 | 7,980 | Baseline |
| Random Forest | 4,120 | 5,980 | 24.0% |
| **XGBoost** | **3,560** | **5,210** | **34.3%** |

**Key Findings**:

- XGBoost provides the best performance
- MAE reduced by $1,860 (34.3%) compared to Linear Regression
- RMSE reduced by $2,770 (34.7%) compared to Linear Regression

### 8. Clustering Analysis

- Applied K-Means clustering to identify job market segments
- Visualized clusters in 2D space
- Calculated centroids and cluster assignments
- Demonstrated iterative convergence process

## 💡 Key Insights

### Data Quality

- Implemented strategic sampling (50% per category)
- Handled missing values systematically
- Applied outlier treatment for robust analysis

### Correlations

- **Experience and Salary**: Positive correlation confirmed
- **Company Size Impact**: Larger companies tend to offer higher salaries
- **Geographic Variations**: Salary differences across countries

### Skills and Qualifications

- **Top Skills**: Python, SQL, Machine Learning, Communication
- **Common Qualifications**: Bachelor's Degree, Master's Degree
- **Skill Combinations**: Certain skill pairs command premium compensation

### Market Trends

- Entry-level positions dominate job postings
- Remote/hybrid work types increasing in availability
- Tech and data-related roles show strong growth

## 🎯 Business Applications

1. **For Job Seekers**:
   - Benchmark salary expectations
   - Identify high-demand skills to develop
   - Understand experience vs compensation relationship

2. **For Employers**:
   - Competitive salary benchmarking
   - Optimize job descriptions and requirements
   - Identify talent availability trends

3. **For Recruiters**:
   - Market intelligence for client advisory
   - Skill gap analysis
   - Regional market comparisons

## 📊 Sample Visualizations

The notebook includes various visualizations:

- Bar charts for categorical distributions
- Correlation heatmaps
- Scatter plots with regression lines
- Line plots for trend analysis
- Clustering visualizations
- Model performance comparisons

## 📝 Data Source

The analysis uses a job descriptions dataset with the following key fields:

- Job Title
- Company
- Location (Country)
- Salary Range
- Experience Required
- Work Type
- Skills
- Qualifications
- Company Size

## 📄 License

[MIT](LICENSE)

## 👤 Authors

- Aram Elheni
- Youssef Jaziri
- Chaima Ben Yedder
- Zied Knani

## 🙏 Acknowledgments

- Dataset source: Kaggle Job Description Dataset
- Python data science community
- Open-source library maintainers
