# Workshop: Delta Live Tables em Ação

This repository contains resources for working with Delta Live Tables in Databricks, including assets, data generators, code, and visual presentations.

## Folder Structure

### `asset/`
Contains Databricks Asset Bundles, including metadata and supporting documentation.

- `readme.md`: Documentation for asset bundles.

### `gen/`
Shadow Traffic Data Generator files used for testing and simulating data ingestion.

- `cdc-events.json`: JSON configuration for Change Data Capture (CDC) event simulation.
- `postgres-drivers.json`: Configuration file for simulating PostgreSQL driver data.
- `uber-eats.json`: JSON configuration file for Uber Eats traffic simulation.
- `readme.md`: Documentation for the `gen` folder.

### `images/`
Contains visual presentations created using Excalidraw.

- `ws-16-dlt-em-acao.png`: Diagram illustrating Delta Live Tables in action.

### `src/`
Holds Databricks-related code and workshop materials.

- `workshop-16-delta-live-tables.zip`: Compressed archive of workshop materials.
- `ws-16-delta-live-tables-action.dbc`: Databricks notebook bundle.
- `readme.md`: Documentation for the `src` folder.

## Usage
- Use the `gen` folder for generating test data with Shadow Traffic.
- The `src` folder contains Databricks code and training material.
- The `images` folder includes visual aids for presentations.

For more details, refer to the respective `readme.md` files in each directory.