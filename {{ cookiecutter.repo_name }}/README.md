{{cookiecutter.project_name}}
==============================

{{cookiecutter.description}}


Project Organization
------------
```

    ├── LICENSE
    ├── ETHICS.md          <- The data science ethics checlist for this project. 
    ├── README.md          <- The top-level README for developers using this project.
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    │   
    │── log                <- Folder to store python log files 
    │
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    |
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── config.yml     <- COnfiguration file for making changes to file paths, data, gan training
    │   │
    │   ├── utility.py     <- Script with utility functions to be used across scripts
    │   │
    │   ├── etl.py         <- Script to download data, preprocess, load
    │   │   
    │   ├── train.py       <- Script to train models
    │   │ 
    │   ├── predict.py     <- Script to make predictions from trained models
    │   │ 
    │   ├── test_train.py  <- Script to test train functions
    │   │  
    │   └── test_utility.py  <- Script to test utility functions, i.e. load data
    │   │   
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    │
    └── pyproject.toml            <- settings for black, isort, pytest
 


```
## Setup

1. Git Clone the repo
```
git clone https://github.com/{{ cookiecutter.github_username}}/{{cookiecutter.repo_name}}.git 
```

2. Go to project root folder
```
cd {{cookiecutter.project_name}}
```

3. Create virtual environment
```
{{cookiecutter.python_interpreter}} -m venv env
source env/bin/activate
{{cookiecutter.python_interpreter}} -m pip install pip setuptools wheel
{{cookiecutter.python_interpreter}} -m pip install -e .

# OR to create virtual env and install development package
make venv

```
4. Setup secret environment vars in terminal
```
Create .env file in project directory to store your secret keys, i.e. AWS, APIs, etc. :

```
5. Run the code in terminal
```
python3 ./src/etl.py
python3 ./src/train.py
python3 ./src/predict.py
```
6. Clean, style, and test code:
   1. To run unit test in terminal (this will also clean and style code)
   ```
   make test
   ```

   2. To clean and autoformat code 
   ```
   make clean
   ```

   3. To lint code 
   ```
   make lint
   ```
   4. Clean, style, and test, and lint code
   ```
   make check
   ```

7. After usage
```
deactivate
```


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template </a> #cookiecutterdatascience</small></p>
<p><small>Example config.yml and scripts for stateless ETL, train, model MVP based on <a target="_blank" href="https://github.com/G-Hung/model-productization_article">G-Hung model production article and repository</a></small></p>
