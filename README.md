# Complete_Azure_DE_Pizza_Project

![Slide1](https://github.com/Abdur-RasheedAde/Complete_Azure_DE_Pizza_Project/blob/main/AzureDEPizzaProject.png)

##  Introduction
This is a complete Azure Data Engineering End-to-end project exploring SQL Server, Azure Blob Storage, Azure Data Factory, Databricks and Power BI. The project ingest a csv file into the onprem SQL Database, created a Data pipeline in Azure Data Factory to Extract the data and reload into Azure Blob Storage so as to create an Analystical Report in Databricks and Visualization in Power BI. 

## Data Source:
The data used is a Cricket World Cup match in 2023 which comes in a json file injested directly from a folder;  
* Cricket World Cup Match in 2023 [Downloadjsonfilehere](https://drive.google.com/drive/folders/1ls9ST-q6c2fCZZOuaC8Bd5lugrTKbVIE?usp=drive_link)

## DE Technical Skills:
+ Schema Creation
+ Data Ingestion
+ Data Warehousing
+ Extract, Transform and Load (ETL) process
+ Flattering of JSON file into a Table
+ Data Modelling (Fact and Dimention table)
+ Data Visualization - dashboard
+ Feedback and Continuous Improvement
  
## Data Engineering Process
1. Creation of database and 4 Schemas: A database (DB) known as CRICKET is created with 4 Schemas (LAND, RAW, CLEAN and CONSUMPTION) for proper logical description and arrangement of the DB. The Star-schema was eventually used in Data Modelling so as to give the datawarehouse a legible understading. [Get the code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/1.%20Schema_CREATION_and_Data_Injestion) 
2. Data Ingestion and Loading: Data is injested into the LAND schema and reloaded into the RAW schema. [Get the code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/2.%20Data_Loading_into_RAW_Schema) 
3. Flattening of Data: Since the data uploaded are ojects, they need to be flatenned so as to create the CLEAN proper column based table. [Get the code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/3.%20Flatten_json_into_CLEAN_table) 
4. Creation of Player and Country table: This is achieved by flattening the json objects in the RAW schema to create a Player and Country column Table (get code here). These 2 tables are connected with the help of a primary and foreign key respectively. [Get the code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/4.%20Player_and_Country_Table) 
5. Extract Data from Inning Array: This is another strategy of the ETL process to transform an array into a proper column based table. This is used to get the Delivery clean Table. [Get the code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/5.%20Delivery_Table)
6. Data Validation: There is an absolute need to check the degree of correctness of a data after the whole ETL process. [Get the code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/6.%20Data_Validation)
7. Creation of Dimension Tables: 5 Dimention tables are created including referee_dim, team_dim, player_dim, venue_dim and match_type_dim tables while poluating data into them and establishing different relationship between them as well. [get code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/7.%20Dimension_Tables_
8. Creation of Date Dimension Table: A date dimention table is also created so as to link it to the match_fact_table. [Get the code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/8.%20Date_Dimension_Tables)
9. Creation of Fact_Tables: 2 Fact tables are created Match_type and Delivery tables and are both populated with data. [Get the code here](https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/9.%20Fact_Tables) 

## Data Visualization
After all ETL process and data warehousing, some important metrics are visualized using the snowflake dashboard. This is a simple created dashboard with just 5 KPIs and can be accessed using the link below. However, this project was created using the free trial of snowflake and may not be accessible after 30 days of uplaod.

The dashbord image is here 👇
<img src="https://github.com/Abdur-RasheedAde/Snowflake_Projects/blob/main/Simple_Snowflake%20Dashboard.PNG" width=75% height=75%>  
Link to the dashboard is here 👉 [Click to view dashboard](https://app.snowflake.com/xelrqqi/zeb17834/#/cricket_match_dashboard-dK2zKZJf9)

## Conclusions 
1. Snowflake is one of the leading cloud big data Softaware as a service (SaaS) for Data supporting both Python and SQL.
2. It is awesome for Data warehousing and ETL process and simple visualization dashboard.

Thanks for taking time to go through this report! and I am open to collaborate with you on any Data Engineering projects exploring snowflake or other cloud big data platforms especially Azure, AWS, GCP and Databricks, you can always reach me on adeoyerasheed30@gmail.com Ciao 🤝
