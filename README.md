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
