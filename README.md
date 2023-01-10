# Overview

Data Engineering Solution Submission for Hovanes Gasparian. The ETL script runs as a Databricks Job using AutoLoader and Delta tables. Typically, Databricks converts notebooks into specially formatted Python scripts for running jobs, CI/CD actions, etc., from GitHub repos. However, those scripts only retain their readable notebook formats inside Databricks. Thus, an actual iPython notebook was used for readability purposes. Otherwise, the notebook would run on a Job cluster on any workspace hosted on AWS, Azure, or GCP. All dependencies would be handled by the Databricks runtime, negating the need for a conventional environment.yml file. However, to demonstrate the integration with GitHub actions, an example [action.yml](https://github.com/hovikgas/data_engineering/blob/main/action.yml) file is included, which, along with the [run_instruction.md](https://github.com/hovikgas/data_engineering/blob/main/run_instructions.md) markdown page, highlights the permissions and parameters needed to integrate with either AWS, Azure, or GCP.

For production workloads, actual PySpark Dataframes would be used, rather than vanilla Pandas Dataframes. Spark distributes workloads and takes advantage of parallelization, allowing for much more seamless scaling as data grows. Most of the Pandas functionality has been translated to the Pandas API for Spark. Very trivial code changes would be needed to translate the Pandas syntax used for production PySpark. As such, pure Pandas was used primarily for simplicity and expedience of local development.

## Dependencies and Prerequisites
Databricks runtime >= 11.3.x

See the [run_instructions](https://github.com/hovikgas/data_engineering/blob/main/run_instructions.md) page for more details on dependencies, as well as the prerequiquites for integration with GitHub Actions in the [action.yml](https://github.com/hovikgas/data_engineering/blob/main/action.yml) file
