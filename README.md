The stored procedure used as an ELT is unique and recursively calls itself depending on the number of levels (times) required for the database to batch process. The dynamic queries are executed through a cursor. The integrated boxing system will rebuild and clean itself and common anomalies are detected and taken care of on the master level.

The first execution of the importation will take a long time as it will analyze every records in order to determine the data type of the columns.
The next imports will take very fewer time as no analysis will be done since the files were already analyzed.
If adding outliers after the first importation, on the other hand, may and will result in a bulk fail on the server side.
This process could and should be handled through a programming language that can process files asynchronously, such as python or c#.

Some imported files contain anomalies and bulk cannot process. An error log file will be generated and a manual fix will be required.

As ELT generation should not be on the server side to be made, C# ELT integration has already begun and planned for the future.
