# Beaderstadt Final Project: Regression Analysis
> My personalized Submission: GitHub Repository with Jupyter Notebook and Peer Review.

## Project Overview
In this project, I explore TODO

[Click here for my notebook file](https://github.com/abeaderstadt/ml_regression_beaderstadt/blob/main/regression_beaderstadt.ipynb)<br>
[Click here for my peer review file](https://github.com/abeaderstadt/ml_regression_beaderstadt/blob/main/peer_review.md)<br>

---

## Key Steps in This Project

## 1. Import and Inspect the Data
- Loaded the Medical Costs Dataset from Kaggle.
- Inspected the dataset using `.info()`, `.head()`, `.describe()`, and `.isnull().sum()`.
- Check for missing values and display summary statistics.

  - **Insights:**
    - TODO instances and ? features.
    - The target variable is TODO

---

## 2. Data Exploration and Preparation

### 2.1 Explore data patterns and distributions
- TODO

### 2.2 Handle missing values and clean data
- TODO 

### 2.3 Feature selection and engineering
- TODO

  - **Rationale:**
    - TODO

---

## 3. Feature Selection and Target Definition

### 3.1 Choose features and target
- TODO

**Reasoning:**  
- These features were selected because TODO

### 3.2 Define X and y
- Assign input features to X
- Assign target variable to y
---

## 4. Train a Model (Linear Regression)

### 4.1 Train and Split the data
- Split the data into training and test sets using train_test_split.
- Preserved the class balance for reliable evaluation.

### 4.2 Train model using Scikit-Learn model.fit() method
  
### 4.3 Evalulate performance for example:
- Regression: R^2, MAE, RMSE (RMSE has been recently updated)
- Clustering: Inertia, Silhouette Score
- Key metrics: TODO

---

## Section 5. Improve the Model or Try Alternates (Implement Pipelines)

### 5.1 Implement Pipeline 1: Imputer → StandardScaler → Linear Regression.
- TODO

### 5.2 Implement Pipeline 2: Imputer → Polynomial Features (degree=3) → StandardScaler → Linear Regression.
- TODO
  
### 5.3 Compare performance of all models across the same performance metrics
- TODO

**Reasoning:**  
- TODO  Which models performed better? How does scaling impact results?
---

## 6. Final Thoughts & Insights

### 6.1 Summarize findings.

TODO ADD KEY CHART 

***Top features and model performance***
- TODO INSTERT TABLE HERE AND NOTE


- TODO LIST KEY FINDINGS & CONCLUSIONS HERE

### 6.2 Discuss challenges faced.
- TODO

### 6.3 Future work
- TODO 

---

## How to Run

1. **Open the Project Notebook**  
   Navigate to and open the Jupyter notebook:  
   `regression_beaderstadt.ipynb`

2. **Select the Correct Kernel**  
   Ensure the notebook uses the correct Python environment where required libraries are installed.

3. **Clear Kernel / Outputs (Optional)**  
   Use Kernel -> Restart & Clear Outputs to start fresh and avoid stale variables or plots.

4. **Run the Notebook**  
   Execute cells sequentially to load data, prepare features, train models, and visualize results.

5. **View Results**  
   TODO

---

##  Machine & Project Setup Instructions

The steps below outline how I set up my machine and this Python project for reproducibility.

---

### Step 1: Create Repository on GitHub
1. Log in to GitHub in your browser.  
2. Create a new repository.  
3. Name your repository using all lowercase letters and dashes.  
   - Example: `applied-ml-beaderstadt`  
4. Set visibility to **Public**.  
5. Click **Create repository**.

---

### Step 2: Enable GitHub Pages (Recommended)
1. In your new repository, click the **Settings** tab.  
2. In the left sidebar, select **Pages**.  
3. Under **Source**, choose **GitHub Actions**.  
4. Click the **Code** tab to return.  

> GitHub will automatically build and publish documentation when you push changes.

---

### Step 3: Clone Your Repo and Open in VS Code
1. Open VS Code.  
2. Navigate to the folder where you would like to clone your repo.  
3. Open a new terminal and type `"git clone https://github.com/abeaderstadt/ml_regression_beaderstadt.git"`.  
4. You should see the repo folder in the explorer.
5. Select file - open folder - and select the newly cloned repo to begin working in it.

---

### Step 4: Install Recommended VS Code Extensions
- VS Code will prompt you to install recommended extensions on first open.  
- Click **Install All** to get:  
  - Python support  
  - Jupyter notebooks  
  - Linting & formatting  
  - Git integration  
- See `.vscode/extensions.json` for full list.

---

### Step 5: Set Up Virtual Environment (.venv)
1. Create a `pyproject.toml` file.  
2. Create a `src` folder with a `.gitkeep` file inside.  

**In the VS Code terminal, run the following commands:**

```powershell
uv venv
uv python pin 3.12
uv sync --extra dev --extra docs --upgrade
uv run pre-commit install
uv run python --version
```
**Activate environment:**
```powershell
.\.venv\Scripts\activate
```

**Notes:**
- .venv contains your project-specific Python environment.
- Python 3.12 is recommended.
- Pre-commit can be uninstalled if not needed.

---

### Step 6: Git Add - Commit - Push
1. Open a terminal in VS Code.
2. Stage all changes:
   ```powershell 
   git add .
   ```
3. Commit with a descriptive message:
   ```powershell 
   git commit -m "Create virtual environment setup files"
   ```
4. Uninstall pre-commit if not needed:
   ```powershell
   pre-commit uninstall
   ```
5. Push to GitHub: This triggers GitHub Actions and publishes documentation via GitHub Pages.
   ``` powershell
   git push -u origin main
   ```

--- 

### Step 7: Later Commits
For subsequent changes: Always use descriptive commit messages.
```powershell
git add .
git commit -m "Update formatting error"
git push
```
