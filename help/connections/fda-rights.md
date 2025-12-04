---
title: Machtigingen voor toegang tot een externe database
description: Leer over welke toestemmingen u tot taken op elke gegevensbestandmotor moet toegang hebben en uitvoeren
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: e0bf1f76f7f781fb6fcc3b44898ba805d87a25c9
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 4%

---

# FDA-matrix (Federated Data Access) {#fda-rights}

De volgende lijst schetst de vereiste gegevensbestandtoestemmingen voor elk systeem, latend u verrichtingen op externe gegevensbestanden door gefederaliseerde gegevenstoegang (FDA) uitvoeren.

|   | Snowflake | Opnieuw | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Verbindend met ver gegevensbestand** | `USAGE ON WAREHOUSE` -, `USAGE ON DATABASE` - en `USAGE ON SCHEMA` -rechten | Een gebruiker maken die is gekoppeld aan de AWS-account | Creeer een de dienstrekening en verlenen belangrijkste toegang tot project | `USE CATALOG` machtiging voor Catalog en `CAN_USE` machtiging voor SQL Warehouse |
| **Creërend lijsten** | `CREATE TABLE ON SCHEMA` privilege | `CREATE` machtiging | Rol die aan serviceaccount is toegewezen, moet de volgende machtigingen bevatten: `bigquery.jobs.create` en `bigquery.tables.create` | `USE SCHEMA` - en `CREATE TABLE` -machtigingen |
| **Creërend indexen** | N.v.t. | `CREATE` machtiging | BigQuery ondersteunt alleen zoekindexen. De rol die aan het serviceaccount is toegewezen, moet de volgende machtigingen bevatten: `bigquery.jobs.create` , `bigquery.tables.getData` en `bigquery.tables.createIndex` | N.v.t. |
| **Creërend functies** | `CREATE FUNCTION ON SCHEMA` privilege | `USAGE ON LANGUAGE plpythonu` toestemming om externe Python-scripts aan te roepen | De rol die aan serviceaccount is toegewezen, moet de volgende machtigingen bevatten: `bigquery.jobs.create` en `bigquery.routines.create` | `CREATE FUNCTION` machtiging |
| **Creërend procedures** | N.v.t. | `USAGE ON LANGUAGE plpythonu` toestemming om externe Python-scripts aan te roepen | De rol die aan het serviceaccount is toegewezen, moet de volgende machtigingen bevatten: `bigquery.jobs.create` en `bigquery.routines.create` |  NVT |
| **het Verwijderen van voorwerpen (lijsten, indexen, functies, procedures)** | Het object in eigendom hebben | Het object in eigendom of supergebruiker zijn | De rol die aan het serviceaccount is toegewezen, moet de volgende machtigingen bevatten: `bigquery.jobs.create` , `bigquery.routines.delete` , `bigquery.tables.delete` en `bigquery.tables.deleteIndex` | N.v.t. |
| **de uitvoeringen van de Controle** | `MONITOR` -bevoegdheid voor het vereiste object | Er zijn geen machtigingen vereist om de opdracht `EXPLAIN` te gebruiken | `monitoring.viewer` rol | `CAN_VIEW` machtiging |
| **het Schrijven gegevens** | `INSERT` en/of `UPDATE` bevoegdheden (afhankelijk van de schrijfbewerking) | `INSERT` - en `UPDATE` -machtigingen | De rol die aan het serviceaccount is toegewezen, moet het volgende bevatten: `bigquery.jobs.create` en `bigquery.tables.updateData` | `MODIFY` machtiging |
| **Ladende gegevens in lijsten** | `CREATE STAGE ON SCHEMA` , `SELECT` en `INSERT` in de rechten voor de doeltabel | `SELECT` - en `INSERT` -machtigingen | De rol die aan het serviceaccount is toegewezen, moet het volgende bevatten: `bigquery.jobs.create` , `bigquery.tables.getData` en `bigquery.tables.updateData` | `SELECT` - en `MODIFY` -machtigingen |
| **Toegang tot cliëntgegevens** | `SELECT on (FUTURE) TABLE(S)` of `VIEW(S)` privilege(s) | `SELECT` machtiging | De rol die aan het serviceaccount is toegewezen, moet het volgende bevatten: `bigquery.jobs.create` en `bigquery.tables.getData` for tables of de `bigquery.dataViewer` rol | `SELECT` machtiging |
| **Toegang tot meta-gegevens** | `SELECT on INFORMATION_SCHEMA SCHEMA` privilege | `SELECT` machtiging | `bigquery.metadataViewer` rol |  `SELECT on INFORMATION_SCHEMA SCHEMA` machtiging |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Verbindend met ver gegevensbestand** | Leesmachtiging (standaard) | `CONNECT` machtiging | Geen bevoegdheid vereist |
| **Creërend lijsten** | `CREATE TABLE ON DATABASE` (magazijn) en `ALTER ON SCHEMA` | `CREATE TABLE` machtiging | `CREATE ON SCHEMA` privilege |
| **Creërend indexen** | N.v.t. | `ALTER` machtiging | N.v.t. |
| **Creërend functies** | N.v.t. | `CREATE FUNCTION` machtiging | `CREATE ON SCHEMA` privilege |
| **Creërend procedures** | `CREATE PROCEDURE ON DATABASE` (magazijn) en `ALTER ON SCHEMA` | `CREATE PROCEDURE` machtiging | `CREATE ON SCHEMA` privilege |
| **het Verwijderen van voorwerpen (lijsten, indexen, functies, procedures)** | `ALTER ON SCHEMA` | `ALTER` machtiging | Het object of de `DROP` -bevoegdheid in eigendom hebben van het object |
| **de uitvoeringen van de Controle** | Workspace Contributor of hoger (`queryinsights.exec_requests_history`) | `CONTROL` machtiging | Geen bevoegdheid vereist voor het gebruik van de instructie `EXPLAIN` |
| **het Schrijven gegevens** | `INSERT` en/of `UPDATE ON OBJECT` | `INSERT` - en `UPDATE` -machtigingen | `INSERT` en `UPDATE` privileges |
| **Ladende gegevens in lijsten** | `SELECT ON OBJECT` en `INSERT ON OBJECT` | `CREATE TABLE` -, `EXECUTE` -, `SELECT` -, `INSERT` -, `UPDATE` - en `ALTER` -machtigingen | `INSERT` -bevoegdheid op tafel, `USAGE` -bevoegdheid op schema |
| **Toegang tot cliëntgegevens** | `SELECT ON OBJECT` | `SELECT` machtiging | `SELECT` privilege |
| **Toegang tot meta-gegevens** | `SELECT ON INFORMATION_SCHEMA` | Geen toestemming vereist om tabel te beschrijven | `USAGE ON SCHEMA` , `SELECT on TABLE` en ook rechten voor tabellen `v_catalog.columns` en `v_catalog.view_columns` |
