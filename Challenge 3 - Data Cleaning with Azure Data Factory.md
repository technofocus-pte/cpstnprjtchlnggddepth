# Challenge 3 - Data Cleaning with Azure Data Factory

**Objective**  
Use ADF pipeline to clean and transform fleet data and load into
fleet_cleaned_data.

**Steps:**

1.  Create Azure PostgreSQL connection in ADF studio linked service and
    **Test Connection** to verify .Create with below details.

   - Name: +++PostgreSQLLinkedService+++
   - Server Name: Select your PostgreSQL server name (e.g., <yourserver>.postgres.database.azure.com).
   - Version : **1.0**
   - Database Name: **flexibleserverdb**.
   - Authentication: Provide the username and password.(+++citus+++ – +++Fhtest208+++)
   - Encryption Method : **SSL**
   - Click **Test Connectio**n to verify.

2.  Create pipeline with the name – +++IngestBlobToPostgreSQL+++

    - Create Copy data action with the name : +++blobtopostgresql+++

    - Source data set (New) – Azure blob storage with Delimited text and
      set below properties

      - Name : +++blobfleetdata+++

      - Linked service – Azure blob linked service

      - File path ->Container-> Directory-> File path->
        **fleetdata** folder-> **fleet_data.csv** file

    - Create new Sink dataset –

- Name : +++AzurePostgreSqlcontosofleettable+++

- Linked Service : **PostgreSQLLinkedService**

  - Table name : Search for **public.contosofleet** and select it.

   - Load from Blob to staging table

3.  Create data flow with cleaning rules:


4.  Load results into **fleet_cleaned_data**

**Success Criteria:**

- Pipeline runs successfully

- Data shows cleaned values in the destination table
