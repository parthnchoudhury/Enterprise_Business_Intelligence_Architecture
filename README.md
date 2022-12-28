<p align="center">
  <img src="assets/gfpgan_logo.png" height=130>
</p>

## <div align="center"><b><a href="README.md">English</a> | <a href="README_CN.md">简体中文</a></b></div>


# Enterprise Business Intelligence Architecture

This scenario shows how data can be ingested into a cloud environment from an on-premises data warehouse of an Agricultural Industry, then served using a business intelligence (BI) model. This approach could be an end goal or a first step toward full modernization with cloud-based components.

The following steps build on the Azure Synapse Analytics end-to-end scenario. It uses Azure Pipelines to ingest data from a SQL database into Azure Synapse SQL pools, then transforms the data for analysis.

![image](https://user-images.githubusercontent.com/76818972/209816208-5e03156f-9865-45f9-8c19-a1b949d1d469.png)

# Workflow

Data source
The source data is located in an SQL Server database in Azure. To simulate the on-premises environment, deployment scripts for this scenario provision an Azure SQL database. The AdventureWorks sample database is used as the source data schema and sample data. For information on how to copy data from an on-premises database, see copy and transform data to and from SQL Server.
Ingestion and data storage
Azure Data Lake Gen2 is used as a temporary staging area during data ingestion. You can then use PolyBase to copy data into an Azure Synapse dedicated SQL pool.

Azure Synapse Analytics is a distributed system designed to perform analytics on large data. It supports massive parallel processing (MPP), which makes it suitable for running high-performance analytics. Azure Synapse dedicated SQL pool is a target for ongoing ingestion from on-premises. It can be used for further processing, as well as serving the data for Power BI through DirectQuery.

Azure Pipelines is used to orchestrate data ingestion and transformation within your Azure Synapse workspace.

Analysis and reporting
The data-modeling approach in this scenario is presented by combining the enterprise model and BI Semantic model. The enterprise model is stored in an Azure Synapse dedicated SQL pool, and the BI Semantic model is stored in Power BI Premium capacities. Power BI accesses the data via DirectQuery.
