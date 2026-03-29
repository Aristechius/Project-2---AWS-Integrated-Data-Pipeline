# Project-2-AWS-Integrated Data Pipeline

A cloud-native data pipeline built with Python, AWS S3, and AWS Lambda. This is my second project and first AWS-integrated build — part of my data engineering upskilling plan.

## What it does

- Uploads raw data files to an S3 bucket
- Triggers an AWS Lambda function on file arrival
- Lambda processes and transforms the data using Python
- Writes cleaned output back to a separate S3 bucket

## Architecture

```
Raw data (local)
      |
      v
  S3 (raw bucket)
      |
   [S3 event trigger]
      |
      v
  AWS Lambda
  (Python transform)
      |
      v
  S3 (processed bucket)
      |
      v
  Output / downstream use
```

## Why this project

This project bridges the gap between local Python work and real cloud infrastructure. It demonstrates a core data engineering pattern — event-driven, serverless data processing — using the AWS services most relevant to the Data Engineer Associate exam.

## Project structure

```
python-project-2-aws/
├── lambda/
│   └── handler.py        # Lambda function code
├── scripts/
│   └── upload_to_s3.py   # Local upload utility
├── data/
│   └── sample/           # Sample input files
├── infra/
│   └── setup_notes.md    # AWS setup instructions
└── README.md
```

## Prerequisites

- AWS account (free tier)
- AWS CLI configured locally
- Python 3.x
- boto3

## How to run

```bash
# Install dependencies
pip install -r requirements.txt

# Upload a file to trigger the pipeline
python scripts/upload_to_s3.py
```

## Status

> Planned — development begins June 2026 after AWS exam.

## Tech

- Python 3.x
- AWS S3
- AWS Lambda
- boto3
