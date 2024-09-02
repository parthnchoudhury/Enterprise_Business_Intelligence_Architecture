<p align="center">
  <img src="https://user-images.githubusercontent.com/76818972/209818252-f5f34122-e268-489c-bf67-ae00962fadc0.jpg" height=130>
</p>

## <div align="center"><b><a href="README.md">English</a> | <a href="README_CN.md">Français</a></b></div>

![download](https://img.shields.io/badge/cloud-101open-yellow)
![PyPI](https://img.shields.io/badge/azure-v2.2-blue)
![Open issue](https://img.shields.io/badge/lambda-passing-yellow)
[![Closed issue](https://img.shields.io/github/issues-closed/TencentARC/GFPGAN)](https://github.com/TencentARC/GFPGAN/issues)
[![LICENSE](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/TencentARC/GFPGAN/blob/master/LICENSE)
[![python lint](https://github.com/TencentARC/GFPGAN/actions/workflows/pylint.yml/badge.svg)](https://github.com/TencentARC/GFPGAN/blob/master/.github/workflows/pylint.yml)

# Enterprise Business Intelligence Architecture

This scenario shows how data can be ingested into a cloud environment from an on-premises data warehouse of an Agricultural Industry, then served using a business intelligence (BI) model. This approach could be an end goal or a first step toward full modernization with cloud-based components.

The following steps build on the Azure Synapse Analytics end-to-end scenario. It uses Azure Pipelines to ingest data from a SQL database into Azure Synapse SQL pools, then transforms the data for analysis.

![image](https://user-images.githubusercontent.com/76818972/209845148-002f4603-cbe3-45ba-94e7-57ed53cdde38.png)

# Workflow

## Data source
The source data is located in an SQL Server database in Azure. To simulate the on-premises environment, deployment scripts for this scenario provision an Azure SQL database. The AdventureWorks sample database is used as the source data schema and sample data. For information on how to copy data from an on-premises database, see copy and transform data to and from SQL Server.

## Ingestion and data storage
1. Azure Data Lake Gen2 is used as a temporary staging area during data ingestion. You can then use PolyBase to copy data into an Azure Synapse dedicated SQL pool.

2. Azure Synapse Analytics is a distributed system designed to perform analytics on large data. It supports massive parallel processing (MPP), which makes it suitable for running high-performance analytics. Azure Synapse dedicated SQL pool is a target for ongoing ingestion from on-premises. It can be used for further processing, as well as serving the data for Power BI through DirectQuery.

3. Azure Pipelines is used to orchestrate data ingestion and transformation within your Azure Synapse workspace.

## Analysis and reporting
The data-modeling approach in this scenario is presented by combining the enterprise model and BI Semantic model. The enterprise model is stored in an Azure Synapse dedicated SQL pool, and the BI Semantic model is stored in Power BI Premium capacities. Power BI accesses the data via DirectQuery.

# About Me :sunglasses: #
- With 12+ years of industry experience, I have thrived in Data Science, Data Governance, IT, Cloud and Product Management. I have a keen interest and expertise in solving business problems using unique logic and analytics. I bring solutions to the table based on competitive Business Acumen and Human Intelligence.
- Have a look at my portfolio: [Helping organizations level all their Business arguments using Data & Technology (AI-Powered) | Ex_SyngentaAG | Ex_Zalando | Ex_Freecharge | Ex_Myntra Jabong | Ex_Supercell | Ex_Infosys](https://www.linkedin.com/in/ianthropos/)
- I love talking about #cloudarchitecture, #businessanalytics, #softwareengineerng, #datapipelines, #machinelearning, and #artificialintelligence
