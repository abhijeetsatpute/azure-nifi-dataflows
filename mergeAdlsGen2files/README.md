# Dataflow into ADLS
A dataflow to merge all the files in ADLSgen2 storage into one file and ingest back to [Azure Data Lake Storagegen2](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction).
<hr/>


Processors that are being used in the pipeline:
- [ListAzureDataLakeStorage ](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-azure-nar/1.12.1/org.apache.nifi.processors.azure.storage.ListAzureDataLakeStorage/index.html) - Lists directory in an Azure Data Lake Storage Gen 2 filesystem.
- [MergeContent](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-standard-nar/1.6.0/org.apache.nifi.processors.standard.MergeContent/index.html) - Merges a Group of FlowFiles together based on a user-defined strategy and packages them into a single FlowFile.
- [UpdateAttribute](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-update-attribute-nar/1.12.1/org.apache.nifi.processors.attributes.UpdateAttribute/additionalDetails.html) - For updating filename of merged file.
- [PutAzureDataLakeStorage](https://nifi.apache.org/docs/nifi-docs/components/org.apache.nifi/nifi-azure-nar/1.12.1/org.apache.nifi.processors.azure.storage.PutAzureDataLakeStorage/index.html) - Puts content into an Azure Data Lake Storage Gen 2

# <b>Templates used</b>

- [ingest_to_adlsgen2](https://github.com/abhijeetsatpute/azure-nifi-dataflows/blob/main/ingest_to_adlsgen2/ingest_into_adls.xml)

> **Configure** *ADLSCredentialsControllerService* Controller Service with Storage Account name and valid access keys.
