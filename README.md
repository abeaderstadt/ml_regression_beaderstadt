##  Machine & Project Setup Instructions

The steps below outline how I set up my machine and this Python project for reproducibility.

---

### Step 2.1: Create Repository on GitHub
1. Log in to GitHub in your browser.  
2. Create a new repository.  
3. Name your repository using all lowercase letters and dashes.  
   - Example: `applied-ml-yourname`  
4. Set visibility to **Public**.  
5. Click **Create repository**.

---

### Step 2.2: Enable GitHub Pages (Recommended)
1. In your new repository, click the **Settings** tab.  
2. In the left sidebar, select **Pages**.  
3. Under **Source**, choose **GitHub Actions**.  
4. Click the **Code** tab to return.  

> GitHub will automatically build and publish documentation when you push changes.

---

### Step 2.3: Clone Your Repo and Open in VS Code
1. Open VS Code.  
2. Press `Ctrl+Shift+P` (Mac: `Cmd+Shift+P`).  
3. Type `"clone"` and select **Git: Clone**.  
4. Paste your repository URL from GitHub.  
5. When asked where to save, navigate to your `Repos` folder:  
   - Windows: `C:\Repos`  
   - Mac/Linux: `~/Repos`  
6. Click **Select Repository Location**.  
7. When prompted **"Open Repository?"**, click **Open**.  

**Alternative:** Clone using the terminal.

---

### Step 2.4: Install Recommended VS Code Extensions
- VS Code will prompt you to install recommended extensions on first open.  
- Click **Install All** to get:  
  - Python support  
  - Jupyter notebooks  
  - Linting & formatting  
  - Git integration  
- See `.vscode/extensions.json` for full list.

---

### Step 2.5: Set Up Virtual Environment (.venv)
1. Create a `pyproject.toml` file.  
2. Create a `src` folder with a `.gitkeep` file inside.  

**In the VS Code terminal, run the following commands:**

```powershell
uv venv
uv python pin 3.12
uv sync --extra dev --extra docs --upgrade
uv run pre-commit install
uv run python --version

**Activate environment:**
.\.venv\Scripts\activate

Notes:
- .venv contains your project-specific Python environment.
- Python 3.12 is recommended.
- Pre-commit can be uninstalled if not needed.
```

---

### 2.6 Git Add - Commit - Push
1. Open a terminal in VS Code.
2. Stage all changes:
   ```powershell 
   git add .
   ```
3. Commit with a descriptive message:
   ```powershell 
   git commit -m "Initialize from pro-analytics-02-starter (no local edits)"
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

### Step 2.7: Later Commits
For subsequent changes: Always use descriptive commit messages.
```powershell
git add .
git commit -m "Personalize pyproject authors and mkdocs site settings"
git push
```
