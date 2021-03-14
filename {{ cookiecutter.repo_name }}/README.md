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
    ├── environment.yml   <- The requirements file for reproducing the analysis conda environment, e.g.
    │                         generated with `conda env freeze > environment.yml`
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
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io
 


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

3. Setup conda env in terminal
```
conda env create 

conda activate {{cookiecutter.repo_name}}

```
4. Setup conda env in terminal
```
Create .env file in project directory to store your secret keys, i.e. AWS, APIs, etc. :

```
5. Run the code in terminal
```
python3 ./src/etl.py
python3 ./src/train.py
python3 ./src/predict.py
```

6. To run unit test in terminal
```
pytest
```

7. To run autoformat.sh in terminal
```
# If you get permission error, you can try
# chmod +rx autoformat.sh

./autoformat.sh
```

8. After usage
```
conda deactivate
conda remove –name {{cookiecutter.repo_name}} –all
```


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template </a> #cookiecutterdatascience</small></p>
<p><small>Example config.yml and scripts for stateless ETL, train, model MVP based on <a target="_blank" href="https://github.com/G-Hung/model-productization_article">G-Hung model production article and repository</a></small></p>
