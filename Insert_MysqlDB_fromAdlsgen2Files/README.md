# Dataflow into Azure Database for MySQL
A dataflow to insert the data into [Azure Database for MySQL](https://docs.microsoft.com/en-us/azure/mysql/) from files stored in [Azure Data Lake Storagegen2](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction).
<hr/>


Processors & Templates that are being used in the pipeline:
- [FetchFromADLS](https://github.com/abhijeetsatpute/azure-nifi-dataflows/tree/main/FetchFromADLS) - Fetch files from ADLS.
- [SplitText](http://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.12.1/org.apache.nifi.processors.standard.SplitText/index.html) - Splits a text file into multiple smaller text files on line boundaries limited by maximum number of lines or total size of fragment.
- [ConvertRecord](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.5.0/org.apache.nifi.processors.standard.ConvertRecord/index.html) - Used to convert CSV (Record Reader) to JSON (Record Write).
- [ConvertJSONToSQL](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.6.0/org.apache.nifi.processors.standard.ConvertJSONToSQL/) - Converts a JSON-formatted FlowFile into an UPDATE, INSERT, or DELETE SQL statement.
- [PutSQL](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.6.0/org.apache.nifi.processors.standard.PutSQL/index.html) - Executes a SQL UPDATE or INSERT command.

# <b>Resources</b>
- [Steven Koon](https://www.youtube.com/watch?v=8KxcAiNdqvw&t=145s&ab_channel=StevenKoon)
- [MySQL Workbench](https://docs.microsoft.com/en-us/azure/mysql/connect-workbench)
- [MySQL JDBC Driver - Time Zone Issue](https://stackoverflow.com/questions/26515700/mysql-jdbc-driver-5-1-33-time-zone-issue)
- [JDBC Driver](https://dev.mysql.com/downloads/connector/j/)

> **Configure** *DBCPConnectionPool* Controller Service with valid JDBC connection string, DB user-pwd, Driver Class name & Driver Location.
