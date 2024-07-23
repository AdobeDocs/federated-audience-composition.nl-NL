---
audience: end-user
title: Aan de slag met schema's
description: Leer hoe u met schema's begint
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: d168a67fb14644dab5d33e0e9d17c850d2a66262
workflow-type: tm+mt
source-wordcount: '455'
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
>abstract="U kunt de schema&#39;s filteren op basis van hun bron. Selecteer één of verscheidene Federale Gegevensbestanden om hun schema&#39;s te tonen."


## Wat is een schema? {#schema-start}

Een schema is een representatie van een tabel in uw database. Het is een object in de toepassing dat definieert hoe de gegevens aan databasetabellen zijn gekoppeld.

Door een schema te creëren, zult u een vertegenwoordiging van uw lijst in FAC kunnen manipuleren:

- Geef deze een vriendelijke naam en beschrijving om het begrip voor de gebruiker te vereenvoudigen
- Bepaal de zichtbaarheid van elk veld op basis van het werkelijke gebruik ervan
- Selecteer zijn primaire sleutel, om schema&#39;s tussen hen te verbinden, zoals nodig in het [ gegevensmodel ](../data-management/gs-models.md#data-model-start)

## Een schema maken {#schema-create}

Volg onderstaande stappen om schema&#39;s in FAC te maken:
Ga in de sectie **[!UICONTROL FEDERATED DATA]** naar de koppeling **[!UICONTROL Models]** . Daar vindt u de tab **[!UICONTROL Schema]** .
Klik op de knop **[!UICONTROL Create schema]** .

![](assets/schema_create.png){zoomable="yes"}

U zult toegang tot een nieuwe interface met een drop-down lijst hebben waar u zult vinden
alle databases die zijn verbonden met uw toepassing. Leer meer op [ gegevensbestandverbinding ](../connections/connections.md#connections-fdb).
Selecteer de brondatabase in de lijst en klik op de tab **[!UICONTROL Add tables]**

![](assets/schema_tables.png){zoomable="yes"}

U hebt toegang tot de lijst met alle tabellen in de database.

Door de tabellen toe te voegen, waarvoor u het schema wilt maken, hebt u toegang tot de onderstaande velden.

![](assets/schema_fields.png){zoomable="yes"}

Voor elke lijst, kunt u:

- naam van schema-label wijzigen
- een beschrijving toevoegen
- Wijzig de naam van alle velden en bepaal de zichtbaarheid ervan.
- selecteer de primaire sleutel van het schema

Hier wordt bijvoorbeeld een tabel geïmporteerd vlak na het toevoegen:

![](assets/schema_lumaorder.png){zoomable="yes"}

Het schema kan als volgt worden gedefinieerd:

![](assets/schema_lumaorders.png){zoomable="yes"}

## Een schema bewerken {#schema-edit}

Als u een schema wilt bewerken, klikt u op de naam van het schema in de map schemas. U hebt toegang tot de onderstaande pagina.
Klik op de knop **[!UICONTROL Edit]** .

![](assets/schema_edit.png){zoomable="yes"}

U hebt toegang tot dezelfde mogelijkheid als wanneer u het schema maakt:

- naam van schema-label wijzigen
- een beschrijving toevoegen
- Wijzig de naam van alle velden en bepaal de zichtbaarheid ervan.
- selecteer de primaire sleutel van het schema

![](assets/schema_edit_orders.png){zoomable="yes"}

## Gegevens voorvertonen in een schema {#schema-preview}

Ga als volgt naar het tabblad **[!UICONTROL Data]** om een voorvertoning van de gegevens in de tabel weer te geven die door het schema wordt vertegenwoordigd.
U kunt het totale aantal opnamen hebben door op de koppeling **[!UICONTROL Calculate]** te klikken.

![](assets/schema_data.png){zoomable="yes"}

U kunt het gegevensoverzicht wijzigen door op de knop **[!UICONTROL Configure columns]** te klikken.

![](assets/schema_columns.png){zoomable="yes"}

## Schema verwijderen {#schema-delete}

Als u een schema wilt verwijderen, klikt u op **[!UICONTROL More]** en vervolgens op **[!UICONTROL Delete]** .

![](assets/schema_delete.png){zoomable="yes"}
