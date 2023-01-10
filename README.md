# Overview
Data Engineering Solution Submission for Hovanes Gasparian. The ETL script is meant to be run as a Databricks Job using AutoLoader and Delta tables. Normally, Databricks converts its notebooks into specially formatted Python scripts for running jobs, CI/CD actions, etc. from GitHub repos.  However, those scripts only retain their readable notebook formats inside of Databricks. Thus, an actual iPython notebook was submitted for readability purposes. Otherwise, the notebook can be run on any workspace hosted on either AWS, Azure, or GCP, and is meant to be run by a Job cluster. As such, all dependencies are handled by the Databricks runtime, negating the need for a conventional environment.yml file. However, to demonstrate the integration with GitHub actions, an example action.yml file has been included which demonstrates the necessary parameters to integrate with either AWS, Azure, or GCP.

Naturally, for production workloads, actual PySpark Dataframes would be used, rather than vanilla Pandas Dataframe. Spark distributes workloads, and takes advantage of parallelization, allowing for much more seamless scaling as data grows. The vast majority of the functionality of Pandas has been translated to the Pandas API for Spark, and very trivial code changes would be needed in order to translate the Pandas syntax used for production PySpark. As such, pure Pandas was used primarily for simplicity and expedience of local development.

## Dependencies and Prerequisites
Databricks runtime >= 11.3.x

See the run instructions markdown file for more details on dependencies, as well as the prerequiquites for integration with GitHub Actions.
