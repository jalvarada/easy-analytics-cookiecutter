# easy-analytics-cookiecutter
[![Maintainers Wanted](https://img.shields.io/badge/maintainers-wanted-red.svg)](https://github.com/pickhardt/maintainers-wanted)

# Requirements to use the cookiecutter template

```
$ conda config --add channels conda-forge
$ conda install cookiecutter
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

# Used Variables
The following table provides an overview about parameter, that are queried by cookiecutter (and why)

| Name | Description |
| ---- | ----------- |
| **project_name** | *Name of your project* |
| **jupyter_password** | *Password to protect your Jupyter service* |
| **postgres_db_password** | *Password of standard postgres user* |
| **shared_db_password** | *Password for shared database* |
| **superset_db_password** | *Password for superset database* |
