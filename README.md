# A42 Custom CookieCutter Data Science Template

_A data science project template, customized from the CookieCutter Data Science template, to make reproducible projects._


#### [Project homepage](https://github.com/JessicaRudd/A42-data-science)


### Requirements to use the cookiecutter template:
-----------
 - Python 2.7 or 3.5+
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


### To start a new project, run:
------------

    cookiecutter https://github.com/JessicaRudd/A42-data-science


<!-- [![asciicast](https://asciinema.org/a/244658.svg)](https://asciinema.org/a/244658) -->


### The resulting directory structure
------------

The directory structure of your new project looks like this: 

```

    ├── LICENSE
    ├── ETHICS.md          <- The data science ethics checlist for this project. 
    ├── README.md          <- The top-level README for developers using this project.
    ├── Makefile           <- Makefile with commands like `make venv` or `make test`
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
    |                      <- Includes an analysis template notebook to get started
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
    └── pyproject.toml            <- black, isort, pytest configs

```

### Installing cookiecutter development requirements
------------

    pip install -r requirements.txt

### Running the cookiecutter tests
------------

    py.test tests
