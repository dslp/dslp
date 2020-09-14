# Default Directory Structure

A template repository with this structure can be found [here](https://github.com/dslp/dslp-repo-template).

We've tried to create a fairly generic directory structure that supports the core workflows in data science projects. You should feel free to add new files and directories as needed, but should be careful in changing the directory structure. Of course, there's nothing to stop you from doing so, we just encourage you to think about it first.

If there's something you think doesn't make sense. Let us know.

## Directories

```
├── .cloud              # for storing cloud configuration files and templates (e.g. ARM, Terraform, etc)
├── .github
│   ├── ISSUE_TEMPLATE
│   │   ├── Ask.md
│   │   ├── Data.Aquisition.md
│   │   ├── Data.Create.md
│   │   ├── Experiment.md
│   │   ├── Explore.md
│   │   └── Model.md
│   ├── labels.yaml
│   └── workflows
├── .gitignore
├── README.md
├── code
│   ├── datasets        # code for creating or getting datasets
│   ├── deployment      # code for deploying models
│   ├── features        # code for creating features
│   └── models          # code for building and training models
├── data                # directory is for consistent data placement. contents are gitignored by default.
│   ├── README.md
│   ├── interim         # storing intermediate results (mostly for debugging)
│   ├── processed       # storing transformed data used for reporting, modeling, etc
│   └── raw             # storing raw data to use as inputs to rest of pipeline
├── docs
│   ├── code            # documenting everything in the code directory (could be sphinx project for example)
│   ├── data            # documenting datasets, data profiles, behaviors, column definitions, etc
│   ├── media           # storing images, videos, etc, needed for docs.
│   ├── references      # for collecting and documenting external resources relevant to the project
│   └── solution_architecture.md    # describe and diagram solution design and architecture
├── environments
├── notebooks
├── pipelines           # for pipeline orchestrators i.e. AzureML Pipelines, Airflow, Luigi, etc.
├── setup.py            # if using python, for finding all the packages inside of code.
└── tests               # for testing your code, data, and outputs
    ├── data_validation
    └── unit
```


## More details:

We don't add dummy files to the repo because we don't want to clutter things and we want users to have the freedom to do things how they want. But we do have views on how you can potentially populate these folders while keeping things organized.

### For code/models:

If you only have one model, keep things flat to keep things simple.

```
code/models
├── __init__.py
├── preprocess.py
├── train.py
└── evaluate.py
```


If you have multiple models deployed, each one needs a directory:

```
code/models
├── __init__.py
├── item_classifier
│   ├── preprocess.py
│   ├── train.py
│   └── evaluate.py
└── thing_forecaster
    ├── preprocess.py
    ├── train.py
    └── evaluate.py
```

If there are multiple versions of the same model deployed, you should use have a directory per version. See our advice on [semantic versioning](semantic-versioning.md).

```
code/models
├── __init__.py
├── item_classifier
│   ├── 1.0.0
│   │   ├── preprocess.py
│   │   └── train.py
│   ├── 2.1.4
│   │   ├── preprocess.py
│   │   └── train.py
│   └── 2.2.0
│       ├── preprocess.py
│       └── train.py
└── thing_forecaster
    ├── preprocess.py
    └── train.py
```

### For code/datasets

Directory for each dataset should contain all the code for creating or ingesting that dataset. It can also include the schema and datasheet.

```
code/datasets
├── __init__.py
├── customer_churn
│   ├── customer_churn.py
│   ├── datasheet.yml
│   └── schema.yml
└── customer_purchase_history
    ├── customer_purchase_history.py
    ├── datasheet.yml
    └── schema.yml
```

## Optional Directories

There are many frameworks and tools that require their own directories. They should be added as necessary. Here are our suggestions.

```
├── mlprojects     # create a root level directory named mlprojects to hold all mlflow project files if using mlflow (or similar)
```
