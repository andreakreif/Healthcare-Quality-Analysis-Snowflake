# Healthcare-Quality-Analysis-CICD

Welcome! This is a portfolio project demonstrating a dbt load of synthetic healthcare data to a dimensional data warehouse designed for healthcare quality metrics calculation. Source data is loaded into the project as seeds to keep the project self-contained.  The database is DuckDB.  Generic tests and singular tests are used.

This repo was created by copying from https://github.com/andreakreif/Healthcare-Quality-Analysis-Snowflake and updating to support DuckDB implementation.  The other repo will take the dbt development further towards the quality calculations while this one will concentrate on demonstrating CI/CD logic (coming soon).

The simulated healthcare data is from Synthea (https://synthetichealth.github.io/synthea/)

The profiles.yml file is included in the repo under the root directory.  The source data is included in repo in the seeds folder so dbt can build it into the database.

## Instructions:
Install DuckDB, dbt and Python 3.12 in an environment if not already installed

Clone this repo
`git clone https://github.com/andreakreif/Healthcare-Quality-Analysis-CICD`

Change into the root directory for this project 'synthea_quality_analysis'
`cd synthea_quality_analysis`

set up virtual environment, may need to adjust path for your installation

`& "$env:LOCALAPPDATA\Programs\Python\Python312\python.exe" -m venv .venv`

Activate virtual environment
`.venv\Scripts\Activate.ps1`

