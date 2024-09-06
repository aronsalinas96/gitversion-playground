<h1 align="center">
    Fact_Campaigns
</h1>



<details open="open">
<summary>Table of Contents</summary>

- [Introduction](#1-introduction)
- [Access Information](#2-access-information)
- [Format and Description](#3-format-and-description)
- [Events / Data Types](#4-events--data-types)
- [Dedup Criteria](#5-dedup-criteria)
- [Code Strategys](#6-code-strategys)
- [References related](#7-references-related)


</details>

---

### 1. Introduction

#### Fact_Campaigns
<table>
<tr>
<td>

TODO: Entity description...

</td>
</tr>
</table>

### 2. Access Information

**Snowflake**

**Database**: SCRM_LPDW_{environment} for each environment <br>
**Schema**: STAR_MODEL <br>
**Table**: Fact_Campaigns

### 3. Format and description


> Last updated on version 0.1.0

| Column Name        | Column Type   | Description                                                                 |
|--------------------|---------------|-----------------------------------------------------------------------------|
| RW_INSERT_TIME_KEY | TIMESTAMP_NTZ | Timestamp when data was received in Data Platform and stored in RAW storage |
| L1_INSERT_TIME_KEY | TIMESTAMP_NTZ | Timestamp when the data was inserted in L1 table.                           |
| Col..              | VARCHAR       | Example col                                                                 |

### 4. Events / Data Types

Data sources and data types for campaigntrk construct:
- l1.campaigntrk
  - dataTypeName ["v1", "v2"]
> Additional info...

### 5. Dedup Criteria

```
        self.unique_columns: Optional[List[col]] = [
            col(ChargingsummarytrkFields.country),
        ]
        self.sorting_columns: Optional[List[col]] = [
            col(ChargingsummarytrkFields.country).desc(),
        ]
```
### 6. Code Strategys

- [PySpark Guidelines](https://confluence.schwarz/x/LIkyFQ)
- [Cookiecutter](https://github.com/cookiecutter/cookiecutter)
- [Testing strategy pyspark ETLs](https://confluence.schwarz/x/1zmqFg)
- [[HowTo] PySpark ETL e2e](https://confluence.schwarz/x/e4g7Fg)
- [[HowTo] Manual run in Databricks using Postman](https://confluence.schwarz/x/mQ1lFg)

### 7. References related

Source Entities:
- TODO: Change this link [ChargingSummary v2](https://confluence.schwarz/x/JasaEwÇ)
- TODO: Change this link [L1: CHARGINGSUMMARYTRK](https://confluence.schwarz/x/hW4YEw)

Snowflake

- [Repository / Code](https://dev.azure.com/lcrm4/Lidl.BS/_git/bs-lpdw-Fact-Campaigns)
- [bs-commons (general utilities for ETLs)](https://dev.azure.com/lcrm4/Lidl.BS/_git/bs-commons)
- [bs-schemas (general utilities for ETLs)](https://dev.azure.com/lcrm4/Lidl.BS/_git/bs-schemas)
- [Orchrestation in airflow](https://dev.azure.com/lcrm4/Lidl.BS/_git/bs-airflow-dbt)
