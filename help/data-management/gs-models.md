---
audience: end-user
title: Aan de slag met gegevensmodellen
description: Leer hoe u begint met gegevensmodellen
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: 61a7b66d16358a4a1c3d4b2ae153e856d8f682f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---

# Aan de slag met gegevensmodellen {#data-model}

>[!CONTEXTUALHELP]
>id="dc_model_menu"
>title="Werken met modellen"
>abstract="Schema&#39;s en gegevensmodellen worden in dit scherm weergegeven. U kunt schema&#39;s en gegevensmodellen van **tot stand brengen leidt** knoop."

>[!CONTEXTUALHELP]
>id="dc_datamodel_add_schema"
>title="Schema&#39;s selecteren"
>abstract="Selecteer de schema&#39;s voor het gegevensmodel."


>[!CONTEXTUALHELP]
>id="dc_datamodel_add_audience"
>title="Een publiek selecteren"
>abstract="Selecteer het publiek voor het gegevensmodel."

>[!CONTEXTUALHELP]
>id="dc_datamodel_properties"
>title="Eigenschappen van Datamodel"
>abstract="Voer het label van het gegevensmodel in."


## Wat is een gegevensmodel {#data-model-start}

Een gegevensmodel is een reeks schema&#39;s, publiek, en de verbindingen tussen hen. Het wordt gebruikt om publiek met gegevensbestandgegevens te verbinden.

Leer meer over [ schema&#39;s ](../customer/schemas.md#schema-start).

Leer meer over [ publiek ](../start/audiences.md).

U ziet bijvoorbeeld onder een weergave van een gegevensmodel de tabellen met hun naam en de koppelingen daartussen.

![](assets/datamodel.png){zoomable="yes"}

In Federated Audience Composition, is het mogelijk om vele gegevensmodellen tot stand te brengen.

Het maken van deze bestanden is gebaseerd op het gebruiksgeval: u kiest de benodigde tabellen en u koppelt deze aan uw behoeften.

## Een gegevensmodel maken {#data-model-create}

Ga als volgt te werk om een gegevensmodel te maken:

1. Open in de sectie **[!UICONTROL Federated Data]** het menu **[!UICONTROL Models]** en blader naar de tab **[!UICONTROL Data model]** .

   Klik op de knop **[!UICONTROL Create data model]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Definieer de naam van het gegevensmodel en klik op de knop **[!UICONTROL Create]** .

1. Klik op het dashboard van het gegevensmodel op **[!UICONTROL Add schemas]** om het schema te kiezen dat aan het gegevensmodel is gekoppeld.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

1. Klik op **[!UICONTROL Add Audiences]** om de doelgroepen te definiëren.

1. Vestig verbindingen tussen lijsten in uw gegevensmodel om nauwkeurige gegevensverhoudingen te verzekeren. [Meer informatie](#data-model-links)

1. Nadat u de configuratie hebt voltooid, klikt u op **[!UICONTROL Save]** om de wijzigingen toe te passen.

## Koppelingen maken {#data-model-links}

Ga als volgt te werk om koppelingen tot stand te brengen tussen tabellen in uw datamodel:

1. Klik op het menu **[!UICONTROL Create link]** van een van de tabellen of klik op de knop **[!UICONTROL Create links]** en kies de twee tabellen:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Vul het opgegeven formulier in om de koppeling te definiëren.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Kardinaliteit**

   * **1-n**: één voorkomen van de bronlijst kan verscheidene overeenkomstige voorkomen van de doellijst hebben, maar één voorkomen van de doellijst kan hoogstens één overeenkomstige voorkomen van de bronlijst hebben.

   * **n-1**: één voorkomen van de doellijst kan verscheidene overeenkomstige voorkomen van de bronlijst hebben, maar één voorkomen van de bronlijst kan hoogstens één overeenkomstige voorkomen van de doellijst hebben.

   * **1-1**: één voorkomen van de bronlijst kan hoogstens één overeenkomstige voorkomen van de doellijst hebben.

Alle koppelingen die voor uw datamodel zijn gedefinieerd, worden hieronder weergegeven:

![](assets/datamodel_alllinks.png){zoomable="yes"}

## Video {#data-model-video}

Leer hoe u een gegevensmodel maakt in deze video:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
