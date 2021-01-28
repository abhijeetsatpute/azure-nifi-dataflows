# CsvToParquet
Converts local csv files to [parquet](https://hackolade.com/help/Parquetschema.html) file format.
<hr/>

Processors that are being used in the pipeline:
- [GetCsvFile](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.5.0/org.apache.nifi.processors.standard.GetFile/index.html) - Fetches csv files as a source.
- [ConvertRecord](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.5.0/org.apache.nifi.processors.standard.ConvertRecord/index.html) - Writes CSVReader 1.12.1 FlowFile data to ParquetRecordSetWriter 1.12.1
- [PutParquetFile](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.6.0/org.apache.nifi.processors.standard.PutFile/) - Writes the contents of a parquet FlowFile to the local file system.


# <b>Resources</b>

- [Avro schema validator](https://json-schema-validator.herokuapp.com/avro.jsp)
- [Parquet Viewer](http://parquet-viewer-online.com/)
- [Expression Language replace()](https://nifi.apache.org/docs/nifi-docs/html/expression-language-guide.html#replace)
- [Regex](https://regex101.com/)

> **Validate** avro schema : *DemoSchema* Controller Service properety *courses* a/c to the input file.
