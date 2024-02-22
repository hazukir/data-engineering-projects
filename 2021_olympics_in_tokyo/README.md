# Project Workflow

💡Integration & storage with ADF & ADLS Gen2
I integrated source files with Azure Data Factory by pulling them from GitHub and storing them in a directory inside a container in ADLS Gen2. I was able to perform some basic data type transformations in ADF, which saved me some work in Databricks.

💡Storage in ADLS Gen2
I stored the transformed data back in another directory inside the same container in ADLS Gen2. Additionally, I used Azure Apps to create an app, allowing me to establish a connection between ADLS Gen2 and Azure Databricks with the generated IDs (ClientID, TenantID, & SecretID). The "Storage Blob Data Contributor" role was required to allow Azure Databricks to access the Storage Account.

💡Basic Transformations with ADB
I utilized Azure Databricks to perform basic transformations with Pyspark.

💡Azure Azure Synapse Analytics
I used Azure Synapse Analytics to access the transformed data in ADLS using the External Table option. Out of curiosity, I attempted to perform an update in one of the tables and discovered that DML is not allowed in External tables.

💡Connecting Synapse Serverless SQL Pool to SSMS
Finally, I connected the Synapse Serverless SQL Pool to SSMS in order to manipulate the data. I found that I had to enable SQL Admin user credentials in SSMS first before I could see the data. Thanks to the "Synapse - SQL Admin" blog post by Joe Gill, I was able to overcome this challenge.
