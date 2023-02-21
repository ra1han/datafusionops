# Workshop Challenges

## Prerequisites
- Dynamics 365 Sales Environment
- Azure Subscription under the same tenant as Dynamics 365 Sales 
- Two csv files - our_sales.csv and their_sales.csv

## Building Datalake Raw/Bronze Layer
- Copy Account table to Synapse lake database: Go to https://make.powerapps.com/. Create Synapse Link for Dataverse to copy the Account table to Synapse. 
- Copy their_sales.csv to Synapse lake database: Go to https://make.powerapps.com/. Import the their_sales.csv as a table to dataverse. Create Synapse Link for Dataverse to copy the their_sales table to Synapse.
- Copy our_sales.csv to Synapse lake database: Go to Azure Synapse Workspace. Import the datalake.ipynb notebook to Azure Synapse. Create the raw lake database and our_sales table using the notebook.

End of it we shall have 3 tables in Lake database in Azure Synapse - Account, our_sales and their_sales.

## Building Datalake Standardised/Silver Layer
- Create standardised database: Create a new database using the notebook named standardised
- Create standardised account table: Use the notebook to create standardised account table which will do some data clean up on the raw account table and load it to the new table.
- Create standardised our_sales table: Use the notebook to create standardised our_sales table which will do some data clean up (date column) on the raw our_sales table and load it to the new table.
- Create standardised their_sales table: Use the notebook to create standardised their_sales table which will do some data clean up (date column) on the raw their_sales table and load it to the new table.

## Building Datalake Curated/Gold Layer
- Create curated database: Create a new database using the notebook named curated
- Create curated account table: Use the notebook to create curated account table which will select some specific columns from the standardised account table and load it to the new table.
- Create curated sales table: Use the notebook to create curated sales table which will merge the sales data from both sales tables and load it to the new table.

## Building Visualisation
- Create Power BI report: Create a Power BI report using the template demo.pbix which consumes the two tables - account and sales. Publish this report to Power BI service.
- Publish report to Dynamics Sales: Publish the report to Dynamics Sales
