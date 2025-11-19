Step 2.1. Copy This Repository on GitHub
Log in to GitHub in your browser.
Go to https://github.com/denisecase/applied-ml-template/.
Click the green Use this template button → choose Create a new repository.
Name your repository
Use all lowercase and dashes between words.
Example: applied-ml-yourname.
Set visibility to Public.
Click Create repository.
Step 2.2 Enable GitHub Pages (Recommended)
Before leaving GitHub, set up your repository to host your code documentation automatically.

In your new repository, click the Settings tab (top right).
In the left sidebar, select Pages.
Under Source, choose GitHub Actions.
Click the Code tab to return to the regular view.
GitHub will automatically build and publish your documentation when you push changes.

Step 2.3. Clone Your Repo to Your Computer and Open In VS Code
Open VS Code
Press Ctrl+Shift+P (Mac: Cmd+Shift+P)
Type "clone" and select "Git: Clone"
Paste your repository URL from GitHub
When asked where to save, navigate to your Repos folder:
Windows: C:\Repos
Mac/Linux: ~/Repos (in your home folder)
Click "Select Repository Location"
When VS Code asks "Open Repository?" - click "Open"
Alternative: Clone using terminal
Step 2.4. Install Recommended VS Code Extensions
When you first open this project, VS Code will prompt you to install recommended extensions. Click "Install All" to get Python support, Jupyter notebooks, linting, formatting, and Git integration. See .vscode/extensions.json for the complete list.

Step 2.5. Set Up Virtual Environment (.venv)
Using your VS Code terminal, run the following commands to:

Create a local virtual environment using uv venv.
Pin a Python version. Version 3.12 is recommended for speed, stability, and current compatibility.
Install optional tools (for dev and docs) and update packages.
Install pre-commit so checks run automatically on each commit.
Verify the python version installed is 3.12 (not 3.13 or 3.14).
Finally, activate your environment (operating system specific).
uv venv
uv python pin 3.12
uv sync --extra dev --extra docs --upgrade
uv run pre-commit install
uv run python --version
Windows (PowerShell):

.\.venv\Scripts\activate
Step 2.6. Git add-commit-push
Open a terminal in VS Code (PowerShell, zsh, or bash).

IMPORTANT: Replace the commit message with a clear and descriptive note about what you added or changed. Wrap the commit message in double quotes.

git add .
git commit -m "Initialize from pro-analytics-02-starter (no local edits)"
git push -u origin main
We can then use git push for later commits.

NOTE: This will trigger the GitHub Actions workflow and publish your documentation via GitHub Pages. This should verify things worked as provided. If anything fails, let us know in the associated discussion.

Step 2.8. Git add-commit-push
Open a terminal in VS Code (PowerShell, zsh, or bash).

git add .
git commit -m "Personalize pyproject authors and mkdocs site settings"
git push