# Azure-Data-Factory-Practices
Azure Data Factory Pipelines &amp; Dataflows - Data Integration and Transformation processes using Azure Data Factory (ADF).

##  1) Copy Data
Copy Data Activity in Azure Data Factory (ADF) is a fundamental component used for moving data from a source to a destination. It supports a wide range of scenarios, making it a versatile tool in data integration and ETL (Extract, Transform, Load) processes like - Migrating data from an on-premises SQL Server database to an Azure SQL Database or Azure Blob Storage, Aggregating data from various databases, files, From APIs into an Azure Data Lake or Azure Synapse Analytics for comprehensive reporting and analytics, Copying raw transactional data from an operational database to a staging area in Azure Data Lake where it can be further transformed and cleaned before loading into a data warehouse, Copying streaming data from IoT devices or social media feeds to Azure Stream Analytics or Azure Blob Storage for real-time processing, loading data from azure data lake gen2 (adls) files to azure sql database or unloading data from azure sql database to files in blob or adls. etc.

### i) Create Source Datasets-Linked Services and Sink Datasets-Linked Services:
   Choose a dataset to specify the location and structure of your data within a data store -> Select Format -> Set Dataset Name -> Choose/Create Linked Service (Name of Linked Service + Integration Runtime + Choose Azure subscription/ Enter Manually + Choose/Create Storage account name + Test Connection + Create) -> Choose File Path -> Select First Row as Header as per requirement -> Choose Import Schema Option as per requirement -> OK

![image](https://github.com/user-attachments/assets/4c5c3263-bce9-4dfe-8eb7-23ee91bf771e)
![image](https://github.com/user-attachments/assets/8ca1b16b-fbfa-4545-a325-5a531774eb82)

### ii) In Mapping:
   Select correct Type of Source and Destination
![image](https://github.com/user-attachments/assets/9a9ae005-0d24-4fee-a28b-3a6677f27ca0)

### iii) Validate and Debug the Pipeline/Add Trigger(Trigger Now/Add Trigger)
![image](https://github.com/user-attachments/assets/117304a7-b669-4b01-adb2-fae7a26d119f)

### For API calling - 
![image](https://github.com/user-attachments/assets/da138d3b-1e13-4392-b3f4-c0ee8364313b)
![image](https://github.com/user-attachments/assets/af15e3f7-6790-478b-92b2-0a8fa86a5928)
![image](https://github.com/user-attachments/assets/f000d2c8-c4c2-4b0d-888a-4ce3b7be2624)


##  2) Delete
Delete Activity in Azure Data Factory (ADF) is used to remove data from a specified data store. It is a key component for managing and maintaining data, especially in scenarios where data needs to be cleaned, purged, or managed as part of an ETL (Extract, Transform, Load) workflow.

### i) Create Source Datasets-Linked Services

![image](https://github.com/user-attachments/assets/45394cdc-71e0-4135-9e83-15cfcbe6147c)

### ii) In Logging settings - Create Logging account linked service and (Choose Folder Path for containing the deleted file names - optional)

![image](https://github.com/user-attachments/assets/ccb503a2-a4d1-45ef-ab5e-32b7771ba591)

### iii) Validate and Debug the Pipeline/Add Trigger(Trigger Now/Add Trigger)

![image](https://github.com/user-attachments/assets/38cf8dfa-859e-4ec1-b93b-4374929f095f)

## 3) Web
Web Activity in Azure Data Factory (ADF) allows you to make HTTP requests to external services, APIs, or endpoints as part of your data workflows. This activity is versatile and can be used in a variety of scenarios where you need to interact with web services, trigger external processes, or integrate with other systems.

### i) In settings put the URL and Choose the method

![image](https://github.com/user-attachments/assets/52ca9d90-66b2-40da-8e6b-df388defd36a)

### ii) Validate and Debug the Pipeline/Add Trigger(Trigger Now/Add Trigger)

![image](https://github.com/user-attachments/assets/97962793-284d-4380-9684-f09c6c546ce7)

## * Parameterization in Loading data and Unloading data from source to destination : Steps : *

![image](https://github.com/user-attachments/assets/b60ae0c3-082d-4571-a72d-567c7e92e83f)
![image](https://github.com/user-attachments/assets/ca4e25d9-ecee-4022-ae2a-b1ba3698a168)
![image](https://github.com/user-attachments/assets/2e449e24-cdc2-4a34-9c94-ae717dbcb14c)
![image](https://github.com/user-attachments/assets/577bc13c-78ae-49ce-96c1-216d3f872ca1)
![image](https://github.com/user-attachments/assets/d97b8429-2769-470a-b7f2-cd7b725c7f5f)
![image](https://github.com/user-attachments/assets/3d539322-c464-4d31-a3c0-7a5d27b0ca53)
![image](https://github.com/user-attachments/assets/5a08d815-505a-42e3-b7b4-a5517c91f278)
![image](https://github.com/user-attachments/assets/c54d25db-6839-43b2-8c76-01e2d0f6eb65)
![image](https://github.com/user-attachments/assets/95ada332-3ced-4366-a83b-01ca075f444c)



















   
   



