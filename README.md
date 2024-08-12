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


## 16) Wait
The Wait activity in Azure Data Factory (ADF) is used to pause the execution of a pipeline for a specified amount of time. This activity is useful in scenarios where you need to introduce delays or wait for certain conditions to be met before proceeding with the next steps in your data workflow. 

![image](https://github.com/user-attachments/assets/d36cc4a8-87d5-4d81-903e-280f9fd88650)

## 17) Validation
The Validation activity in Azure Data Factory (ADF) is used to check whether certain conditions or prerequisites are met before proceeding with the execution of subsequent activities in a pipeline. This activity is essential for ensuring data integrity, verifying the availability of required resources, and preventing errors during the data processing workflow.

![image](https://github.com/user-attachments/assets/5776fb04-859d-41f4-9087-dd18e609193b)

![image](https://github.com/user-attachments/assets/508c134f-6d67-4303-b131-8463711cd61f)

![image](https://github.com/user-attachments/assets/6a72c0e4-ab15-4b1d-afd7-388a1f7366bb)

![image](https://github.com/user-attachments/assets/49fc1465-cea9-437b-9e0e-480ab8c9339a)

![image](https://github.com/user-attachments/assets/d2583618-7f2c-4e39-a2e5-368631ddfc2e)

![image](https://github.com/user-attachments/assets/4a2611e4-09af-4d6e-bccd-6cf0ba46fb06)

![image](https://github.com/user-attachments/assets/ed902ec2-d049-4c72-9a9b-e4b1a51de751)

![image](https://github.com/user-attachments/assets/ababbcc5-a970-4217-b671-120293238835)

![image](https://github.com/user-attachments/assets/8d682d19-25f9-4915-ab65-c82847681470)


## 18) Filter
In Azure Data Factory (ADF), the Filter activity is used to process and filter data based on specific conditions. This can be particularly useful for data transformations and pipeline orchestration. 

![image](https://github.com/user-attachments/assets/b5538b0c-07c1-49e8-8578-2fce10a01085)

![image](https://github.com/user-attachments/assets/1aec0690-e0d7-4d4d-841a-f5109e1abfaf)

![image](https://github.com/user-attachments/assets/7d63d8b0-40e3-4d25-94c6-1595266fb9e7)


## 19) Dataflow - Join and Aggregate

![image](https://github.com/user-attachments/assets/5c1371fc-6361-48f5-9357-ec462740c43c)

![image](https://github.com/user-attachments/assets/fea509e0-ecdd-4853-bc84-10cd78b5fe84)

![image](https://github.com/user-attachments/assets/0bad7ce3-3e29-44fa-991d-b498dd269919)

![image](https://github.com/user-attachments/assets/b8bd3571-e0cc-4b64-843e-30c7c2a79de8)

![image](https://github.com/user-attachments/assets/2dedf216-301a-4391-bd5a-7bcfe9f2a3c8)

![image](https://github.com/user-attachments/assets/6cea0506-2e7b-4ae1-8bbb-13e5574c583c)

![image](https://github.com/user-attachments/assets/2defdc32-9009-45e0-be8f-975ede4f9e8b)

![image](https://github.com/user-attachments/assets/281b574b-416e-4a59-a401-2fcddcc5a7a7)

After creating the dataflow, we need to trigger/debug through a pipeline.

![image](https://github.com/user-attachments/assets/597aeb9a-45d5-4660-8e9d-dad69718e5b6)


## 20) Dataflow - Conditional Split

![image](https://github.com/user-attachments/assets/0a0eac18-7792-47c6-92a8-a40392c2f003)

![image](https://github.com/user-attachments/assets/1f2dc5d5-b061-4b3a-b5ae-b4baad9e8284)

## 21) Dataflow - Exists

![image](https://github.com/user-attachments/assets/c17ae6a5-7b4c-486f-b317-f55420f3829a)

![image](https://github.com/user-attachments/assets/92c1d233-c0af-455d-bb3e-81ac27f84e24)

## 22) Dataflow - Select

![image](https://github.com/user-attachments/assets/3f15a9c6-be82-454f-aec4-20568357c4a5)

![image](https://github.com/user-attachments/assets/990c672d-17e5-495b-922c-35e80decfcdc)

![image](https://github.com/user-attachments/assets/ec62c28d-3192-4ff3-a3af-bff73aa81073)


## 23) Dataflow - Filter and Sort

![image](https://github.com/user-attachments/assets/99058e5f-a830-4cd0-a595-9380132c3414)

![image](https://github.com/user-attachments/assets/68bb4ec4-03bb-4535-b072-90bef9ae127e)

![image](https://github.com/user-attachments/assets/e0f5c84a-e02e-4cb6-9bbc-263837b8c772)

## 24) Dataflow - Union and Derived Column

![image](https://github.com/user-attachments/assets/dcf47df2-076d-49ac-9993-3aae48d32a19)

![image](https://github.com/user-attachments/assets/56966a7f-fe63-48ea-b594-5dce1ca07bb5)

![image](https://github.com/user-attachments/assets/a9c071a1-85da-4856-91b1-7a2ea0944862)

![image](https://github.com/user-attachments/assets/963a60f2-1bad-4e86-9b5e-ca05f8f4ff0b)


## 25) Dataflow - Surrogate Key

![image](https://github.com/user-attachments/assets/4d1c6715-dfe8-41a1-beab-8b1fd74bd600)

![image](https://github.com/user-attachments/assets/d2dba020-b0c1-406e-b66e-a94243462f36)

![image](https://github.com/user-attachments/assets/d1938d5d-8a2d-4683-bd1e-513c5159662c)


## 26) Dataflow - Pivot

![image](https://github.com/user-attachments/assets/4dba2b54-565f-49a1-9f2c-2a683e1cc8b8)

![image](https://github.com/user-attachments/assets/b2b84a96-16bf-4934-9d69-2bfdaf503722)

![image](https://github.com/user-attachments/assets/dfa1f1d1-14c8-4194-afad-d64a07f7cdd1)

![image](https://github.com/user-attachments/assets/30d7888d-90cc-4708-a140-c7987056ead9)

![image](https://github.com/user-attachments/assets/9a7d90e9-211e-44ea-afa6-036b47a6a331)

![image](https://github.com/user-attachments/assets/b7a1a861-33e1-499b-8e3b-33c95fe3cc82)


## 27) Dataflow - Unpivot

![image](https://github.com/user-attachments/assets/0b54f711-eded-4231-8ede-7332389a4275)

![image](https://github.com/user-attachments/assets/e18c6cd5-86f2-4921-bb8d-fa59dde33eb6)

![image](https://github.com/user-attachments/assets/56db0965-36d0-4a5e-903c-7dbaa5d3a7f5)

![image](https://github.com/user-attachments/assets/132ad22d-1e58-43f9-9cf3-c6f9ca94b036)

![image](https://github.com/user-attachments/assets/ac7bf3bf-c67e-4227-9bcc-29126fd02830)

![image](https://github.com/user-attachments/assets/b7370549-065d-4522-bbac-15f33c3e0d22)


## 28) Dataflow - Window Functions

![image](https://github.com/user-attachments/assets/e755fe57-94d1-42f2-aab0-b1f4abd8eebd)

![image](https://github.com/user-attachments/assets/7e17480e-e4ea-4da9-8170-d42fae4b230c)

![image](https://github.com/user-attachments/assets/318ba57e-5d24-4e6c-88d8-cce9faa71137)

![image](https://github.com/user-attachments/assets/e60e26ec-cd4c-4a4a-a341-b868e1279e4d)

![image](https://github.com/user-attachments/assets/70312b68-0785-4a19-b2e4-39fc441a8a1b)

![image](https://github.com/user-attachments/assets/a99e9959-573f-41e0-922d-93e7bfd54577)

![image](https://github.com/user-attachments/assets/91b07024-8bfc-4235-8a87-7371d761bb19)



## 29) Dataflow - Alter Row (Implemented SCD Type 1)

![image](https://github.com/user-attachments/assets/5802ee85-b306-4ed0-915d-69ea62476ede)

![image](https://github.com/user-attachments/assets/aa447c70-b72d-47c0-94d3-464999823e70)

![image](https://github.com/user-attachments/assets/7f344f55-e87e-447e-94ea-40d417c2922d)

![image](https://github.com/user-attachments/assets/a56bec8b-d863-41f4-8551-e365a7a6a2f5)

![image](https://github.com/user-attachments/assets/cf0c0d4f-8ece-4e25-91e1-493b00badcc4)

Slowly Changing Dimensions (SCD) are a common data warehousing concept used to manage and track changes in dimension data over time. The approach you take depends on how you want to handle and store historical data changes. 

SCD Type 0: Retain Original
Definition: No historical data is maintained. The dimension record is updated with new values, and previous values are lost.
Use Case: Suitable for dimensions where changes are rare, and historical accuracy is not crucial.
Example: A dimension with a fixed attribute that does not need historical tracking.

SCD Type 1: Overwrite
Definition: Updates the existing record with new values, overwriting the old values without keeping historical data.
Use Case: When historical changes are not important, and only the current value is needed.
Example: Updating a customer's address where you do not need to keep previous addresses.

SCD Type 2: Add New Row
Definition: Adds a new record for each change in the dimension attributes, maintaining historical data. Typically involves using start and end dates or version numbers to track changes.
Use Case: When you need to track the history of changes to dimension attributes and maintain a complete history of changes.
Example: Tracking changes in a customer’s status over time, such as a promotion or change in customer type.

SCD Type 3: Add New Attribute
Definition: Adds new columns to the existing record to store historical values, allowing the storage of current and previous values in the same record.
Use Case: When only a limited history of changes is needed, and the focus is on tracking a specific number of previous values.
Example: Storing a customer’s current and previous address in separate columns.

SCD Type 4: Historical Table
Definition: Maintains current dimension data in one table and historical data in another table. The current table holds the most recent version, while the historical table tracks all changes.
Use Case: When you want to separate current and historical data, making it easier to manage and query current data while preserving historical changes.
Example: Storing active employee records in one table and all historical employee changes in another table.

SCD Type 6: Hybrid (Combination of Type 1, Type 2, and Type 3)
Definition: Combines aspects of Types 1, 2, and 3. It retains the current value (Type 1), keeps historical records (Type 2), and may also store previous values in separate attributes (Type 3).
Use Case: When you need to manage different aspects of historical and current data simultaneously, combining features from multiple SCD types.
Example: Keeping current address, historical addresses, and tracking the most recent change date.


SCD Type 7: Extension of Type 6
Definition: Adds a layer of data versioning, often integrating Type 6 with additional mechanisms to handle changes and historical data more comprehensively.
Use Case: For advanced scenarios where detailed version tracking and change management are required.
Example: Combining Type 2 and Type 3 approaches with additional fields or tables for detailed historical tracking.










































































































































   
   



