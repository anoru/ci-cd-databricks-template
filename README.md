# Lab Data Science

_A logical, reasonably standardized, but flexible project structure for doing and sharing data science work._


### Requirements to use the cookiecutter template:
-----------
 - Python 2.7 or later
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

    cookiecutter https://github.com/.... # TO DO: Change this to point on the github repo of the template


### The resulting directory structure
------------

The directory structure of your new project looks like this: 


    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make virtual` or `make install`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data               <- This folder is only for local developing, delete .gitkeep to not include
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │   ├── references     <- Data dictionaries, manuals, and all other explanatory materials.
    │   ├── reports        <- Generated analysis as HTML, PDF, LaTeX, etc.
    │      └── figures     <- Generated graphics and figures to be used in reporting
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-az-initial-data-exploration`.
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so project can be imported
    │
    ├── {{cookiecutter.project_name}}  <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    ├── .env               <- Environment variables go here, can be read by `python-dotenv` package
    │
    ├── sandbox            <- Help to create a sanbdox env to test the project on local.
    │   │                     Please change only the runtime_requirements.txt file 
    │   │                     to specify the requirments needed during production runtime
    │   ├── create_cluster
    │   ├── run_now
    │   ├── run_pipeline
    │   └── runtime_requirements.txt
    │
    ├── deployment              <- Scripts to test and deploy in databricks
    │   ├── deployment.yml      <- Deployment configuration
    │   │
    │   ├── cicd-databricks     <- Python package de deploy on databricks
    │   │
    │   ├── dev-tests           <- Here goes the dev pipelines test. Excuted when merging to dev
    │   │   ├── pipeline1
    │   │   │   ├── job_spec_aws.json
    │   │   │   └── pipeline_runner.py
    │   │   │
    │   ├── integration-tests   <- Here goes the integration pipelines test. Excuted when merging to main
    │   │   ├── pipeline1
    │   │   │   ├── job_spec_aws.json
    │   │   │   └── pipeline_runner.py
    │   │   │
    │   └── pipelines           <- Here goes the production job pipelines. Excuted after release and deployment
    │       └── pipeline1
    │           ├── job_spec_aws.json
    │           └── pipeline_runner.py
    │
    │ job_spec_aws.json     : Contain model name, cluster configuration, and the job scheduling
    │ pipeline_runner.py    : The main pipeline script 
    └──

### References
------------

- <p><a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a></p>

- <p><a target="_blank" href="https://docs.databricks.com/dev-tools/ci-cd/ci-cd-jenkins.html">Continuous integration and delivery on Databricks using Jenkins</a></p>

- <p><a target="_blank" href="https://databricks.com/blog/2020/06/05/automate-continuous-integration-and-continuous-delivery-on-databricks-using-databricks-labs-ci-cd-templates.html">Automate continuous integration and continuous delivery on Databricks using Databricks Labs CI/CD Templates</a></p>

- <p><a target="_blank" href="https://resources.github.com/whitepapers/GitHub-Actions-Cheat-sheet/">GitHub Actions Cheat Sheet</a></p>

- <p><a target="_blank" href="https://databricks.com/session_na20/continuous-delivery-of-ml-enabled-pipelines-on-databricks-using-mlflow">Continuous Delivery of ML-Enabled Pipelines on Databricks using MLflow</a></p>

- <p><a target="_blank" href="https://github.com/databrickslabs/cicd-templates">Databricks Labs CI/CD Templates: Automated Databricks CI/CD pipeline creation and deployment</a></p>

- <p><a target="_blank" href="https://github.com/mshtelma/lendingclubsscoringdemo">Databricks Labs CI/CD Templates Tutorial - lendingclubsscoringdemo</a></p>

- <p><a target="_blank" href="https://github.com/mshtelma/cicdtestdev">Databricks actions - cicdtestdev</a></p>






