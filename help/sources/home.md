---
keywords: Experience Platform;home;popular topics
solution: Experience Platform
title: Adobe Experience Platform Source Connectors overview
topic: overview
---

# Source connectors overview

Adobe Experience Platform allows data to be ingested from external sources while providing you with the ability to structure, label, and enhance incoming data using [!DNL Platform] services. You can ingest data from a variety of sources such as Adobe applications, cloud-based storage, databases, and many others.

[!DNL Experience Platform] provides a RESTful API and an interactive UI that lets you set-up source connections to various data providers with ease. These source connections enable you to authenticate your third-party systems, set times for ingestion runs, and manage data ingestion throughput.

With [!DNL Experience Platform], you can centralize data you collect from disparate sources and use the insights gained from it to do more.

## Types of sources

Sources in [!DNL Experience Platform] are grouped into the following categories:

### Adobe applications

[!DNL Experience Platform] allows data to be ingested from other Adobe applications, including Adobe Analytics, Adobe Audience Manager, and [!DNL Experience Platform Launch]. See the following related documents for more information:

- [Adobe Audience Manager connector overview](connectors/adobe-applications/audience-manager.md)
- [Create an Adobe Audience Manager source connector in the UI](./tutorials/ui/create/adobe-applications/audience-manager.md)
- [Adobe Analytics data connector overview](connectors/adobe-applications/analytics.md)
- [Create an Adobe Analytics source connector in the UI](./tutorials/ui/create/adobe-applications/analytics.md)
- [Create a Customer Attributes source connector in the UI](./tutorials/ui/create/adobe-applications/customer-attributes.md)

### Advertising

[!DNL Experience Platform] provides support for ingesting data from a third-party advertising system. See the following related documents for more information on specific source connectors:

- [!DNL Google AdWords](connectors/advertising/ads.md) connector

### Cloud Storage

Cloud storage sources can bring your own data into [!DNL Platform] without the need to download, format, or upload. Ingested data can be formatted as XDM JSON, XDM parquet, or delimited. Every step of the process is integrated into the Sources workflow using the user interface. See the following related documents for more information:

- [!DNL Azure Data Lake Storage Gen2](connectors/cloud-storage/adls-gen2.md) connector
- [!DNL Azure Blob and Amazon S3](connectors/cloud-storage/blob-s3.md) connector
- [!DNL Amazon Kinesis](connectors/cloud-storage/kinesis.md) connector
- [!DNL Apache HDFS](connectors/cloud-storage/hdfs.md) connector
- [!DNL Azure Event Hubs](connectors/cloud-storage/eventhub.md) connector
- [!DNL Azure File Storage](connectors/cloud-storage/azure-file-storage.md) connector
- [!DNL FTP and SFTP](connectors/cloud-storage/ftp-sftp.md) connector
- [!DNL Google Cloud Storage](connectors/cloud-storage/google-cloud-storage.md) connector

### Customer Relationship Management (CRM)

CRM systems provide data that can help build customer relationships, which in turn, create loyalty and drive customer retention. [!DNL Experience Platform] provides support for ingesting CRM data from [!DNL Microsoft Dynamics 365] and [!DNL Salesforce]. See the following related documents for more information:

- [!DNL Microsoft Dynamics](connectors/crm/ms-dynamics.md) connector
- [!DNL Salesforce](connectors/crm/salesforce.md) connector

### Customer Success

[!DNL Experience Platform] provides support for ingesting data from a third-party customer success application. See the following related documents for more information:

- [!DNL Salesforce Service Cloud](connectors/customer-success/salesforce-service-cloud.md) connector
- [!DNL ServiceNow](connectors/customer-success/servicenow.md) connector

### Database

[!DNL Experience Platform] provides support for ingesting data from a third-party database. See the following related documents for more information on specific source connectors:

