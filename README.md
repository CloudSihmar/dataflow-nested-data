# Data Transformation with Google Cloud Dataflow and BigQuery (CLI steps)

This repository demonstrates how to transform data from a JSON file in Google Cloud Storage using Google Cloud Dataflow and store it in BigQuery.

## Prerequisites

- Google Cloud SDK installed
- Google Cloud project setup
- Google Cloud Storage bucket created
- Python installed

## Steps

### 1. Create a Bucket and Upload the CSV File

1. Create a new bucket in Google Cloud Storage.
2. Upload your CSV file to the created bucket.



### 2. Open Cloud Shell and Upload the Python Pipeline File

1. Open Google Cloud Shell.
2. Upload your Python pipeline file (e.g., `json_to_bigquery.py`) to Cloud Shell.

### 3. Set Up Python Virtual Environment, install apache beam and start a pipeline

Install the `virtualenv` module, create a virtual environment, and then activate it:

```sh
pip3 install virtualenv
python3 -m virtualenv env
source env/bin/activate


# Install Apache Beam
pip3 install apache-beam[gcp]

# Run the pipeline
python3 json_to_bigquery.py 







