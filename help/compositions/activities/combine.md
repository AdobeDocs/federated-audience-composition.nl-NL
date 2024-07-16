---
audience: end-user
title: De combinatie-activiteit gebruiken
description: Meer informatie over het gebruik van de combinatieactiviteit
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 12%

---


# Combineren {#combine}

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Combineer activiteit"
>abstract="**combineert** activiteit staat u toe om segmentatie op uw binnenkomende bevolking uit te voeren. U kunt dus meerdere populaties combineren, een deel ervan uitsluiten of gegevens alleen gemeenschappelijk houden voor meerdere doelen."

**combineert** activiteit staat u toe om segmentatie op uw binnenkomende bevolking uit te voeren. U kunt dus meerdere populaties combineren, een deel ervan uitsluiten of gegevens alleen gemeenschappelijk houden voor verschillende doelen.

**combineer** activiteit kan na een andere activiteit, maar niet aan het begin van de samenstelling worden geplaatst. Om het even welke activiteit kan worden geplaatst na **combineren**.

## De combinatieactiviteit configureren {#combine-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Samenvoegopties voor doorsnede"
>abstract="**doorsnede** staat u toe om slechts de elementen gemeenschappelijk voor de verschillende binnenkomende populaties in de activiteit te houden. In de **Reeksen om zich bij** sectie aan te sluiten, controleer alle vorige activiteiten u zich wilt aansluiten bij."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Samenvoegopties voor uitsluiting"
>abstract="De **uitsluiting** staat u toe om elementen van één bevolking volgens bepaalde criteria uit te sluiten. In de **Reeksen om zich bij** sectie aan te sluiten, controleer alle vorige activiteiten u zich wilt aansluiten bij."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Selecteer het segmentatietype"
>abstract="Selecteer hoe u het publiek wilt combineren: verenigen, doorsnijden of uitsluiten."

Volg deze gemeenschappelijke stappen beginnen de **te vormen combineren** activiteit:

1. Voeg meerdere activiteiten toe om minstens twee verschillende uitvoeringstakken te vormen.

1. Voeg a **** activiteit aan om het even welke vorige takken combineren.

1. Selecteer het segmentatietype: [ Vereniging ](#union), [ Intersectie ](#intersection) of [ Uitsluiting ](#exclusion), en klik **gaat** verder.

   ![](../assets/combine.png)

1. In de **Reeksen om zich bij** sectie aan te sluiten, controleer alle vorige activiteiten u zich wilt aansluiten.

## Samenvoegen {#combine-union}

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Afstemmingsopties voor doorsnede"
>abstract="Selecteer het afstemmingstype om te bepalen hoe duplicaten worden verwerkt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Afstemmingsopties"
>abstract="Selecteer het **Type van Verzoening** om te bepalen hoe te om duplicaten te behandelen."

In **combineer** activiteit, kunt u a **Vereniging** vormen.

![](../assets/combine-union.png)

Voor dit, moet u het **Type van Verzoening** selecteren om te bepalen hoe de duplicaten worden behandeld:

* **Sleutels slechts**: dit is de standaardwijze. De activiteit behoudt slechts één element wanneer elementen van de verschillende binnenkomende overgangen dezelfde sleutel hebben. Deze optie kan alleen worden gebruikt als de binnenkomende populaties homogeen zijn.
* **een selectie van kolommen**: selecteer deze optie om de lijst van kolommen te bepalen waarop de gegevensverzoening wordt toegepast. U moet eerst de primaire set (de set met de brondata) selecteren en vervolgens de kolommen die u voor de samenvoeging wilt gebruiken.

## Doorsnede {#combine-intersection}

In **combineer** activiteit, kunt u een **Intersection** vormen.

![](../assets/combine-intersection.png)

Hiervoor voert u de volgende extra stappen uit:

1. Selecteer het **Type van Verzoening** om te bepalen hoe de duplicaten worden behandeld. Zie [ Unie ](#union) sectie.
1. U kunt **controleren produceert complementaire** optie als u wenst om de resterende bevolking te verwerken. Het complement zal de samenvoeging bevatten van de resultaten van alle binnenkomende activiteiten min de doorsnede. Een extra uitgaande overgang zal dan aan de activiteit worden toegevoegd.

## Uitsluiting {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Uitsluitingsregels"
>abstract="Indien nodig, kunt u binnenkomende lijsten manipuleren. Immers, om een doel van een ander schema uit te sluiten, dat ook als het richten dimensie wordt bekend, moet dit doel aan het zelfde schema worden teruggekeerd zoals het belangrijkste doel. Om dit te doen, klik **een regel** in de E **sectie van de uitsluitingsregels** toevoegen en de voorwaarden van de schemaverandering specificeren. Afstemming van gegevens vindt plaats via een attribuut of een join-functie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Te combineren sets selecteren"
>abstract="In de **Reeksen om zich bij** sectie aan te sluiten, selecteer de **Primaire reeks** van de binnenkomende overgangen. Dit is de set waaruit elementen worden uitgesloten. De andere sets komen overeen met de elementen voordat deze worden uitgesloten van de primaire set."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Uitsluitingsregels"
>abstract="Indien nodig, kunt u binnenkomende lijsten manipuleren. Immers, om een doel van een ander schema uit te sluiten, dat ook als het richten dimensie wordt bekend, moet dit doel aan het zelfde schema worden teruggekeerd zoals het belangrijkste doel. Om dit te doen, klik **een regel** in de **sectie van de Regels van de Uitsluiting** toevoegen en de voorwaarden van de schemaverandering specificeren. Afstemming van gegevens vindt plaats via een attribuut of een join-functie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Combineren genereert een complement"
>abstract="Wisselen op **produceer complementaire** optie om de resterende bevolking in een extra overgang te verwerken."

In **combineer** activiteit, kunt u een **Uitsluiting** vormen.

![](../assets/combine-exclusion.png)

Hiervoor moet u de volgende extra stappen volgen:

1. In de **Reeksen om zich bij** sectie aan te sluiten, selecteer de **Primaire reeks** van de binnenkomende overgangen. Dit is de set waaruit elementen worden uitgesloten. De andere sets komen overeen met de elementen voordat deze worden uitgesloten van de primaire set.

1. Indien nodig, kunt u binnenkomende lijsten manipuleren. Als u een doel wilt uitsluiten van een ander schema, moet dit doel worden geretourneerd naar hetzelfde schema als het hoofddoel. Om dit te doen, klik **een regel** in de **sectie van de Regels van de Uitsluiting** toevoegen en de voorwaarden van de schemaverandering specificeren. Afstemming van gegevens vindt plaats via een attribuut of een join-functie. <!-- pas compris-->
1. U kunt **controleren produceert volledigheid** optie als u wenst om de resterende bevolking te verwerken. Zie de [ sectie van de Intersectie ](#intersection).

<!--
## Examples{#combine-examples}

In the following example, we are using a **Combine** activity and we add a **union** to retrieves all the profiles of the two queries: persons between 18 and 27 years old and persons between 34 and 40 years old.

![](../assets/workflow-union-example.png)

The following example shows the **intersection** between two query activities. It is being used here to retrieve profiles who are between 18 to 27 years old and whose email address has been provided.

![](../assets/workflow-intersection-example.png)

The following **exclusion** example shows two queries configured to filter profiles who are between 18 and 27 years old and have an Adobe email domain. The profiles with an Adobe email domain are then excluded from the first set. 

![](../assets/workflow-exclusion-example.png)
-->
