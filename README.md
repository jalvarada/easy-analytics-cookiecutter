# easy-analytics-cookiecutter
[![Maintainers Wanted](https://img.shields.io/badge/maintainers-wanted-red.svg)](https://github.com/pickhardt/maintainers-wanted)

<br>

DESCRIPTION IS STILL MISSING, IN HERE SOMETHING ABOUT REPRODUCBILITY, SAMPLE NOTEBOOKS, GOOD PRACTICES AND LEARNING SHOULD BE WRITTEN.


Inspired by [Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/) and [cookiecutter-data-science](https://github.com/drivendata/cookiecutter-data-science).
****
# Instructions

## Steps to use this cookiecutter template

<br>

1. Install [miniconda3](https://docs.conda.io/en/latest/miniconda.html)
2. Install [git](https://www.jcchouinard.com/install-git/)
3. Install cookiecutter

```sh
# add conda-forge channel
$ conda config --add channels conda-forge

# Install cookiecutter
$ conda install cookiecutter
```
4. Create a new project
```sh
# 1 - Change working directory to your Desktop
$ cd Desktop

# 2 - Create a new project
$ cookiecutter https://github.com/jalvarada/easy-analytics-cookiecutter

# 3 - Change working directory to the project folder
$ cd Desktop/<project name> # MAC USERS
$ cd Desktop\<project name> # WINDOWS USERS

# 4 - Build the conda environment
$ conda env create -f environment.yml

# 5 - Activate conda environment
$ conda activate dev

# 6 - Run jupyter notebooks and begin working!
$ jupyter notebook

# 7 - Deactiivate conda environmente
$ conda deactivate
```

## Pimp your jupyter notebook
<br>

```sh
# 1 - change working directory to <project name>
$ cd Desktop/<project name> # MAC USERS
$ cd Desktop\<project name> # WINDOWS USERS

# 2 - generate base config file
$ jupyter notebook --generate-config

# 3 - Install jupyter extensions
$ jupyter contrib nbextension install --user
$ jupyter nbextension install --py --user jupytext

# 4 - Create config folder to enable some nice extensions
$ mkdir /Users/<username>/.jupyter/nbconfig # MAC
$ mkdir C:\Users\<username>\.jupyter\nbconfig # WINDOWS

# 5 - Create custom folder to modify jupyter default behaviour
$ mkdir /Users/<username>/.jupyter/custom # MAC
$ mkdir C:\Users\<username>\.jupyter\custom # WINDOWS

# 6 - copy .js file from <project name> (current wd) to .jupyter
$ cp .jupyter/custom/custom.js /Users/jupyter/custom/custom.js # MAC
$ copy .jupyter\custom\custom.js C:\Users\.jupyter\custom\custom.js # WINDOWS

# 7 - copy .json file from <project name> (current wd) to .jupyter
$ cp .jupyter/nbconfig/notebook.json /Users/jupyter/nbconfig/notebook.js # MAC
$ copy .jupyter\nbconfig\notebook.json C:\Users\.jupyter\nbconfig\notebook.json # WINDOWS

# 8 - Enjoy!!
$ jupyter notebook
```

# The directory structure
------------

The directory structure of your new project looks like this:

```
├── README.md            <- The top-level README for developers using this project.
├── config               <- Files used for jupyter notebook customization 
├── data
│   ├── external         <- Data from third party sources.
│   ├── interim          <- Intermediate data that has been transformed.
│   ├── processed        <- The final, canonical data sets for modeling.
│   └── raw              <- The original, immutable data dump.
││
├── models               <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks            <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
││
├── reports              <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures          <- Generated graphics and figures to be used in reporting
│
├── sql                  <- Hive, Presto or Spark queries
│
├── src                  <- Source code for use in this project.
│   ├── __init__.py      <- Makes src a Python module
│   │
│   ├── data             <- Scripts to download or generate data
│   │   └── make_dataset.py
│   │
│   ├── features         <- Scripts to turn raw data into features for modeling
│   │   └── build_features.py
│   │
│   ├── models           <- Scripts to train models and then use trained models to make
│   │   │                 predictions
│   │   ├── predict_model.py
│   │   └── train_model.py
│   │
│   ├── utils            <- Productivity and repetetive tasks scripts
│   │   └── utils.py
│   |
│   └── visualization    <- Scripts to create exploratory and results oriented visualizations
│       └── visualize.py
│    
├── .env                 <- Environment variables read by python-dotenv. DANGEROUS!!!
│
├── environment.yml      <- Reproducible conda environment ready for analytics.
│
├── requirements.txt     <- The requirements file for reproducing the analysis environment, e.g.
│                           generated with `pip freeze > requirements.txt`
│
└── setup.py             <- Package building requierd file
```

