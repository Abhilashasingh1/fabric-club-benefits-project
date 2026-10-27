# Microsoft Fabric — Club Benefits Data Engineering Project

## Project Overview

This project demonstrates a data engineering workflow using Microsoft Fabric and PySpark. It uses the Medallion Architecture to transform raw data into cleaned, business-ready datasets for club reporting and benefit eligibility analysis.

## Architecture

**Bronze → Silver → Gold**

- **Bronze:** Ingest and preserve source data.
- **Silver:** Clean, standardize, and prepare data for analysis.
- **Gold:** Organize business-ready datasets for reporting and analysis.

## Gold Tables

| Table | Purpose |
|---|---|
| `gold_club_summary` | Summarizes firms and sales metrics by club and geography. |
| `gold_firm_benefit_status` | Organizes firm-level benefit eligibility and recorded status messages by scheme period. |
| `gold_firm_club_history` | Supports analysis of firms' club assignments across scheme periods. |

## Technologies

- Microsoft Fabric
- PySpark
- Delta tables
- Medallion Architecture
- Data transformation and aggregation

## Business Questions

1. How many firms belong to each club?
2. Which firms are eligible or ineligible for benefits, and what status information is recorded?
3. Which firms appear in the same club across multiple scheme periods?

## Data Quality and Interpretation

Benefit ineligibility does not necessarily mean a benefit was lost. Historical eligibility changes and verified business rules are required to establish benefit loss. Repeated club assignments should also be validated against the source data.

## How to Explore

1. Open the notebook in this repository.
2. Review the Bronze, Silver, and Gold transformations.
3. Run the notebook in a configured Microsoft Fabric environment with access to the required source data and Lakehouse tables.
4. Validate table counts, duplicate keys, null values, and business logic before using the results.

## Project Status

The initial Bronze-to-Silver workflow and three Gold tables have been created. Further validation and documentation are part of the ongoing development.

## Data Privacy

Use synthetic or authorized, anonymized data when sharing this project publicly. Do not publish confidential company data, credentials, or connection strings.
