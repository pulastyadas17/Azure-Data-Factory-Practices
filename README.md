# Azure-Data-Factory-Practices
Azure Data Factory Pipelines &amp; Dataflows - Data Integration and Transformation processes using Azure Data Factory (ADF).

##  1) Copy Data
Copy Data Activity in Azure Data Factory (ADF) is a fundamental component used for moving data from a source to a destination. It supports a wide range of scenarios, making it a versatile tool in data integration and ETL (Extract, Transform, Load) processes like - Migrating data from an on-premises SQL Server database to an Azure SQL Database or Azure Blob Storage, Aggregating data from various databases, files, From APIs into an Azure Data Lake or Azure Synapse Analytics for comprehensive reporting and analytics, Copying raw transactional data from an operational database to a staging area in Azure Data Lake where it can be further transformed and cleaned before loading into a data warehouse, Copying streaming data from IoT devices or social media feeds to Azure Stream Analytics or Azure Blob Storage for real-time processing etc.

### i) Create Source Datasets-Linked Services and Sink Datasets-Linked Services:
   Choose a dataset to specify the location and structure of your data within a data store -> Select Format -> Set Dataset Name -> Choose/Create Linked Service (Name of Linked Service + Integration Runtime + Choose Azure subscription/ Enter Manually + Choose/Create Storage account name + Test Connection + Create) -> Choose File Path -> Select First Row as Header as per requirement -> Choose Import Schema Option as per requirement -> OK

![image](https://github.com/user-attachments/assets/4c5c3263-bce9-4dfe-8eb7-23ee91bf771e)
![image](https://github.com/user-attachments/assets/8ca1b16b-fbfa-4545-a325-5a531774eb82)

### ii) In Mapping:
   Select correct Type of Source and Destination
![image](https://github.com/user-attachments/assets/9a9ae005-0d24-4fee-a28b-3a6677f27ca0)

### iii) Validate and Debug the Pipeline/Add Trigger(Trigger Now/Add Trigger)
![image](https://github.com/user-attachments/assets/117304a7-b669-4b01-adb2-fae7a26d119f)

##  2) Delete
Delete Activity in Azure Data Factory (ADF) is used to remove data from a specified data store. It is a key component for managing and maintaining data, especially in scenarios where data needs to be cleaned, purged, or managed as part of an ETL (Extract, Transform, Load) workflow.

### i) Create Source Datasets-Linked Services

![image](https://github.com/user-attachments/assets/45394cdc-71e0-4135-9e83-15cfcbe6147c)

### ii) In Logging settings - Create Logging account linked service and (Choose Folder Path for containing the deleted file names - optional)

![image](https://github.com/user-attachments/assets/ccb503a2-a4d1-45ef-ab5e-32b7771ba591)

### iii) Validate and Debug the Pipeline/Add Trigger(Trigger Now/Add Trigger)

![image](https://github.com/user-attachments/assets/38cf8dfa-859e-4ec1-b93b-4374929f095f)




   
   



