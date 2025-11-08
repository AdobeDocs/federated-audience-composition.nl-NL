---
audience: end-user
title: Verbindingen met gefederaliseerde databases maken en beheren
description: Leer hoe u verbindingen met Federale databases maakt en beheert
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: 4ad3897bec276cf4c63f9192ce34b17bd598fe84
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 1%

---

# Verbindingen maken {#connections-fdb}

>[!AVAILABILITY]
>
>Voor toegang tot verbindingen hebt u een van de volgende machtigingen nodig:
>
>- **beheer Federated Gegevensbestand**
>- **Mening Federated Gegevensbestand**
>
>Voor meer informatie over de vereiste toestemmingen, te lezen gelieve de [&#x200B; gids van de toegangscontrole &#x200B;](/help/governance-privacy-security/access-control.md).

Met de Experience Platform Federated Audience Composition kunt u een publiek opbouwen en verrijken vanuit de gegevensopslagruimten van derden en het publiek importeren naar Adobe Experience Platform.

## Ondersteunde databases {#supported-databases}

Als u met uw gefedereerde database en Adobe Experience Platform wilt werken, moet u eerst een verbinding tot stand brengen tussen de twee bronnen. Met Federated Audience Composition kunt u verbinding maken met de volgende databases.

&#x200B;* Amazon Redshift
&#x200B;* Azure Synapse Analytics
&#x200B;* Databricks
&#x200B;* Google BigQuery
&#x200B;* Microsoft Fabric
&#x200B;* Oracle
&#x200B;* Snowflake
&#x200B;* Vertica Analytics

## Verbinding maken {#create}

Als u een verbinding wilt maken, selecteert u **[!UICONTROL Federated databases]** in de sectie Federatieve gegevens.

![&#x200B; de Federated knoop van Gegevensbestanden wordt benadrukt binnen de linkernavigatie.](assets/home/select-federated.png){zoomable="yes" width="70%" align="center"}

De sectie Federated databases wordt weergegeven. Selecteer **[!UICONTROL Add federated database]** om een verbinding te maken.

![&#x200B; Add wordt de federated gegevensbestandknoop benadrukt binnen de Federated pagina van de gegevensbestandvertoning.](assets/home/add-federated.png){zoomable="yes" width="70%" align="center"}

De pop-up Verbindingseigenschappen wordt weergegeven. U kunt uw verbinding een naam geven en selecteren welk type database u wilt maken.

![&#x200B; de gefederaliseerde gegevensbestandtypes worden getoond.](assets/home/select-type.png){zoomable="yes" width="70%" align="center"}

Nadat u een type hebt geselecteerd, wordt de sectie **[!UICONTROL Details]** weergegeven. Deze sectie verschilt op basis van het eerder gekozen databasetype.

>[!BEGINTABS]

>[!TAB  Amazon Redshift ]

>[!AVAILABILITY]
>
>Alleen Amazon Redshift AWS, Amazon Redshift Spectrum en Amazon Redshift Serverless worden ondersteund.
>
>Bovendien, wordt de veilige toegang tot uw externe Amazon Redshift gegevenspakhuis door privé verbinding gesteund.

Nadat u Amazon Redshift hebt geselecteerd, kunt u de volgende details toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Server | De naam van de gegevensbron. |
| Account | De gebruikersnaam van de account. |
| Wachtwoord | Het wachtwoord van de account. |
| Database | De naam van de database. Als dit in de servernaam wordt gespecificeerd, kan dit gebied leeg worden verlaten. |
| Werkschema | De naam van het schema van het gegevensbestand voor werklijsten te gebruiken. Meer informatie over deze eigenschap kan in de [&#x200B; documentatie van het Schema van Amazon &#x200B;](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"} worden gevonden.<br/><br/>**Nota:** u kunt om het even welk schema van het gegevensbestand gebruiken, met inbegrip van schema&#39;s die voor tijdelijke gegevensverwerking worden gebruikt, zolang u de vereiste toestemmingen hebt om met dit schema te verbinden. Nochtans, moet u **&#x200B;**&#x200B;duidelijke het werken schema&#39;s gebruiken wanneer het verbinden van veelvoudige zandbakken met het zelfde gegevensbestand. |

>[!TAB  Analytics van Azure Synapse ]

>[!NOTE]
>
>Neem contact op met uw Adobe Customer Care-medewerker als u een veilige verbinding wilt maken met Azure Synapse Analytics.

Nadat u Azure Synapse Analytics hebt geselecteerd, kunt u de volgende gegevens toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Server | De URL van de Azure Synapse-server. |
| Account | De gebruikersnaam voor de Azure Synapse-account. |
| Wachtwoord | Het wachtwoord voor de Azure-synapsaccount. |
| Database | De naam van de database. Als dit in de servernaam wordt gespecificeerd, kan dit gebied leeg worden verlaten. |
| Opties | Aanvullende opties voor de verbinding. Voor Azure Synapse Analytics kunt u het type verificatie opgeven dat door de connector wordt ondersteund. Federated Audience Composition biedt momenteel ondersteuning voor `ActiveDirectoryMSI` . Voor meer informatie over verbindingskoorden, te lezen gelieve de [&#x200B; sectie van de koorden van de voorbeeldverbinding binnen de documentatie van Microsoft &#x200B;](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}. |

>[!TAB  Gegevensbestanden ]

>[!NOTE]
>
>De veilige toegang tot uw extern gegevenspakhuis van Gegevensbestanden door privé verbinding wordt gesteund. Dit omvat veilige verbindingen met Databricks-databases die worden gehost op Amazon Web Services (AWS) via privékoppelingen en databases die worden gehost op Microsoft Azure via VPN. Neem contact op met uw Adobe-vertegenwoordiger voor hulp bij het instellen van veilige toegang.

Na het selecteren van Gegevensbestanden, kunt u de volgende details toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Server | De naam van de Databricks-server. |
| HTTP-pad | De weg aan uw Cluster of Warehouse. Voor meer informatie over de weg, te lezen gelieve de [&#x200B; documentatie van Gegevensbestanden over verbindingsdetails &#x200B;](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}. |
| Wachtwoord | Het toegangstoken voor de server van Gegevensbestanden. Voor meer informatie over deze waarde, te lezen gelieve de [&#x200B; documentatie van Gegevensbestanden over persoonlijke toegangstokens &#x200B;](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}. |
| Catalogus | De naam van de catalogus met databases. Voor meer informatie over catalogi in Gegevensbestanden, te lezen gelieve de [&#x200B; documentatie van Gegevensbestanden over catalogi &#x200B;](https://docs.databricks.com/aws/en/catalogs/){target="_blank"} |
| Werkschema | De naam van het databaseschema dat moet worden gebruikt voor de werktabellen. <br/><br/>**Nota:** u kunt **om het even welk** schema van het gegevensbestand gebruiken, met inbegrip van schema&#39;s die voor tijdelijke gegevensverwerking worden gebruikt, zolang u de vereiste toestemmingen hebt om met dit schema te verbinden. Nochtans, moet u **&#x200B;**&#x200B;duidelijke het werken schema&#39;s gebruiken wanneer het verbinden van veelvoudige zandbakken met het zelfde gegevensbestand. |
| Opties | Aanvullende opties voor de verbinding. De beschikbare opties worden weergegeven in de volgende tabel. |

Voor Databases kunt u de volgende aanvullende opties instellen:

| Opties | Beschrijving |
| ------- | ----------- |
| TimeZoneName | De naam van de te gebruiken tijdzone. Deze waarde vertegenwoordigt de sessieparameter `TIMEZONE` . Voor meer informatie over tijdstreken, gelieve de [&#x200B; documentatie van Gegevensbestanden over timezones &#x200B;](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"} te lezen. |

>[!TAB  Google BigQuery ]

>[!NOTE]
>
>De veilige toegang tot uw extern gegevenspakhuis van Google BigQuery door VPN wordt gesteund.

Nadat u Google BigQuery hebt geselecteerd, kunt u kiezen welke verificatiemethode u wilt gebruiken wanneer u verbinding maakt met Federated Audience Composition.

Als u **[!UICONTROL Account/Password Authentication]** selecteert, kunt u de volgende aanmeldingsgegevens toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Serviceaccount | Het e-mailadres van uw serviceaccount. Voor meer informatie, te lezen gelieve de [&#x200B; documentatie van de de dienstrekening van de Wolk van Google &#x200B;](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}. |

Als u **[!UICONTROL OAuth 2.0]** selecteert, kunt u de volgende aanmeldingsgegevens toevoegen:

>[!NOTE]
>
>Voordat u verbinding maakt met Google BigQuery via OAuth 2.0, moet u de omleidings-URL configureren in uw Google Cloud-project. Voeg de omleidings-URL `https://fac-oauth.adobe.io/oauth` toe aan uw Google Cloud-project onder uw OAuth 2.0-client-id-configuratie.

| Veld | Beschrijving |
| ----- | ----------- |
| Client-id | De client-id van uw Google BigQuery-project. Dit veld fungeert als een gebruikersnaam voor uw project. |
| Clientgeheim | Het clientgeheim van uw Google BigQuery-project. Dit veld fungeert als een wachtwoord voor uw project. |
| Toegangsbereik | De vooraf ingevulde informatie die van het werkingsgebied uw Token OAuth een lijst maakt wordt geautoriseerd voor binnen uw middelen van de Wolk van Google. |

Selecteer **[!UICONTROL Sign in]** om uw verificatie te voltooien.

Na het invoeren van uw login details, kunt u de volgende details toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Project | De id van uw project. Voor meer informatie, te lezen gelieve de [&#x200B; het projectdocumentatie van de Wolk van Google &#x200B;](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}. |
| Gegevensset | De naam van de gegevensset. Voor meer informatie, te lezen gelieve de [&#x200B; documentatie van de Cloud van Google &#x200B;](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}. |
| Hoofdbestandspad | Het sleutelbestand naar de server. Alleen `json` bestanden worden ondersteund. |
| Opties | Aanvullende opties voor de verbinding. De beschikbare opties worden weergegeven in de volgende tabel. |

Voor Google BigQuery kunt u de volgende aanvullende opties instellen:

| Opties | Beschrijving |
| ------- | ----------- |
| ProxyType | Het type proxy dat wordt gebruikt om verbinding te maken met BigQuery. Tot de ondersteunde waarden behoren `HTTP` , `http_no_tunnel` , `socks4` en `socks5` . |
| ProxyHost | De hostnaam of het IP-adres waar de proxy kan worden bereikt. |
| ProxyUid | Het poortnummer waarop de proxy wordt uitgevoerd. |
| ProxyPwd | Het wachtwoord voor de proxy. |
| bgpath | **Nota:** dit is slechts van toepassing voor het **bulk-lading hulpmiddel** (SDK van de Wolk). <br/><br/> Het pad naar de map Cloud SDK bin op de server. U hoeft dit alleen in te stellen als u de map `google-cloud-sdk` naar een andere locatie hebt verplaatst of als u de variabele PATH niet wilt gebruiken. |
| GCloudConfigName | **Nota:** dit is slechts van toepassing voor het **bulk-lading hulpmiddel** (Wolk SDK) boven versie 7.3.4. <br/><br/> De naam van de configuratie die de parameters voor het laden van de gegevens opslaat. Deze waarde is standaard `accfda` . |
| GCloudDefaultConfigName | **Nota:** dit is slechts van toepassing voor het **bulk-lading hulpmiddel** (Wolk SDK) boven versie 7.3.4. <br/><br/> De naam van de tijdelijke configuratie om de belangrijkste configuratie voor ladingsgegevens te ontspannen. Deze waarde is standaard `default` . |
| GCloudRecreateConfig | **Nota:** dit is slechts van toepassing voor het **bulk-lading hulpmiddel** (Wolk SDK) boven versie 7.3.4. <br/><br/> Een booleaanse waarde die u laat beslissen als het bulkladingsmechanisme automatisch de configuraties van SDK van de Wolk van Google zou moeten ontspannen, schrappen of wijzigen. Als deze waarde is ingesteld op `false` , worden gegevens geladen via een bestaande configuratie op de computer. Als deze waarde is ingesteld op `true` , moet u controleren of de configuratie juist is ingesteld. Als dit niet het geval is, wordt de fout `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` weergegeven en wordt het laadmechanisme weer ingesteld op het standaardlaadmechanisme. |

>[!TAB  de Stof van Microsoft ]

Nadat u Microsoft Fabric hebt geselecteerd, kunt u de volgende gegevens toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Server | De URL voor de Microsoft Fabric-server. |
| Toepassings-id | The application ID for Microsoft Fabric. Voor meer informatie over toepassingsidentiteitskaart, te lezen gelieve de [&#x200B; documentatie van de Stof van Microsoft over toepassingsopstelling &#x200B;](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app){target="_blank"}. |
| Clientgeheim | Het clientgeheim voor de toepassing. Voor meer informatie over het cliëntgeheim, te lezen gelieve de [&#x200B; documentatie van de Stof van Microsoft over toepassingsopstelling &#x200B;](https://learn.microsoft.com/en-us/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}. |
| Opties | Aanvullende opties voor de verbinding. De beschikbare opties worden weergegeven in de volgende tabel. |

Voor Microsoft Fabric kunt u de volgende aanvullende opties instellen:

| Optie | Beschrijving |
| ------ | ----------- |
| Verificatie | Het type van authentificatie die door de schakelaar wordt gebruikt. Tot de ondersteunde waarden behoren: `ActiveDirectoryMSI` . Voor meer informatie, te lezen gelieve de [&#x200B; documentatie van Microsoft over opslagconnectiviteit &#x200B;](https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity){target="_blank"}. |

>[!TAB  Oracle ]

>[!NOTE]
>
>Federated Audience Composition biedt ondersteuning voor gefederaliseerde verbindingsinstellingen met Oracle-databases op versie 11g of hoger en worden gehost op AWS, Azure, Exadata of een privécloud (mits deze toegankelijk is via een extern netwerk). Neem contact op met de Adobe Customer Care als u nog vragen hebt over het instellen van de Oracle-database of als u een veilige verbinding met Oracle wilt maken.

Nadat u Oracle hebt geselecteerd, kunt u de volgende gegevens toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Server | De URL voor de Oracle-server. |
| Account | De gebruikersnaam van de account. |
| Wachtwoord | Het wachtwoord van de account. |

>[!TAB  Snowflake ]

>[!NOTE]
>
>Beveiligde toegang tot uw externe Snowflake-gegevenspakhuis via een persoonlijke koppeling wordt ondersteund. Je Snowflake-account moet worden gehost op Amazon Web Services (AWS) of Azure en zich in dezelfde regio bevinden als je Federated Audience Composition-omgeving. Neem contact op met uw Adobe-vertegenwoordiger voor hulp bij het instellen van veilige toegang tot uw Snowflake-account.

Nadat u Snowflake hebt geselecteerd, kunt u kiezen welke verificatiemethode u wilt gebruiken wanneer u verbinding maakt met Federatieve Audience Composition.

Als u **[!UICONTROL Account/Password Authentication]** selecteert, kunt u de volgende aanmeldingsgegevens toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Server | De naam van de server. |
| Gebruiker | De gebruikersnaam voor de account. |
| Wachtwoord | Het wachtwoord voor de account. |

Als u **[!UICONTROL OAuth 2.0]** selecteert, kunt u de volgende aanmeldingsgegevens toevoegen:

>[!NOTE]
>
>Voordat u verbinding maakt met Snowflake via OAuth 2.0, moet u de omleidings-URL configureren in uw Snowflake OAuth-integratieobject. Voeg de omleidings-URL `https://fac-oauth.adobe.io/oauth` toe aan uw Snowflake OAuth-integratieconfiguratie.

| Veld | Beschrijving |
| ----- | ----------- |
| Server | De naam van de server. |
| Client-id | De client-id van uw Snowflake-project. Dit veld fungeert als een gebruikersnaam voor uw project. |
| Clientgeheim | Het clientgeheim van uw Snowflake-project. Dit veld fungeert als een wachtwoord voor uw project. |

Selecteer **[!UICONTROL Sign in]** om uw verificatie te voltooien.

Na het invoeren van uw login details, kunt u de volgende details toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Database | De naam van de database. Als dit in de servernaam wordt gespecificeerd, kan dit gebied leeg worden verlaten. |
| Werkschema | De naam van het databaseschema dat moet worden gebruikt voor de werktabellen. <br/><br/>**Nota:** u kunt **om het even welk** schema van het gegevensbestand gebruiken, met inbegrip van schema&#39;s die voor tijdelijke gegevensverwerking worden gebruikt, zolang u de vereiste toestemmingen hebt om met dit schema te verbinden. Nochtans, moet u **&#x200B;**&#x200B;duidelijke het werken schema&#39;s gebruiken wanneer het verbinden van veelvoudige zandbakken met het zelfde gegevensbestand. |
| Persoonlijke sleutel | De persoonlijke sleutel voor uw databaseverbinding. U kunt een `.pem` -bestand uploaden vanaf uw lokale systeem. |
| Opties | Aanvullende opties voor de verbinding. De beschikbare opties worden weergegeven in de volgende tabel. |

Voor Snowflake kunt u de volgende aanvullende opties instellen:

| Opties | Beschrijving |
| ------- | ----------- |
| werkschema | De naam van het databaseschema dat moet worden gebruikt voor werktabellen. |
| TimeZoneName | De naam van de te gebruiken tijdzone. Deze waarde vertegenwoordigt de sessieparameter `TIMEZONE` . Standaard wordt de tijdzone van het systeem gebruikt. Voor meer informatie over tijdstreken, te lezen gelieve de [&#x200B; documentatie van Snowflake op timezones &#x200B;](https://docs.snowflake.com/en/sql-reference/parameters#timezone){target="_blank"}. |
| WeekStart | De dag waarop je de week wilt beginnen. Deze waarde vertegenwoordigt de sessieparameter `WEEK_START` . Voor meer informatie over week begin, gelieve te lezen de [&#x200B; documentatie van Snowflake op de parameter van het wekbegin &#x200B;](https://docs.snowflake.com/en/sql-reference/parameters#week-start){target="_blank"} |
| UseCachedResult | Een Booleaanse waarde die bepaalt of de resultaten in de cache van Snowflake worden gebruikt. Deze waarde vertegenwoordigt de sessieparameter `USE_CACHED_RESULTS` . Deze waarde is standaard ingesteld op true. Voor meer informatie over deze parameter, te lezen gelieve de [&#x200B; documentatie van Snowflake over het voortbestaan van resultaten &#x200B;](https://docs.snowflake.com/en/user-guide/querying-persisted-results){target="_blank"}. |
| bulkThreads | Het aantal threads dat moet worden gebruikt voor Snowflake-bulklader. Hoe meer threads toegevoegd worden, hoe beter de prestaties zijn voor grotere bulkladingen. Deze waarde is standaard ingesteld op 1. |
| chunkSize | De bestandsgrootte van het segment van elke bulklader. Wanneer u deze bestanden tegelijkertijd met meer threads gebruikt, kunt u de prestaties van de bulkladingen verbeteren. Deze waarde is standaard ingesteld op 128 MB. Voor meer informatie over brokgrootte, te lezen gelieve de [&#x200B; documentatie van Snowflake bij het voorbereiden van gegevensdossiers &#x200B;](https://docs.snowflake.com/en/user-guide/data-load-considerations-prepare){target="_blank"}. |
| StageName | De naam van een vooraf ingericht intern opvoerende milieu. Dit kan in bulkladingen in plaats van het creëren van een nieuw tijdelijk stadium worden gebruikt. |

>[!TAB  Vertica Analytics ]

Nadat u Vertica Analytics hebt geselecteerd, kunt u de volgende gegevens toevoegen:

| Veld | Beschrijving |
| ----- | ----------- |
| Server | De URL van de Vertica Analytics-server. |
| Account | De gebruikersnaam van de account. |
| Wachtwoord | Het wachtwoord van de account. |
| Database | De naam van de database. Als dit in de servernaam wordt gespecificeerd, kan dit gebied leeg worden verlaten. |
| Werkschema | De naam van het databaseschema dat moet worden gebruikt voor de werktabellen. <br/><br/>**Nota:** u kunt **om het even welk** schema van het gegevensbestand gebruiken, met inbegrip van schema&#39;s die voor tijdelijke gegevensverwerking worden gebruikt, zolang u de vereiste toestemmingen hebt om met dit schema te verbinden. Nochtans, moet u **&#x200B;**&#x200B;duidelijke het werken schema&#39;s gebruiken wanneer het verbinden van veelvoudige zandbakken met het zelfde gegevensbestand. |
| Opties | Aanvullende opties voor de verbinding. De beschikbare opties worden weergegeven in de volgende tabel. |

Voor Vertica Analytics kunt u de volgende aanvullende opties instellen:

| Opties | Beschrijving |
| ------- | ----------- |
| TimeZoneName | De naam van de te gebruiken tijdzone. Deze waarde vertegenwoordigt de sessieparameter `TIMEZONE` . Voor meer informatie over timezones, gelieve de [&#x200B; documentatie van Vertica Analytics op timezones &#x200B;](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"} te lezen |

>[!ENDTABS]

Na het toevoegen van de details van de verbinding, gelieve nota te nemen van de volgende extra montages:

>[!NOTE]
>
>Om Federatieve Samenstelling van het Publiek voor een bepaald gegevensbestand te gebruiken, moet u **alle** van de IP adressen verbonden aan dat gegevensbestand lijsten van gewenste personen.

| Instellingen | Details |
| -------- | ------- |
| Verbinding inschakelen | Een Booleaanse schakeloptie die bepaalt of de verbinding automatisch wordt ingeschakeld. |
| Server-IP&#39;s | Een popover die toont welke IP adressen moeten worden gevoegd op lijst van gewenste personen om met het gegevensbestand te verbinden. |
| Verbinding testen | Hiermee kunt u de configuratiegegevens verifiëren. |

U kunt nu **[!UICONTROL Deploy functions]** selecteren, gevolgd door **[!UICONTROL Add]** om de verbinding tussen de gefedereerde database en Experience Platform te voltooien.

