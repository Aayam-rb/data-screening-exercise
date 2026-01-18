# data-screening-exercise

# Data Screening Exercise

This repository contains the completed Data Screening Exercise for Relevant Research. The exercise involves cleaning, analyzing, and visualizing immigration detention data in the United States.

---

## **Project Overview**

- **Objective:** Clean, analyze, and visualize the top 10 largest immigration detention facilities from a messy dataset.
- **Dataset:** `messy_ice_detention.csv`
- **Output:** Cleaned dataset, analysis notebook/script, and a visualization of the top 10 facilities.

---

## **Files**

| File | Description |
|------|-------------|
| `ice_detention_analysis.ipynb` | Jupyter Notebook containing data cleaning, analysis, and visualization steps |
| `Cleaned_ice_detention.csv` | Cleaned dataset after preprocessing |
| `line_chart.png` | Visualization of the top 10 largest detention facilities |
| `messy_ice_detention.csv` | Original messy dataset |
| `.ipynb_checkpoints/` | Checkpoints automatically created by Jupyter Notebook |
| `Data Scientist Screening Evaluation - 2026-01.pdf` | Assessment instructions |

---

## **How to Run**

### **Python**

1. Make sure you have Python installed (recommended 3.9+).
2. Install required packages:
pip install pandas matplotlib seaborn

3. Run the analysis notebook:
jupyter notebook ice_detention_analysis.ipynb
or, if using script
python ice_detention_analysis.py
4. The output visualization (line_chart.png) will be generated automatically.

### **Methodology**

Data Cleaning: Removed extra headers, fixed misformed dates, handled missing values, and removed special characters from string columns.

Data Analysis: Summed Level A-D populations to calculate Total Population and identified the top 10 largest facilities.

Visualization: Created a bar chart of the top 10 facilities using Matplotlib/Seaborn.

### **AI / LLM Usage**

ChatGPT was used for assistance in the following ways:

1. Loading the CSV and converting Excel-style dates

Prompt:
"Write a Python function to load a CSV file that is not in standard format"
"Convert Excel-style date columns to proper datetime objects."

Usage: ChatGPT’s suggestions were adapted to correctly load the messy CSV and convert the Last Inspection End Date column to a proper Python datetime type.

2. Cleaning string columns

Prompt:
"Write a Python function that loops through each column to check the datatype and removes special characters from all string columns in a DataFrame."

Usage: The AI response was modified to handle missing values and ensure non-string columns were not affected.

3. Handling missing values

Prompt:
"Write a Python function that checks and gets all the 'object' data type columns which have missing values in the DataFrame."

Usage: Modified to ensure only relevant columns were checked and missing values were properly identified.

4. Filling missing Name, City, and State values

ChatGPT helped suggest values for missing facility information in the dataset. These changes were verified manually.

5. Creating the visualization (bar chart)

Prompt:
"Write Python code to plot a horizontal bar chart of the top 10 detention facilities by total population, with the largest bar at the top, and save the figure as a PNG."

Usage: ChatGPT’s suggestions were adapted to generate line_chart.png with inverted y-axis, labels, and title for easy interpretation.

No other AI tools were used.

### **Reference:**

ChatGPT (OpenAI) – guidance on Python functions: handling missing values, cleaning strings, loading CSVs, date conversion, and creating visualizations