---
audience: end-user
title: Aan de slag met Federale Databases
description: Leer hoe te om uw Federale Gegevensbestanden tot stand te brengen en te beheren
source-git-commit: 847da9a5eeb28199010f8491f7eebba4a60a83f1
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 2%

---

# Aan de slag met Federale Databases {#federated-db}


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="Federale databases"
>abstract="De bestaande verbindingen aan Federale Gegevensbestanden zijn vermeld in dit scherm. Om een nieuwe verbinding tot stand te brengen, klik **voegt gefedereerde gegevensbestand** knoop toe."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="Federale database-eigenschappen"
>abstract="Ga de naam van het nieuwe Federatieve Gegevensbestand in, en selecteer zijn type."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="Gegevens van gefederaliseerde database"
>abstract="Ga de montages in om met het nieuwe Federatieve Gegevensbestand te verbinden. Gebruik de **knoop van de Verbinding van de Test** om uw configuratie te bevestigen."

Maak, configureer, test en sla de verbinding met een externe database op.

Ondersteunde externe databases:

* Snowflake
* Google Big Query
* Azure synapse
* Vertica Analytics
* Amazon Redshift

## Snowflake {#snowflake}

* **[!UICONTROL Server]**:

* **[!UICONTROL User]**: naam van de gebruiker.

* **[!UICONTROL Password]**: wachtwoord gebruikersaccount.

* **[!UICONTROL Database]**:

* **[!UICONTROL Working schema]**:

* **[!UICONTROL Private key]** :
Alleen .pem-bestanden worden geaccepteerd

* **[!UICONTROL Options]**: De connector ondersteunt de opties die in de onderstaande tabel worden beschreven.

