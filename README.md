The stored procedure used as an ELT is unique and recursively calls itself depending on the number of levels (times) required for the database to batch process. The dynamic queries are executed through a cursor.

Some imported files contain anomalies and bulk cannot process. An error log file will be generated and a manual fix will be required.

Note: The integrated boxing system will rebuild and clean itself and common anomalies are detected and taken care of on the master level.
