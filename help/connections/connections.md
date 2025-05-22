---
audience: end-user
title: Verbindingen met gefederaliseerde databases maken en beheren
description: Leer hoe u verbindingen met Federale databases maakt en beheert
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: e26b3cfda7c4de98d1e47fc40edd2b87859c6209
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 2%

---

# Verbindingen maken {#connections-fdb}

>[!AVAILABILITY]
>
>Voor toegang tot verbindingen hebt u een van de volgende machtigingen nodig:
>
>- **beheer Federated Gegevensbestand**
>- **Mening Federated Gegevensbestand**
>
>Voor meer informatie over de vereiste toestemmingen, te lezen gelieve de [ Gids van de Samenstelling van de Publiek van de Toegang Federatieve ](/help/start/feature-access.md).

Met Experience Platform Federated Audience Composition kan de Klant een publiek opbouwen en verrijken vanuit de gegevensopslagruimten van derden en het publiek naar Adobe Experience Platform importeren. De gesteunde gegevensopslagplaatsen zijn vermeld in [ deze sectie ](../start/access-prerequisites.md#supported-systems).

Als u met uw gefedereerde database en Adobe Experience Platform wilt werken, moet u eerst een verbinding tot stand brengen. Deze verbinding wordt ingesteld in een speciale gebruikersinterface die beschikbaar is in de Adobe Experience Platform-gebruikersinterface, zoals beschreven op deze pagina.

Ga als volgt te werk om een verbinding met uw database in te stellen:

1. Blader naar de sectie **[!UICONTROL FEDERATED DATA]** links in de track.

1. Klik in de koppeling **[!UICONTROL Federated databases]** op de knop **[!UICONTROL Add federated database]** .

   ![](assets/connections_list.png){zoomable="yes"}

1. Stel de verbinding **[!UICONTROL Properties]** in met de naam en het type van de database.

   ![](assets/connections_name.png){zoomable="yes"}

   Als u het type selecteert, hebt u toegang tot andere eigenschappen om deze in te vullen. Leer meer hier over de gesteunde gegevensbestanden op [ deze pagina ](federated-db.md).

   ![](assets/connections_details.png){zoomable="yes"}

   De configuratie-instellingen zijn afhankelijk van het type database. Blader hieronder naar de koppelingen voor toegang tot de gegevens die u nodig hebt om de verbinding in te stellen:

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Databricks](federated-db.md#databricks)
   * [Google Big Query](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)
   * [Microsoft Fabric](federated-db.md#microsoft-fabric)

1. Selecteer voor elke ondersteunde database de knop **[!UICONTROL Server IP]** . De lijst van alle IPs verbonden aan uw Federated de instanties van de Samenstelling van de Publiek tonen.

   ![](assets/connections_server_IPs.png){zoomable="yes"}

   Klik IP van de lijst om het in uw systeem te kopiëren en dit IP te machtigen om met uw gegevensbestand te verbinden.

   >[!NOTE]
   >
   >Om Federated Audience Composition voor een bepaald gegevensbestand te gebruiken, moet u alle IP adressen verbonden aan dat gegevensbestand lijsten van gewenste personen.

1. Klik op de knop **[!UICONTROL Test connection]** en op de knop **[!UICONTROL Deploy functions]** nadat u de details hebt ingevuld.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

1. Voltooi het maken van de verbinding door op de knop **[!UICONTROL Save]** te klikken.

   Een overzicht van uw Federated gegevensbestandverbinding is beschikbaar, zoals hieronder getoond:

   ![](assets/connections_overview.png){zoomable="yes"}
