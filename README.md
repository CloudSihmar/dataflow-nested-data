Data Transformation with Google Cloud Dataflow and BigQuery (CLI steps)
This repository demonstrates how to transform data from a JSON file in Google Cloud Storage using Google Cloud Dataflow and store it in BigQuery.

Prerequisites
Google Cloud SDK installed
Google Cloud project setup
Google Cloud Storage bucket created
Python installed
Steps
1. Create a Bucket and Upload the CSV File
Create a new bucket in Google Cloud Storage.
Upload your CSV file to the created bucket.
2. Open Cloud Shell and Upload the Python Pipeline File
Open Google Cloud Shell.
Upload your Python pipeline file (e.g., csv_to_bigquery.py) to Cloud Shell.
3. Set Up Python Virtual Environment, install apache beam and start a pipeline
Install the virtualenv module, create a virtual environment, and then activate it:

pip3 install virtualenv
python3 -m virtualenv env
source env/bin/activate


# Install Apache Beam
pip3 install apache-beam[gcp]

# Run the pipeline
python3 csv_to_bigquery.py \
--input gs://sandeep-apache/data-flow-demo.csv \
--output  gs://sandeep-apache/out.txt \
--project techlanders-internal \
--region us-central1 \
--staging_location gs://sandeep-apache/staging \
--temp_location gs://sandeep-apache/temp \
--runner DataFlowRunner
