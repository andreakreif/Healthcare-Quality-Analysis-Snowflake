# Healthcare-Quality-Analysis-CICD

Welcome! This is a portfolio project demonstrating a dbt load of synthetic healthcare data to a dimensional data warehouse designed for healthcare quality metrics calculation. Source data is loaded into the project as seeds to keep the project self-contained.  The database is DuckDB.  Generic tests and singular tests are used.

This repo was created by copying from https://github.com/andreakreif/Healthcare-Quality-Analysis-Snowflake and updating to support DuckDB implementation.  The other repo will take the data development further towards the quality calculations in snowflake while this one will concentrate on demonstrating CI/CD logic (coming soon).

The simulated healthcare data is from Synthea (https://synthetichealth.github.io/synthea/)

The profiles.yml file is included in the repo under the root directory.  The source data is included in repo in the seeds folder so dbt can build it into the database.

## Prerequisites

- **Python 3.12.** dbt doesn't yet support newer versions such as 3.15.
  Check with `py -3.12 --version`. If it isn't installed, get it from
  [python.org](https://www.python.org/downloads/).
- **Git**, to clone the repo.

## Instructions:

1. Get the code by cloning this repo
`git clone https://github.com/andreakreif/Healthcare-Quality-Analysis-CICD`

2. Change to the root directory for this project 'synthea_quality_analysis'
`cd synthea_quality_analysis`

3. Set up virtual environment with Python 
`py -3.12 -m venv .venv`
   then
`.venv\Scripts\Activate.ps1`
4. Install dbt, DuckDB and dependencies
`pip install -r requirements.txt`

5. Load raw data into DuckDb
`dbt seed --profiles-dir .`

6. Build and test
`dbt build --profiles-dir . --exclude-resource-type seed`

