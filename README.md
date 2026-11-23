# IBM Community Article Recommendations

Udacity Data Science Nanodegree project exploring article recommendations from user interactions on the IBM Watson Studio platform.

**Status: unfinished starter.** The local environment is configured and dependency imports have been checked. Recommendation functions and written responses still need to be completed. The notebook has not been executed end to end, and project tests have not yet been run.

## Project scope

1. Explore users, articles, and interaction patterns.
2. Recommend popular articles using interaction counts.
3. Build user-user collaborative filtering and handle new users.
4. Use TF-IDF and KMeans on article titles for content recommendations.
5. Use SVD and cosine similarity for article recommendations, and discuss evaluation and tradeoffs.

This classroom version uses `starter/data/user-item-interactions.csv`, containing article IDs, titles, and user identifiers. Titles provide the text for content recommendations. The older `articles_community.csv` and precomputed `user_item_matrix.p` are not required by this version.

## Folder layout

```text
dsnd-recommendation-systems-project/
|-- .vscode/settings.json          # Interpreter and notebook working directory
|-- requirements.txt              # Pinned packages and supporting dependencies
|-- README.md
|-- LICENSE.txt                   # Supplied Udacity license
|-- CODEOWNERS                    # Supplied upstream ownership configuration
|-- starter/
|   |-- Recommendations_with_IBM.ipynb
|   |-- project_tests.py
|   |-- README.md                 # Original scaffold description
|   |-- top_5.p                   # Reference titles used by supplied tests
|   |-- top_10.p
|   |-- top_20.p
|   `-- data/user-item-interactions.csv
`-- .venv/                        # Local environment; excluded from Git
```

The classroom brief and rubric are kept in the sibling `Recommendations Project Documents` folder in the local course workspace. That folder also holds the downloaded archive and a reference notebook; it is not part of this repository. Use the notebook under `starter` for project work.

## Windows setup

The configured environment uses Windows 11 and Python 3.11.9. Install Python 3.11 and VS Code with Microsoft's Python and Jupyter extensions to work locally.

Open the project root in VS Code. In a **PowerShell** terminal at that root, create an environment only if `.venv` does not already exist:

```powershell
py -3.11 -m venv .venv
```

If the launcher is unavailable, use the full path to your Python 3.11 executable. For example, if Python is installed at the following location under your user profile:

```powershell
& "$env:USERPROFILE\AppData\Local\Python\pythoncore-3.11-64\python.exe" -m venv .venv
```

PowerShell expands `$env:USERPROFILE` to your user folder, so no username needs to be hardcoded. Python's installation location can vary; adjust the path to match your computer. Prefer the `py -3.11` command above when the launcher is available.

Install the recorded dependencies:

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

These commands use the environment's interpreter directly, so activation is not required. The main packages are pandas, NumPy, Matplotlib, scikit-learn, and ipykernel. The requirements file also pins their supporting dependencies.

## Working in VS Code

1. Open this repository's root folder, rather than only `starter`.
2. Open `starter/Recommendations_with_IBM.ipynb`.
3. Use **Select Kernel** to choose `.venv/Scripts/python.exe` if it is not already selected.
4. Complete the notebook sections in order, preserving the supplied checks.

Project settings specify `.venv` as the default interpreter and `starter` as the notebook working directory. The working directory matters because the notebook and test module use relative paths such as `data/user-item-interactions.csv` and `top_5.p`.

The starter contains incomplete assignments and functions, so **Run All will not succeed until implementation is complete**. After completing the project, restart the kernel, run all cells in order, and save the outputs.

## Validation

Check dependency consistency from the project root:

```powershell
.\.venv\Scripts\python.exe -m pip check
```

Project validation uses the notebook's assertions and calls to `project_tests.py`. That module is a helper, not a standalone test runner. Some supplied checks print failure messages instead of raising exceptions; review their output as well as execution errors. Keep the three `.p` reference files alongside the notebook for the popularity tests.

Passing imports and dependency checks verifies environment setup only; it does not establish correctness of the recommendation implementations.

## Submission and attribution

The intended submission is a public GitHub repository containing the completed notebook, saved results, supporting files, and setup instructions. A web application and an installable recommendation package are optional extensions.

The starter code, dataset, and supplied tests came from the Udacity classroom workspace. The downloaded Git history records `https://github.com/udacity/dsnd-recommendation-systems-project.git` as its upstream remote. That URL returned HTTP 404 when checked on 23 November 2026. The classroom files include updates relative to that Git baseline and are the starting point for this work.

Retain the supplied attribution and consult [LICENSE.txt](LICENSE.txt) for the license text accompanying the educational materials.
