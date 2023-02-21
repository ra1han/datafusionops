# Workshop Challenges

## Prerequisites
- Dynamics 365 Sales Environment
- Azure Subscription under the same tenant as Dynamics 365 Sales 
- Two csv files - our_sales.csv and their_sales.csv

## Building Datalake Raw/Bronze Layer
- Copy Account table to Synapse lake database: Go to https://make.powerapps.com/. Create Synapse Link for Dataverse to copy the Account table to Synapse. 
- Copy their_sales.csv to Synapse lake database: Go to https://make.powerapps.com/. Import the their_sales.csv as a table to dataverse. Create Synapse Link for Dataverse to copy the their_sales table to Synapse.
- Copy our_sales.csv to Synapse lake database: Go to Azure Synapse Workspace. Import the datalake.ipynb notebook to Azure Synapse. Create the raw lake database and our_sales table using the notebook.

End of it we shall have 3 tables in Lake database in Azure Synapse - Account, our_sales and their_sales

## Building Datalake Standardised/Silver Layer
- Load CSV files as external table in Serverless SQL pool
- Create a dimensional model in Serveour_sales.csv in rless SQL pool

## Building Datalake Curated/Gold Layer
- Create a Power BI report from the dimensional model
- Publish the report to Dynamics Sales portal 

## Building Visualisation
