# Data Science Repository
## Overview
This is a Template for a data science repository with python, poetry, pre-commit hooks & jupyterlab


## Repository structure
### Folders
- *config*: configs (jsons)
- *data*: (not committed) this is where your data lives
- *analytics*: code
  - *experiments*: experiments, like jupyter notebooks
  - *lib*: shared code, libraries, functions, classes
  - *src*: source code, executables

### Other files
- *.gitignore*
- *poetry.lock*: Python packages which are used and intalled using poetry, see below
- *README.md*: gives an overview

## Requirements
- python 3.8.10 (use pyenv: https://github.com/pyenv/pyenv-installer)
- poetry https://python-poetry.org/docs/basic-usage/#project-setup
- virtualenv `sudo apt-get install python3.8-venv`

## Installation

In the root folder, install the virtualenvironment that runs pre-commit.
This will add a precommit hook to `.git/hooks/pre-commit`.
```
python3.8 -m venv .venv
poetry install
poetry run pre-commit install
```

## Connect the Python Environment to Jupyter

```
poetry run python -m ipykernel install --user --name ds_py38 --display-name "DS py3.8.10"
```

