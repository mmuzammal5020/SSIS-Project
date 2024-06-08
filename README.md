It is a simple SSIS Project Where new data is coming on daily bases so, We have to automate the process a cycle with following processes as per the client's requirements:-
  1. Load data from source file into MS SQL database
  2. Rename the new files as per company's naming convention
  3. After the end of data lifecycle, move the file into Archive folder
  4. Save the file as zip file in Archive
  5. Now after ziping the file, delete the original copy

Here is the MS SQL Code to create a table to load data from source file into destination table in MS SQL database
``` sql
CREATE TABLE [ssis_project].[dbo].[FF_CD_Data] 
	(
	id INT,
	F_name NVARCHAR(50),
    M_Name NVARCHAR(50),
    L_name NVARCHAR(50),
	dob DATE
	);
```

Query to view data in MS SQL
``` sql
SELECT TOP (1000) [id]
      ,[F_name]
      ,[M_Name]
      ,[L_name]
      ,[dob]
  FROM [ssis_project].[dbo].[FF_CD_Data]
```