| Optie | Beschrijving |
|---|---|
| werkschema | Databaseschema dat moet worden gebruikt voor werktabellen |
| entrepot | Naam van het standaardentrepot aan gebruik. De standaardinstelling van de gebruiker wordt hierdoor genegeerd. |
| TimeZoneName | Standaard leeg, wat betekent dat de systeemtijdzone van de Campaign Classic-app-server wordt gebruikt. De optie kan worden gebruikt om de TIMEZONE-sessieparameter te forceren. <br> voor meer op dit, verwijs naar [ deze pagina ](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone). |
| WeekStart | WEEK_START, sessieparameter. Standaard ingesteld op 0. <br> voor meer op dit, verwijs naar [ deze pagina ](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start). |
| UseCachedResult | USE_CACHED_RESULTS sessieparameter. Standaard ingesteld op TRUE. Deze optie kan worden gebruikt om Snowflake caching resultaten onbruikbaar te maken. <br> voor meer op dit, verwijs naar [ deze pagina ](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html). |
| bulkThreads | Het aantal draden dat moet worden gebruikt voor bulksgewijs laden van Snowflaken, meer threads betekenen betere prestaties voor grotere bulkladingen. Standaard ingesteld op 1. Het aantal kan, afhankelijk van het aantal van de machindraad worden aangepast. |
| chunkSize | Hiermee bepaalt u de bestandsgrootte van het segment voor bulksloader. Standaard ingesteld op 128 MB. Kan worden aangepast voor een betere prestatie, wanneer gebruikt met bulkThreads. Meer tegelijkertijd actieve threads betekenen betere prestaties. <br> voor meer op dit, verwijs naar [ documentatie van de Snowflake ](https://docs.snowflake.net/manuals/sql-reference/sql/put.html). |
| StageName | Naam van het vooraf ingestelde interne werkgebied. Het wordt gebruikt in bulk lading in plaats van het creëren van een nieuwe tijdelijke fase. |

## Google Big Query {#google-big-query}

* **[!UICONTROL Service account]**: E-mail van uw **[!UICONTROL Service account]** . Voor meer informatie over dit, verwijs naar [ de documentatie van de Wolk van Google ](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

* **[!UICONTROL Project]**: naam van de **[!UICONTROL Project]** . Voor meer informatie over dit, verwijs naar [ de documentatie van de Wolk van Google ](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

* **[!UICONTROL Dataset]**: naam van de **[!UICONTROL Dataset]** . Voor meer informatie over dit, verwijs naar [ de documentatie van de Wolk van Google ](https://cloud.google.com/bigquery/docs/datasets-intro).

* **[!UICONTROL Key file Path]**: upload het sleutelbestand naar de server. Alleen .json-bestanden worden geaccepteerd.

* **[!UICONTROL Options]**: De connector ondersteunt de opties die in de onderstaande tabel worden beschreven.

| Optie | Beschrijving |
|:-:|:-:|
| ProxyType | Het type proxy dat wordt gebruikt om verbinding te maken met BigQuery via ODBC- en SDK-connectors. </br> HTTP (gebrek), http_no_tunnel, socks4 en socks5 worden momenteel gesteund. |
| ProxyHost | Hostnaam of IP-adres waar de proxy kan worden bereikt. |
| ProxyPort | Poortnummer waarop de proxy wordt uitgevoerd, bijvoorbeeld 8080 |
| ProxyUid | Gebruikersnaam voor de geverifieerde proxy |
| ProxyPwd | Wachtwoord ProxyUid |
| bqpath | Dit is alleen van toepassing voor bulkload (Cloud SDK). </br> Als u wilt voorkomen dat de PATH-variabele wordt gebruikt of als de Google-cloud-sdk-map naar een andere locatie moet worden verplaatst, kunt u met deze optie het exacte pad naar de SDK-binmap van de cloud op de server opgeven. |
| GCloudConfigName | Dit is alleen van toepassing vanaf versie 7.3.4 en voor bulkload (Cloud SDK).</br> De Google Cloud SDK gebruikt configuraties om gegevens in BigQuery-tabellen te laden. In de configuratie met de naam `accfda` worden de parameters voor het laden van de gegevens opgeslagen. Met deze optie kunnen gebruikers echter een andere naam voor de configuratie opgeven. |
| GCloudDefaultConfigName | Dit is alleen van toepassing vanaf versie 7.3.4 en voor bulkload (Cloud SDK).</br> De actieve Google Cloud SDK-configuratie kan niet worden verwijderd zonder de actieve tag eerst over te brengen naar een nieuwe configuratie. Deze tijdelijke configuratie is nodig om de hoofdconfiguratie voor het laden van gegevens opnieuw te maken. De standaardnaam voor de tijdelijke configuratie is `default` . Indien nodig kunt u deze naam wijzigen. |
| GCloudRecreateConfig | Dit is alleen van toepassing vanaf versie 7.3.4 en voor bulkload (Cloud SDK).</br> Wanneer dit op `false` is ingesteld, probeert het mechanisme voor bulkladen de Google Cloud SDK-configuraties niet opnieuw te maken, te verwijderen of te wijzigen. In plaats daarvan worden gegevens geladen met behulp van de bestaande configuratie op de computer. Deze functie is nuttig wanneer andere bewerkingen afhankelijk zijn van Google Cloud SDK-configuraties. </br> Als de gebruiker deze motoroptie inschakelt zonder de juiste configuratie, geeft het mechanisme voor het laden van grote hoeveelheden een waarschuwingsbericht weer: `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` . Om verdere fouten te voorkomen, zal het dan aan het gebruiken van het standaard ODBC de bulkladingsmechanisme van het Tussenvoegsel van de Serie terugkeren. |

## Opnieuw azure synapsen {#azure-synapse-redshift}

* **[!UICONTROL Server]**: URL van de Azure synapse-server

* **[!UICONTROL Account]**: Naam van de gebruiker

* **[!UICONTROL Password]**: wachtwoord gebruikersaccount

* **[!UICONTROL Database]**: naam van de database

* **[!UICONTROL Options]**

## Vertica Analytics {#vertica-analytics}

* **[!UICONTROL Server]**: URL van de [!DNL Vertica Analytics] -server

* **[!UICONTROL Account]**: Naam van de gebruiker

* **[!UICONTROL Password]**: wachtwoord gebruikersaccount

* **[!UICONTROL Database]**: naam van de database

* **[!UICONTROL Working schema]**: naam van uw werkschema.

* **[!UICONTROL Options]**: De connector ondersteunt de opties die in de onderstaande tabel worden beschreven.

De connector ondersteunt de volgende opties:

| Optie | Beschrijving |
|---|---|
| TimeZoneName | Standaard leeg, wat betekent dat de systeemtijdzone van de Campaign Classic-app-server wordt gebruikt. De optie kan worden gebruikt om de TIMEZONE-sessieparameter te forceren. |


## Amazon Redshift {#amazon-redshift}

* **[!UICONTROL Server]**: naam van de DNS

* **[!UICONTROL Account]**: Naam van de gebruiker

* **[!UICONTROL Password]**: wachtwoord gebruikersaccount

* **[!UICONTROL Database]**: naam van de database indien niet opgegeven in DSN. Deze kan leeg worden gelaten, indien opgegeven in de DSN

* **[!UICONTROL Working schema]**: naam van uw werkschema. [Meer informatie](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

