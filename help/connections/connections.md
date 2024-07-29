---
audience: end-user
title: Verbindingen met Federale Databases maken en beheren
description: Leer hoe te om verbindingen met Federale Gegevensbestanden tot stand te brengen en te beheren
badge: label="Beperkte beschikbaarheid" type="Informative"
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# Verbindingen maken {#connections-fdb}

Met Experience Platform Federated Audience Composition kan de Klant een publiek opbouwen en verrijken vanuit de gegevensopslagruimten van derden en het publiek naar Adobe Experience Platform importeren.

Als u met uw gefedereerde database en Adobe Experience Platform wilt werken, moet u eerst een verbinding tot stand brengen. Deze verbinding wordt ingesteld in een speciale gebruikersinterface die beschikbaar is in de Adobe Experience Platform-gebruikersinterface, zoals beschreven op deze pagina.

Ga als volgt te werk om een verbinding met uw database in te stellen:

1. Blader naar de sectie **[!UICONTROL FEDERATED DATA]** links in de track.

1. Klik in de koppeling **[!UICONTROL Federated Databases]** op de knop **[!UICONTROL Add federated database]** .

   ![](assets/connections_list.png){zoomable="yes"}

1. Stel de verbinding **[!UICONTROL Properties]** in met de naam en het type van de database.

   ![](assets/connections_name.png){zoomable="yes"}

   Als u het type selecteert, hebt u toegang tot andere eigenschappen om deze in te vullen. Leer meer hier over de gesteunde gegevensbestanden in [ deze pagina ](federated-db.md).

   ![](assets/connections_details.png){zoomable="yes"}

   De configuratie-instellingen zijn afhankelijk van het type database. Blader hieronder naar de koppelingen voor toegang tot de gegevens die u nodig hebt om de verbinding in te stellen:

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure synapse](federated-db.md#azure-synapse-redshift)
   * [Google Big Query](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Klik op de knop **[!UICONTROL Test connection]** en op de knop **[!UICONTROL Deploy functions]** nadat u de details hebt ingevuld.

1. Voltooi het maken van de verbinding door op de knop **[!UICONTROL Save]** te klikken.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

   Er is een overzicht beschikbaar van uw Federated Database-verbinding, zoals hieronder wordt getoond:

   ![](assets/connections_overview.png){zoomable="yes"}
