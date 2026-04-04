# ingest-restapi-adls-adf

## Project Overview

This project demonstrates a scalable ingestion framework using Azure Data Factory to extract data from REST APIs and load it into ADLS Gen2 (raw layer).

## Architecture

REST API → Azure Data Factory → ADLS Gen2 (Raw JSON)

## Key Features

* Config-driven ingestion
* Pagination handling (next URL pattern)
* Incremental data loading
* Parameterized pipelines
* Secure secret management via Azure Key Vault

## Tech Stack

* Azure Data Factory
* Azure Data Lake Storage Gen2
* Azure Key Vault

## Structure

* adf/ → Pipelines, datasets, linked services
* source_config/ → API and pagination configurations
* config/ → Environment-specific configurations

## Use Case

Designed for scalable ingestion of API-based data sources into a centralized data lake.

## Security

All credentials are managed using Azure Key Vault and accessed via Managed Identity.

## Output

Data is stored in ADLS Gen2 under the raw layer in JSON format.
