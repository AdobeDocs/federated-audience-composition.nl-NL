---
audience: end-user
title: Verbindingen met Federale Databases maken en beheren
description: Leer hoe te om verbindingen met Federale Gegevensbestanden tot stand te brengen en te beheren
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: 98689f24fc7eeffa4cdfa5418c160c13abba7527
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 5%

---

# Verbindingen maken {#connections-fdb}

Als u rechtstreeks met een gefedereerde database werkt in AEP, moet u een verbinding tot stand brengen.

Als u een verbinding met uw database wilt instellen, gaat u naar de sectie **[!UICONTROL FEDERATED DATA]** en klikt u in de koppeling **[!UICONTROL Federated Databases]** op de knop **[!UICONTROL Add federated database]** .

![](assets/connections_list.png){zoomable="yes"}

U krijgt toegang tot het venster voor de verbinding **[!UICONTROL Properties]** met de naam en het type van de database.

![](assets/connections_name.png){zoomable="yes"}

Als u het type selecteert, hebt u toegang tot andere eigenschappen die u wilt invullen. [ leer meer hier over de gesteunde gegevensbestanden ](federated-db.md).

![](assets/connections_details.png){zoomable="yes"}

Afhankelijk van het type van uw gegevensbestand, leer in de verbindingen onder de informatie u aan opstelling de verbinding nodig hebt:
* [Amazon Redshift](federated-db.md#amazon-redshift)
* [Azure synapse](federated-db.md#azure-synapse-redshift)
* [Google Big Query](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

Klik op de knop **[!UICONTROL Test connection]** en op de knop **[!UICONTROL Deploy functions]** nadat u de details hebt ingevuld.
Voltooi het maken van de verbinding door op de knop **[!UICONTROL Save]** te klikken.

![](assets/connections_testdeploy.png){zoomable="yes"}

U zult een overzicht van uw Federated gegevensverbinding als dit hebben:

![](assets/connections_overview.png){zoomable="yes"}