- [!DNL Amazon Redshift](connectors/databases/redshift.md) connector
- [!DNL Apache Hive on Azure HDInsights](connectors/databases/hive.md) connector
- [!DNL Apache Spark on Azure HDInsights](connectors/databases/spark.md) connector
- [!DNL Azure Data Explorer](connectors/databases/data-explorer.md) connector
- [!DNL Azure Synapse Analytics](connectors/databases/synapse-analytics.md) connector
- [!DNL Azure Table Storage](connectors/databases/ats.md) connector
- [!DNL Couchbase](connectors/databases/couchbase.md) connector
- [!DNL Google BigQuery](connectors/databases/bigquery.md) connector
- [!DNL GreenPlum](connectors/databases/greenplum.md) connector
- [!DNL HP Vertica](connectors/databases/hp-vertica.md) connector
- [!DNL IBM DB2](connectors/databases/ibm-db2.md) connector
- [!DNL MariaDB](connectors/databases/mariadb.md) connector
- [!DNL Microsoft SQL Server](connectors/databases/sql-server.md) connector
- [!DNL MySQL](connectors/databases/mysql.md) connector
- [!DNL Oracle](connectors/databases/oracle.md) connector
- [!DNL Phoenix](connectors/databases/phoenix.md) connector
- [!DNL PostgreSQL](connectors/databases/postgres.md) connector

### Marketing Automation

[!DNL Experience Platform] provides support for ingesting data from a third-party marketing automation system. See the following related documents for more information on specific source connectors:

- [!DNL HubSpot](connectors/marketing-automation/hubspot.md) connector

### Payments

[!DNL Experience Platform] provides support for ingesting data from a third-party payments system. See the following related documents for more information on specific source connectors:

- [!DNL PayPal](connectors/payments/paypal.md) connector

### Protocols

[!DNL Experience Platform] provides support for ingesting data from a third-party protocols system. See the following related documents for more information on specific source connectors:

- [!DNL Generic OData](connectors/protocols/odata.md) connector

## Access control for sources in data ingestion

Permissions for sources in data ingestion can be managed within the Adobe Admin Console. You can access permissions through the *[!UICONTROL Permissions]* tab in a particular product profile. From the **[!UICONTROL Edit Permissions]** panel, you can access the permissions pertaining to sources through the *[!UICONTROL data ingestion]* menu entry. The **[!UICONTROL View Sources]** permission grants read-only access to available sources in the *[!UICONTROL Catalog]* tab and authenticated sources in the *[!UICONTROL Browse]* tab, while the **[!UICONTROL Manage Sources]** permission grants full access to read, create, edit, and disable sources.

The following table outlines how the UI behaves based on different combinations of these permissions:

| Permission level | Description |
| ---- | ----|
| **[!UICONTROL View Sources]** On | Grant read-only access to sources in each source-type in the *Catalog* tab, as well as the *Browse*, *Accounts*, and *DataFlow* tabs. |
| **[!UICONTROL Manage Sources]** On | In addition to the functions included in **[!UICONTROL View Sources]**, grants access to *[!UICONTROL Connect Source]* option in *[!UICONTROL Catalog]* and to *[!UICONTROL Select Data]* option in *[!UICONTROL Browse]*. **[!UICONTROL Manage Sources]** also allows you to enable or disable *[!UICONTROL DataFlows]* and edit their schedules. |
| **[!UICONTROL View Sources]** Off and **[!UICONTROL Manage Sources]** Off | Revoke all access to sources. |

For more information about the available permissions granted through the Admin Console, including those four sources, see the [access control overview](../access-control/home.md).

## Terms and conditions {#terms-and-conditions}

By using any of the Sources labeled as beta (“Beta”), You hereby acknowledge that the Beta is provided ***“as is” without warranty of any kind***.

Adobe shall have no obligation to maintain, correct, update, change, modify, or otherwise support the Beta. You are advised to use caution and not to rely in any way on the correct functioning or performance of such Beta and/or accompanying materials. The Beta is considered Confidential Information of Adobe.

Any “Feedback” (information regarding the Beta including but not limited to problems or defects you encounter while using the Beta, suggestions, improvements, and recommendations) provided by You to Adobe is hereby assigned to Adobe including all rights, title, and interest in and to such Feedback.

Submit Open Feedback or create a Support Ticket to share your suggestions or report a bug, seek a feature enhancement.
