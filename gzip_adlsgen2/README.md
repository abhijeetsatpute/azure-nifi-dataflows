# Dataflow into ADLS
A dataflow to ingest compressed input files ([gzip](https://en.wikipedia.org/wiki/Gzip)) to [Azure Data Lake Storagegen2](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction).
<hr/>

Processors that are being used in the pipeline:
- [GetFile](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.5.0/org.apache.nifi.processors.standard.GetFile/index.html) - Creates FlowFiles from files in a directory.
- [CompressContent](https://nifi.apache.org/docs/nifi-docs/components/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.9.0/org.apache.nifi.processors.standard.CompressContent/index.html) - Compresses or decompresses the contents of FlowFiles using a user-specified compression algorithm and updates the mime.type attribute as appropriate
- [PutAzureDataLakeStorage](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-azure-nar/1.12.1/org.apache.nifi.processors.azure.storage.PutAzureDataLakeStorage/index.html) - Puts content into an Azure Data Lake Storage Gen 2

# <b>Resources</b>

- [Ingesting data into Azure Data Lake Storage](https://docs.cloudera.com/cdf-datahub/7.2.0/nifi-azure-ingest/topics/cdf-datahub-fm-adls-ingest-overview.html)

> **Configure** *ADLSCredentialsControllerService* Controller Service with Storage Account name and valid access keys.
