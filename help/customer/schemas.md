---
audience: end-user
title: Aan de slag met schema's
description: Leer hoe u met schema's begint
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 3c0cbda211eed4fa1a8fdab015d4db4c9ad0cf30
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 2%

---

# Aan de slag met schema&#39;s {#schemas}

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Tabellen selecteren"
>abstract="Selecteer de tabellen die u wilt toevoegen voor het gegevensmodel."

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="Sleutel"
>abstract="Selecteer een sleutel voor de afstemming van gegevens."

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="Naam van het schema"
>abstract="Voer de naam van het schema in."


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="Beschrijving van schema"
>abstract="De schemabeschrijving maakt een lijst van kolommen, types en etiketten. U kunt ook de afstemmingssleutel voor het schema controleren. Klik op het potloodpictogram om de schemadefinitie bij te werken."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Brondatabase selecteren om te filteren"
>abstract="U kunt de schema&#39;s filteren op basis van hun bron. Selecteer één of verscheidene Federated gegevensbestanden om hun schema&#39;s te tonen."

## Wat is een schema {#schema-start}

Een schema is een representatie van een tabel in uw database. Het is een object in de toepassing dat definieert hoe de gegevens aan databasetabellen zijn gekoppeld.

Door een schema te maken, kunt u een representatie van de tabel definiëren in de Experience Platform Federated Audience Composition:

* Geef deze een vriendelijke naam en beschrijving om het begrip voor de gebruiker te vereenvoudigen
* De zichtbaarheid van elk veld bepalen op basis van het werkelijke gebruik ervan
* Selecteer zijn primaire sleutel, om schema&#39;s tussen hen te verbinden, zoals nodig in het [ gegevensmodel ](../data-management/gs-models.md#data-model-start)

>[!CAUTION]
>
>Wanneer u meerdere sandboxen met dezelfde database verbindt, moet u afzonderlijke werkschema&#39;s gebruiken.
>

## Een schema maken {#schema-create}

Voer de onderstaande stappen uit om schema&#39;s te maken in Federated Audience Composition:

1. Open het menu **[!UICONTROL Models]** in de sectie **[!UICONTROL Federated Data]** . Blader naar het tabblad **[!UICONTROL Schema]** en klik op **[!UICONTROL Create schema]** .

   ![](assets/schema_create.png){zoomable="yes"}

   Met deze stap hebt u toegang tot een nieuw scherm met een vervolgkeuzelijst waarin u de database(s) kunt vinden die zijn verbonden met uw omgeving. Leer meer over gegevensbestandverbinding in [ deze sectie ](../connections/connections.md#connections-fdb).

1. Selecteer de brondatabase in de lijst en klik op **[!UICONTROL Next]** .

   ![](assets/schema_tables.png){zoomable="yes"}

   U kunt dan de lijst van alle lijsten in het gegevensbestand zien.

1. Selecteer de tabellen waarvoor u het schema wilt maken.

1. Elke geselecteerde tabel genereert een schema met de gekozen kolommen. Vorm het schema en zijn kolommen zoals nodig.

   ![](assets/schema_fields.png){zoomable="yes"}

   Voor elke tabel kunt u:

   * wijzigt het label van het schema
   * een beschrijving toevoegen
   * naam van alle veldlabels wijzigen en zichtbaarheid instellen
   * selecteer de primaire sleutel van het schema

   Het schema kan als volgt worden gedefinieerd:

   ![](assets/schema_example.png)

1. Klik op **[!UICONTROL Done]** nadat u de configuratie hebt voltooid.

## Een schema bewerken {#schema-edit}

Voer de volgende stappen uit om een schema te bewerken:

1. Open het eerder gemaakte schema.

1. Klik op de knop **[!UICONTROL Edit]** .

   ![](assets/schema_edit.png){zoomable="yes"}

1. Van het **[!UICONTROL Edit schema]** venster, kunt u tot de zelfde opties toegang hebben en vormen zoals wanneer [ creërend een schema ](#schema-create).

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## Gegevens voorvertonen in een schema {#schema-preview}

Blader naar het tabblad **[!UICONTROL Data]** zoals hieronder om een voorvertoning van de gegevens in de tabel weer te geven die door het schema wordt vertegenwoordigd.

Klik op de koppeling **[!UICONTROL Calculate]** om een voorvertoning weer te geven van het totale aantal opnamen.

![](assets/schema_data.png){zoomable="yes"}

Klik op de knop **[!UICONTROL Configure columns]** om de gegevensweergave te wijzigen.

![](assets/schema_columns.png){zoomable="yes"}

## Een schema vernieuwen {#schema-refresh}

Tabellen in een gefederaliseerde database kunnen worden bijgewerkt, toegevoegd of verwijderd. In dergelijke gevallen moet u het schema in Adobe Experience Platform vernieuwen om het uit te lijnen met de meest recente wijzigingen. Om dit uit te voeren, klik de drie punten naast de naam van het schema om bij te werken en te selecteren **verfrissen schema**.

U kunt de schemadefinitie ook bijwerken wanneer het uitgeven van het.

![](assets/schema_refresh.png){zoomable="yes"}


## Schema verwijderen {#schema-delete}

Als u een schema wilt verwijderen, klikt u op de knop **[!UICONTROL More]** en kiest u **[!UICONTROL Delete]** .

![](assets/schema_delete.png){zoomable="yes"}
