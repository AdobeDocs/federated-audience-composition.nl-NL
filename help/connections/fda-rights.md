---
title: Machtigingen voor toegang tot een externe database
description: Meer informatie over specifieke rechten voor elke database-engine
source-git-commit: 8cd1b967e004d84fda3788e442e41d2010f5ec24
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 2%

---

# FDA Rights Matrix {#fda-rights}

In de onderstaande tabel worden de vereiste databaserechten voor elk systeem beschreven, zodat gebruikers bewerkingen op externe databases kunnen uitvoeren via FDA.

|   | Snowflake | Opnieuw | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Verbindend met ver gegevensbestand** | GEBRUIK OP WAREHOUSE, GEBRUIK OP DATABASE EN GEBRUIK OP SCHEMA-privileges | Een gebruiker maken die is gekoppeld aan de AWS-account | Creeer een de dienstrekening en verlenen belangrijkste toegang tot project | GEBRUIK CATALOG-bevoegdheden voor Catalog en CAN_USE-bevoegdheden voor SQL Warehouse |
| **Creërend lijsten** | TABEL MAKEN OP SCHEMA-voorrecht | BEVOEGDHEID MAKEN | De rol die aan de dienstrekening wordt toegewezen moet bevatten: bigquery.jobs.create en bigquery.tables.create toestemmingen | HET BEVOEGDHEID VAN HET SCHEMA VAN HET GEBRUIK EN CREËREN DE BEVOEGDHEID VAN DE TABEL |
| **Creërend indexen** | N.v.t. | BEVOEGDHEID MAKEN | BigQuery ondersteunt alleen zoekindexen. De rol die aan de dienstrekening wordt toegewezen moet bevatten: bigquery.jobs.create, bigquery.tables.getData en bigquery.tables.createIndex toestemmingen | N.v.t. |
| **Creërend functies** | FUNCTIE MAKEN VOOR SCHEMA-BEVOEGDHEID | GEBRUIK OP TAALvoorrecht om externe pythonuscripts aan te roepen | De rol die aan de dienstrekening wordt toegewezen moet bevatten: bigquery.jobs.create en bigquery.routines.create toestemmingen | FUNCTIE-bevoegdheden MAKEN |
| **Creërend procedures** | N.v.t. | GEBRUIK OP TAALvoorrecht om externe pythonuscripts aan te roepen | De rol die aan de dienstrekening wordt toegewezen moet bevatten: bigquery.jobs.create en bigquery.routines.create toestemmingen |  NVT |
| **het Verwijderen van voorwerpen (lijsten, indexen, functies, procedures)** | Het object in eigendom hebben | Het object in eigendom of supergebruiker zijn | De rol die aan de dienstrekening wordt toegewezen moet bevatten: bigquery.jobs.create, bigquery.routines.delete, bigquery.tables.delete en bigquery.tables.deleteIndex toestemmingen |
| **de uitvoeringen van de Controle** | BEVOEGDHEID MONITOR voor het vereiste object | Geen bevoegdheid vereist om de opdracht EXPLAIN te gebruiken | monitoring.viewer, rol | CAN_VIEW-machtiging |
| **het Schrijven gegevens** | INSERT- en/of UPDATE-bevoegdheden (afhankelijk van schrijfbewerking) | Rechten INVOEGEN en BIJWERKEN | De rol die aan de dienstrekening wordt toegewezen moet bevatten: bigquery.jobs.create en bigquery.tables.updateData |  BEVOEGDHEID WIJZIGEN |
| **Ladende gegevens in lijsten** | WERKGEBIED MAKEN OP SCHEMA, SELECTEREN en INVOEGEN in de rechten voor de doeltabel | SELECTEREN EN INVOEGEN, rechten | De rol die aan de dienstrekening wordt toegewezen moet bevatten: bigquery.jobs.create, bigquery.tables.getData en bigquery.tables.updateData | privileges SELECTEREN en WIJZIGEN |
| **Toegang tot cliëntgegevens** | SELECTEREN OP (TOEKOMSTIGE) TABLE(S)- OF WEERGAVEBEVOEGDHEDEN | SELECT, bevoegdheid | De rol die aan de dienstrekening wordt toegewezen moet bevatten: bigquery.jobs.create en bigquery.tables.getData voor lijsten of bigquery.dataViewer rol |  SELECT, bevoegdheid |
| **Toegang tot meta-gegevens** | SELECTEER INFORMATIE_SCHEMA-SCHEMA-voorrecht | SELECT, bevoegdheid | bigquery.metadataViewer, rol |  SELECTEER INFORMATIE_SCHEMA-SCHEMA-voorrecht |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Verbindend met ver gegevensbestand** | Leesmachtiging (standaard) | CONNECT-machtiging | Geen bevoegdheid vereist |
| **Creërend lijsten** | CREEER LIJST OP DATABASE (pakhuis) EN VERANDERT OP SCHEMA | TABEL MAKEN, machtiging | CREËREN OP SCHEMA-voorrecht |
| **Creërend indexen** | N.v.t. | ALTER-machtiging | N.v.t. |
| **Creërend functies** | N.v.t. | FUNCTIE MAKEN, machtiging | CREËREN OP SCHEMA-voorrecht |
| **Creërend procedures** | PROCEDURE INSTELLEN VOOR DATABASE (magazijn) EN VERANDEREN OP SCHEMA | TOESTEMMING VOOR PROCEDURE MAKEN | CREËREN OP SCHEMA-voorrecht |
| **het Verwijderen van voorwerpen (lijsten, indexen, functies, procedures)** | ALTER OP SCHEMA | ALTER-machtiging | het bezit van het voorwerp of DROP voorrecht op voorwerp |
| **de uitvoeringen van de Controle** | Workspace Contributor of hoger machtigingen (queryinghts.exec_Requests_history)  | CONTROLE-machtiging | Geen bevoegdheid vereist om instructie EXPLAIN te gebruiken |
| **het Schrijven gegevens** | INVOEGEN en/of BIJWERKEN OP OBJECT | Machtigingen INVOEGEN en BIJWERKEN | Rechten INVOEGEN en BIJWERKEN |
| **Ladende gegevens in lijsten** | SELECTEREN OP OBJECT en INVOEGEN OP OBJECT | TABLE MAKEN, UITVOEREN, SELECTEREN, INVOEGEN, BIJWERKEN, WIJZIGEN | INSERT-bevoegdheid op tafel, USAGE-bevoegdheid op schema |
| **Toegang tot cliëntgegevens** | SELECTEREN OP OBJECT | machtiging SELECTEREN | SELECT, bevoegdheid |
| **Toegang tot meta-gegevens** | SELECTEREN OP INFORMATIE_SCHEMA | Geen toestemming vereist om tabel te beschrijven | GEBRUIKEN OP SCHEMA, SELECTEREN OP TABLE en ook privileges op tables v_catalog.columns en v_catalog.view_columns |
