# Dataflow from ADLS
A dataflow to retrieve files from [Azure Data Lake Storagegen2](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction).
<hr/>

Processors that are being used in the pipeline:
- [ListAzureDataLakeStorage](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-azure-nar/1.12.1/org.apache.nifi.processors.azure.storage.ListAzureDataLakeStorage/index.html) - Lists directory in an Azure Data Lake Storage Gen 2 filesystem.
- [FetchAzureDataLakeStorage](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-azure-nar/1.12.1/org.apache.nifi.processors.azure.storage.FetchAzureDataLakeStorage/index.html) - Fetch the provided file from Azure Data Lake Storage.
