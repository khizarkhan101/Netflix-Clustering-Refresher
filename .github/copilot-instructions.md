<!-- Generated: concise, repo-specific Copilot instructions -->
# Copilot instructions for this repository

Purpose: Help AI coding agents become productive quickly by documenting the project's discoverable structure and local developer workflows.

- **Repo summary (discoverable):** This workspace currently contains a Python virtual environment at `.venv` and a Jupyter notebook named `.venv\netflix.ipynb`. The environment includes packages commonly used for notebooks and ML workflows (e.g., `sklearn`, `nbconvert`, `jupyter_server`, `debugpy`, `zmq`).

- **Primary entry points:**
  - Notebook: `.venv\netflix.ipynb` — inspect this first to understand the data flow and experiments.
  - Virtual environment: `.venv` — use the interpreter inside this venv to run scripts and tests.

- **Quick setup / run (local dev):**
  - Activate the venv (PowerShell):
    ```powershell
    .\.venv\Scripts\Activate.ps1
    ```
  - Or (cmd):
    ```cmd
    .\.venv\Scripts\activate.bat
    ```
  - Use the venv Python to run scripts or start a notebook server. If a `requirements.txt` or `pyproject.toml` appears later, prefer installing into `.venv`.

- **What to look for when editing or generating code:**
  - Prefer notebook-friendly changes: keep analysis, data-loading, and visualization blocks grouped in notebooks; move reusable logic into small Python modules if re-used across cells.
  - When creating new files, place lightweight helpers under a top-level package (create one if needed) rather than scattering logic in notebooks.

- **Conventions inferred from the workspace:**
  - Virtual environment is committed/placed inside the repo at `.venv` — use it directly rather than creating a new venv with a different path.
  - Notebooks are used as first-class artifacts. Preserve cell order and outputs when edits are intentional; prefer small, well-named cells for clarity.

- **Debugging & testing hints (discoverable):**
  - `debugpy` is available in the venv; use it to attach debuggers to running notebook kernels or scripts.
  - No explicit test framework or scripts were found; when adding tests, include a lightweight `pytest` setup and a `Makefile` or `README` entry describing how to run them.

- **Integration points / dependencies:**
  - The venv contains packages indicating Jupyter and scikit-learn usage; assume data-science style dependencies and keep changes small and well-documented.

- **PR guidance for AI agents:**
  - Keep changes minimal and self-contained. For notebook edits, include a short summary of the cell-level changes and why they were made.
  - If adding dependencies, update a top-level `requirements.txt` or `pyproject.toml` and call out the reason in the PR.

If anything in this file is unclear or you'd like additional checks (e.g., scanning for source modules, building a requirements list, or extracting runnable scripts from notebooks), tell me what to add and I'll iterate.
