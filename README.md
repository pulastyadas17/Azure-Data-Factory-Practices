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
### step 01 :
![image](https://github.com/user-attachments/assets/b60ae0c3-082d-4571-a72d-567c7e92e83f)
### step 02 :
![image](https://github.com/user-attachments/assets/ca4e25d9-ecee-4022-ae2a-b1ba3698a168)
### step 03 :
![image](https://github.com/user-attachments/assets/2e449e24-cdc2-4a34-9c94-ae717dbcb14c)
### step 04 :
![image](https://github.com/user-attachments/assets/577bc13c-78ae-49ce-96c1-216d3f872ca1)
### step 05 :
![image](https://github.com/user-attachments/assets/d97b8429-2769-470a-b7f2-cd7b725c7f5f)
### step 06 :
![image](https://github.com/user-attachments/assets/3d539322-c464-4d31-a3c0-7a5d27b0ca53)
### step 07 :
![image](https://github.com/user-attachments/assets/5a08d815-505a-42e3-b7b4-a5517c91f278)
### step 08 :
![image](https://github.com/user-attachments/assets/c54d25db-6839-43b2-8c76-01e2d0f6eb65)
### step 09 :
![image](https://github.com/user-attachments/assets/95ada332-3ced-4366-a83b-01ca075f444c)

## 4) Execute Pipeline
The Execute Pipeline activity in Azure Data Factory (ADF) allows you to invoke another pipeline from within a parent pipeline. This activity is particularly useful for organizing, reusing, and managing complex workflows in ADF.

### i) In settings choose Invoked Pipeline and Wait on Completion for completing the previous pipeline activity. Then Debug/Trigger Now

![image](https://github.com/user-attachments/assets/b2c7f373-d4d6-459d-8b0c-9538212bc2ab)

![image](https://github.com/user-attachments/assets/6c358fdb-e0ab-4332-a96d-225f9aedb48c)

![image](https://github.com/user-attachments/assets/0ab5796f-b760-4979-96dd-d6a7e51d4e59)

![image](https://github.com/user-attachments/assets/b33730fc-d6fe-4a39-aae9-ce94043278ea)

![image](https://github.com/user-attachments/assets/f661347d-3a33-4420-978b-6e489380c3bf)



## 5) Set Variable
The Set Variable activity in Azure Data Factory (ADF) is used to define and update the values of variables within a pipeline. This activity is highly useful for managing and controlling the flow of data processing workflows by storing dynamic values that can be used later in the pipeline.

### i) In settings the name and value should be given. Then Debug/Trigger Now as per desired activity. Here date and time has been concatenated in the output.

![image](https://github.com/user-attachments/assets/a365a0ee-a9c2-4998-8d02-57f9140d629c)

![image](https://github.com/user-attachments/assets/3c942ce9-3271-442c-9271-53c933879046)

![image](https://github.com/user-attachments/assets/9be75a32-c9f0-41e3-9b00-0df454d43df0)

![image](https://github.com/user-attachments/assets/4eeeecf8-88b6-4115-9cdd-7f2efda5e142)

![image](https://github.com/user-attachments/assets/f4893ac6-f680-4d0a-ba9a-461374452d2a)

![image](https://github.com/user-attachments/assets/94167e7e-a4a0-468f-ade4-5010a6a052d0)

![image](https://github.com/user-attachments/assets/bcbf1cd3-a4f9-4173-af39-655da1098025)

## 6) Append Variable
The Append Variable activity in Azure Data Factory (ADF) is used to add new values to an existing array variable within a pipeline. This is particularly useful when you need to build up a collection of items, such as a list of files, database records, or error messages, during the execution of a pipeline. 

### i) In settings the name and value should be given. Then Debug/Trigger Now as per desired activity. Here date and time has been concatenated in the output.

![image](https://github.com/user-attachments/assets/61cd1260-5c4a-4ee8-a85c-3c97640baba6)

![image](https://github.com/user-attachments/assets/1319778d-64e8-4595-b92d-08b57ecafc8b)

![image](https://github.com/user-attachments/assets/36d55203-c914-45c2-a749-74787fd1356e)

![image](https://github.com/user-attachments/assets/77747fc8-6de3-4a4c-93e7-32b6ec9e3652)

![image](https://github.com/user-attachments/assets/f1db0d29-2570-4b3b-9c89-6ca62defe267)

## 7) Get Metadata
The Get Metadata activity in Azure Data Factory (ADF) is used to retrieve metadata information about data stored in various data sources. This activity allows you to gain insights into the structure, properties, and characteristics of your data, which can be critical for building dynamic and flexible ETL processes.

### i) In settings we need to choose the dataset and linked service. After that we need to select the field list argument as per requirement. Then Debug/Trigger Now as per desired activity. Here date and time has been concatenated in the output.

![image](https://github.com/user-attachments/assets/be679d0f-b6ed-407f-8b21-74638456da28)

![image](https://github.com/user-attachments/assets/bee9309f-f158-46fa-b546-cf5d6ad7862f)

![image](https://github.com/user-attachments/assets/de8d8394-4e67-41a0-b47e-3befd5499193)

![image](https://github.com/user-attachments/assets/05b7a40a-5df9-43e6-a888-ba9fa4486e7f)

![image](https://github.com/user-attachments/assets/52096db5-1af6-446e-b8f4-376e484139e3)

![image](https://github.com/user-attachments/assets/0e47ef4b-cf3e-4092-a769-f4b0f2619001)

![image](https://github.com/user-attachments/assets/4dba505e-4ea9-41de-8b56-2c19a710f74f)


## 8) Fail
The Fail Activity in Azure Data Factory (ADF) is used to intentionally fail a pipeline or mark a specific point in the pipeline as failed based on certain conditions or logic. This activity is useful for managing error handling, enforcing business rules, and controlling the flow of a pipeline.

### i) In settings we need to provide the fail message and error code. Then Debug/Trigger Now as per desired activity.

![image](https://github.com/user-attachments/assets/121456ff-9764-4536-b0a4-aeec2b367c5a)


## 9) Script
The Script Activity in Azure Data Factory (ADF) allows you to run SQL scripts against databases within your data integration workflows. This activity is particularly useful for performing complex database operations that cannot be easily achieved through standard data transformation activities in ADF.

![image](https://github.com/user-attachments/assets/f9f109c0-99a5-41d3-a232-2d549350c842)

![image](https://github.com/user-attachments/assets/c2c4b5ea-128e-457e-86df-d074f0544127)

![image](https://github.com/user-attachments/assets/256e235a-4907-43c4-8b47-dfb1b9e67c28)


## 10) Stored Procedure
The Stored Procedure activity in Azure Data Factory (ADF) allows you to execute stored procedures in a SQL database as part of your data integration and ETL (Extract, Transform, Load) processes. This activity is useful for performing complex data operations, executing business logic, or handling tasks that require multiple steps within a database.

![image](https://github.com/user-attachments/assets/c83b17aa-49df-43f5-90ac-67b2f93efb7e)

![image](https://github.com/user-attachments/assets/0678511f-c8e8-4422-9d21-2debe9101700)

![image](https://github.com/user-attachments/assets/797cbdff-7853-4d63-a06a-ba2fc0e44721)

![image](https://github.com/user-attachments/assets/2e4eac00-49cb-4f29-9e05-8b9c6c9a0b71)

![image](https://github.com/user-attachments/assets/7e714c87-02cf-4b97-9610-df9d8a6300bd)


## 11) For Each
The ForEach activity in Azure Data Factory (ADF) is used to iterate over a collection of items, such as an array, and execute a set of activities for each item in the collection. This activity is essential for scenarios where you need to perform repetitive tasks across multiple data elements or entities. 

![image](https://github.com/user-attachments/assets/0859471e-e789-4d8b-9319-4c019c43b972)

![image](https://github.com/user-attachments/assets/ecdafb0a-c6d2-4515-bb9f-9ff34667d03c)

![image](https://github.com/user-attachments/assets/5700142d-59f2-4fc6-abfd-b82e31edc94a)

![image](https://github.com/user-attachments/assets/01ab2488-6c73-471a-b60e-1685f6365f2a)

![image](https://github.com/user-attachments/assets/5dba574c-5665-4f5f-b827-771199f7cefb)


## 12) If
The If Condition activity in Azure Data Factory (ADF) allows you to introduce conditional logic into your data workflows. This activity evaluates a Boolean expression and directs the pipeline flow based on whether the expression evaluates to true or false. This is especially useful for creating dynamic and flexible data pipelines that can adapt to different conditions or scenarios.

![image](https://github.com/user-attachments/assets/f0893ed0-55e3-446a-be42-68ec8cc465d6)

![image](https://github.com/user-attachments/assets/14d72019-6c9c-4ae8-b9e8-4c1fda143a0c)

![image](https://github.com/user-attachments/assets/989ace04-035a-4c52-98e9-c995c004ed39)

![image](https://github.com/user-attachments/assets/55d80d29-80b6-4b5c-ac86-cf228af16482)

![image](https://github.com/user-attachments/assets/ed832b38-0a29-4c5e-befa-37824fc4bad5)

![image](https://github.com/user-attachments/assets/f7b9b443-675c-40ad-a893-ffd95e809fcd)

![image](https://github.com/user-attachments/assets/28d27bc8-ca2f-478a-b951-68856c22e86f)

![image](https://github.com/user-attachments/assets/46c2d133-b59c-46d1-9174-5e3ef4ff552c)

![image](https://github.com/user-attachments/assets/6a8dee28-974d-4d13-aca5-cbd4e4626ec1)

![image](https://github.com/user-attachments/assets/512457ef-ddbb-4c81-9d43-45cd1afab060)


## 13) Switch
The Switch activity in Azure Data Factory (ADF) is used to implement branching logic based on the value of a specific expression. Unlike the If Condition activity, which only handles true/false logic, the Switch activity allows you to evaluate multiple possible values and execute different activities depending on the outcome. This is particularly useful for scenarios where you have multiple conditions to check, each leading to a different set of actions.

![image](https://github.com/user-attachments/assets/27b709d2-96af-4994-94ee-ce5770f59566)

![image](https://github.com/user-attachments/assets/0c642f15-3ea0-4c18-aa8b-c814cc44c867)

![image](https://github.com/user-attachments/assets/b41f25cb-56e2-482a-930b-dd27367fafdb)

![image](https://github.com/user-attachments/assets/6ae9bcad-20d6-47fc-a93f-720b40b7eacb)

![image](https://github.com/user-attachments/assets/f2bfe6e3-7fba-4ae3-a7e0-1ba252360eae)

## 14) Until
The Until activity in Azure Data Factory (ADF) is used to repeatedly execute a set of activities until a specified condition evaluates to true. This is useful for scenarios where you need to wait for a specific event or condition to occur before proceeding with the rest of the pipeline.Scenarios like - Continuously checking for the availability of a file or data before proceeding with the pipeline,Waiting for an external process or job to complete before continuing with the pipeline,Repeating an action until a specific timeout condition is met.

![image](https://github.com/user-attachments/assets/07be417e-faa2-4817-9111-e8331b80b9ee)

![image](https://github.com/user-attachments/assets/ee954b8e-2322-411c-a4b3-d9eb5216042d)

![image](https://github.com/user-attachments/assets/1bb0a715-5a15-4f45-8978-880785296683)

![image](https://github.com/user-attachments/assets/8edaa884-9aac-4f09-8681-1cd6ef015367)

## 15) Lookup
The Lookup activity in Azure Data Factory (ADF) is used to retrieve data from a data source and make it available for use in other activities within the pipeline. This activity is particularly useful for fetching configuration settings, controlling the flow of the pipeline based on data, or retrieving specific values that guide the pipeline's logic.The Lookup activity can fetch a list of IDs, file names, or date ranges from a database, which can then be passed as parameters to other activities like Copy Data, ForEach, or Execute Pipeline.
Benefit: Facilitates dynamic parameterization, enabling more flexible and reusable pipeline designs that can handle varying inputs or scenarios.
Lookup activity can be used to check if certain data exists in a table or if a specific condition is met (e.g., ensuring that today's data has been loaded). If the condition is not met, the pipeline can be configured to either stop, retry, or take an alternative path.
If you need to loop through a list of items (e.g., filenames, IDs), the Lookup activity can retrieve the list from a database or file. This list can then be passed to a ForEach activity for iterative processing.
Benefit: Enables complex looping mechanisms in pipelines, allowing for batch processing of multiple items dynamically.
The Lookup activity in ADF is a versatile tool for retrieving data and making real-time decisions within a pipeline. Whether you're fetching configuration settings, controlling pipeline flow, or performing data validation, the Lookup activity helps you build dynamic and adaptable data integration solutions that respond to the current state of your data and environment.


![image](https://github.com/user-attachments/assets/101240b6-8a58-4fe1-91a7-6e1f8f949161)

![image](https://github.com/user-attachments/assets/d52ebad4-ccef-47a2-83c7-ebd7331e93ea)

![image](https://github.com/user-attachments/assets/918fc03e-15f5-4d61-9c50-77f1d7bad67a)

![image](https://github.com/user-attachments/assets/a5e34b6d-1df0-4489-be85-ef7de62b3227)

![image](https://github.com/user-attachments/assets/53d28c17-640c-4915-9c82-075edf626f58)

Here we want to delete the values of ID field present in resign table from our actual emp database.


















































































   
   



