---
audience: end-user
title: Aan de slag met gegevensmodellen
description: Leer hoe u begint met gegevensmodellen
badge: label="Beperkte beschikbaarheid" type="Informative"
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: 2eef334ccc5b6c342a26dc452b76dc61f272ba84
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

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


## Wat is een gegevensmodel? {#data-model-start}

Een gegevensmodel is een reeks schema&#39;s, publiek, en de verbindingen tussen hen. Het wordt gebruikt om publiek met gegevensbestandgegevens te verbinden.

Leer meer over [ schema&#39;s ](../customer/schemas.md#schema-start).

Leer meer over [ publiek ](../start/audiences.md).

U ziet bijvoorbeeld onder een weergave van een gegevensmodel de tabellen met hun naam en de koppelingen daartussen.

![](assets/datamodel.png){zoomable="yes"}

In Federated Audience Composition, is het mogelijk om vele gegevensmodellen tot stand te brengen.

Het maken van deze bestanden is gebaseerd op het gebruiksgeval: u kiest de benodigde tabellen en u koppelt deze aan uw behoeften.

## Een gegevensmodel maken {#data-model-create}

Ga als volgt te werk om een gegevensmodel te maken:

1. Ga in de sectie **[!UICONTROL FEDERATED DATA]** naar de koppeling **[!UICONTROL Models]** en blader naar de tab **[!UICONTROL Data model]** .

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Klik op de knop **[!UICONTROL Create data model]** om de naam van het gegevensmodel te definiëren en klik op de knop **[!UICONTROL Create]** .

   ![](assets/datamodel_name.png){zoomable="yes"}

1. Voeg vervolgens de schema&#39;s, het publiek en de koppelingen van uw gegevensmodel toe.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

### Koppelingen maken {#data-model-links}

Ga als volgt te werk om koppelingen tot stand te brengen tussen tabellen in uw datamodel:

1. Klik op het menu **[!UICONTROL Create link]** van een van de tabellen of klik op de knop **[!UICONTROL Create links]** en kies de twee tabellen:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Vul het opgegeven formulier in om de koppeling te definiëren.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Kardinaliteit**

   * 1-N: één instantie van de brontabel kan meerdere overeenkomende instanties van de doeltabel hebben, maar één instantie van de doeltabel kan maximaal één overeenkomende instantie van de brontabel hebben.

   * N-1: één instantie van de doeltabel kan meerdere overeenkomende instanties van de brontabel hebben, maar één instantie van de brontabel kan maximaal één overeenkomende instantie van de doeltabel hebben.

   * 1-1: één instantie van de brontabel kan maximaal één overeenkomende instantie van de doeltabel hebben.

Alle koppelingen die voor uw datamodel zijn gedefinieerd, worden hieronder weergegeven:

![](assets/datamodel_alllinks.png){zoomable="yes"}

## Video {#data-model-video}

Leer hoe u een gegevensmodel maakt in deze video:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
