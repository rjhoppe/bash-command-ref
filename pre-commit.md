# How to run pre-commit hooks on your repo
## 1. Install the pre-commit library via pip
```
pip install pre-commit
```
## 2. Add a .pre-commit-config.yaml file to your repo
Here is an example of what your preconfig file can look like:
```
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v2.3.0
    hooks:
    -   id: check-yaml
    -   id: end-of-file-fixer
    -   id: trailing-whitespace
    -   id: check-added-large-files
    -   id: check-json
    -   id: check-merge-conflict
    -   id: trailing-whitespace
    -   id: check-ast
```
## 3. Run the pre-commit install to set up the git hook scripts
```
pre-commit install
```
After running this command, pre-commit will automatically run using the parameters configured in the .pre-commit-config.yaml file on all futures git commits.
NOTE: By default, pre-commit will only run on the changed files during git hooks.
## 4. Manually run pre-commit
```
pre-commit run --all-files
```
