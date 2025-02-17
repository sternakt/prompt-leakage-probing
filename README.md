# Prompt Leakage Probing

## Overview

The **Prompt Leakage Probing** project is a framework for testing Large Language Model (LLM) agents to assess their susceptibility to system prompt leaks by calculating the advantage. It is built using [AG2](https://ag2.ai/).

## What This Project Does

1. **Tests two agents** one with original prompt and one with sanitized prompt to asses the judge advantage for ech security level (higher advantage is weaker security to prompt leakage).
2. **Uses a "judge" and "analyzer" framework** to determine which agent the judge is prompting.
3. **Saves the results** to a CSV file for further analysis.

---

## Step-by-Step Instructions

### Prerequisites

1. **Install Python 3.10 or higher.** Check your Python version:
   ```bash
   python --version
   ```

2. **Set up your OpenAI API Key.** Export the key as an environment variable:
   ```bash
   export OPENAI_API_KEY="your_openai_api_key"
   ```

### 1. Clone the Repository and Navigate to It

```bash
git clone https://github.com/sternakt/prompt-leakage-probing.git
cd prompt-leakage-probing
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Understand the Notebooks

The project includes three Jupyter notebooks. Each tests a specific level of prompt leakage protection:

- **Low Protection**
- **Medium Protection**
- **High Protection**

#### Run the notebooks:

1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

2. Open the desired notebook (e.g., `low_protection.ipynb`) and run all cells.

3. Last cell will calculate the advantage for that security level

We have already uploaded the results (probe_results_low.csv, probe_results_medium.csv, probe_results_high.csv) from 40 runs so you can skip the generation and go straight to result analysis and advantage calculation.
