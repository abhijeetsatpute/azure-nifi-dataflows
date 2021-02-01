# Dataflow into ADLS
A dataflow to ingest input file data to [Azure Data Lake Storagegen2](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction).
<hr/>

Processors that are being used in the pipeline:
- [GetFile](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.5.0/org.apache.nifi.processors.standard.GetFile/index.html) - Fetches csv files as a source.
- [PutAzureDataLakeStorage](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-azure-nar/1.12.1/org.apache.nifi.processors.azure.storage.PutAzureDataLakeStorage/index.html) - Puts content into an Azure Data Lake Storage Gen 2

# <b>Resources</b>

- [Ingesting data into Azure Data Lake Storage](https://docs.cloudera.com/cdf-datahub/7.2.0/nifi-azure-ingest/topics/cdf-datahub-fm-adls-ingest-overview.html)

> **Configure** *ADLSCredentialsControllerService* Controller Service with Storage Account name and valid access keys.
