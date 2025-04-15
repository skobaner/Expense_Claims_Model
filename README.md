# Expense Claim Validation System

This project automates the processing and validation of travel and meal expense claims submitted in natural language, using LLMs and structured rule logic based on the Ontario Public Service Travel, Meal, and Hospitality Expenses Directive (2020).


## Project Setup Instructions (for VS Code)

### 1. Install Python
- Download from: https://www.python.org/downloads/
- During install, make sure to check **"Add Python to PATH"**

---

### 2. Set Up VS Code
- Open VS Code
- Go to **Extensions** (`Ctrl+Shift+X`)
- Search **Python** and install the extension by Microsoft

---

### 3. Install Project Dependencies
- Open **Terminal** in VS Code (`Terminal → New Terminal`)
- Run this command:
  ```bash
  pip install -r requirements.txt


## How to Use

1. Add Raw Claims:  
   Place your unstructured claims into `Data/raw_claims.json`. 

2. Run the Pipeline:  
   Use `Claim_process_wf_v2.ipynb` to:
   - Extracts structured data with LLMs
   - Validates each claim
   - Saves results to Excel

3. Visualize Rules (Optional):  
   Use `Decision_trees.ipynb` to generate decision trees for transparency.



## Overview

- Accepts raw text-based claims (e.g., from emails, forms, messages).
- Uses a language model (OpenAI) to extract structured fields from each claim.
- Applies rule-based decision trees to validate claims against policy.
- Outputs categorized and validated claims to Excel for reporting.

## Project Structure

    ├── Data/
    │   └── raw_claims.json                                # Input: Unstructured claims data
    │
    ├── Graphs/
    │   └── combined_graph.svg                             # Graph: visual representation of the validation logic
    │    
    ├── Results/
    │   └── processed_claims.xlsx                          # Output: Validated claims in Excel
    │
    ├── Decision_trees.ipynb                               # Builds visual representation of the validation logic
    ├── Claim_process_wf_v2.ipynb                          # Core logic: parsing, processing, validation
    ├── Travel_Meal_Hospitality_Expenses_Directive.md      # Extracted Rules Official directive (rules source)
    └── README.md

## Features

- Natural Language Processing: Converts free-text claims into structured JSON.
- Policy-Based Validation: Evaluates claims using formalized rules from the directive.
- Visual Decision Trees: Helps explain how each decision is made.
- Export to Excel: Separates meal and travel claims into clean outputs.

## Technologies

- OpenAI GPT-3.5 Turbo API





