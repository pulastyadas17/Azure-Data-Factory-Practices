# Azure-Data-Factory-Practices
Azure Data Factory Pipelines &amp; Dataflows - Data Integration and Transformation processes using Azure Data Factory (ADF).

##  Copy Data
### Copy Data Activity in Azure Data Factory (ADF) is a fundamental component used for moving data from a source to a destination. It supports a wide range of scenarios, making it a versatile tool in data integration and ETL (Extract, Transform, Load) processes like - Migrating data from an on-premises SQL Server database to an Azure SQL Database or Azure Blob Storage, Aggregating data from various databases, files, From APIs into an Azure Data Lake or Azure Synapse Analytics for comprehensive reporting and analytics, Copying raw transactional data from an operational database to a staging area in Azure Data Lake where it can be further transformed and cleaned before loading into a data warehouse, Copying streaming data from IoT devices or social media feeds to Azure Stream Analytics or Azure Blob Storage for real-time processing etc.

Basic Steps:

1) Create Source Datasets-Linked Services and Sink Datasets-Linked Services:
   Choose a dataset to specify the location and structure of your data within a data store -> Select Format -> Set Dataset Name -> Choose/Create Linked Service (Name of Linked Service + Integration Runtime + Choose Azure subscription/ Enter Manually + Choose/Create Storage account name + Test Connection + Create) -> Choose File Path -> Select First Row as Header as per requirement -> Choose Import Schema Option as per requirement -> OK

2) In Mapping:
   Select correct Type of Source and Destination

3) Validate and Debug the Pipeline/Add Trigger(Trigger Now/Add Trigger)

   
   



