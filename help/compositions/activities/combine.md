---
audience: end-user
title: De combinatie-activiteit gebruiken
description: Meer informatie over het gebruik van de combinatieactiviteit
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 11%

---


# Combineren {#combine}

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Combineer activiteit"
>abstract="De **Combineren** de activiteit staat u toe om segmentatie op uw binnenkomende bevolking uit te voeren. U kunt dus meerdere populaties combineren, een deel ervan uitsluiten of gegevens alleen gemeenschappelijk houden voor meerdere doelen."

De **Combineren** de activiteit staat u toe om segmentatie op uw binnenkomende bevolking uit te voeren. U kunt dus meerdere populaties combineren, een deel ervan uitsluiten of gegevens alleen gemeenschappelijk houden voor verschillende doelen. Hier volgen de beschikbare segmentatietypen:

* De **Unie** staat u toe om het resultaat van veelvoudige activiteiten in één enkel doel te hergroeperen.
* De **Intersectie** Hiermee kunt u alleen de elementen behouden die gemeenschappelijk zijn voor de verschillende binnenkomende populaties in de activiteit.
* De **Uitsluiting** kunt u elementen op basis van bepaalde criteria uitsluiten van één populatie.

De **Combineren** activiteit kan na enige andere activiteit worden geplaatst, maar niet aan het begin van de samenstelling. Elke activiteit kan na de **Combineren**.

## De combinatieactiviteit configureren {#combine-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Samenvoegopties voor doorsnede"
>abstract="De **intersection** Hiermee kunt u alleen de elementen behouden die gemeenschappelijk zijn voor de verschillende binnenkomende populaties in de activiteit. In de **Stelt in om te verbinden** in, controleert u alle vorige activiteiten waaraan u wilt deelnemen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Samenvoegopties voor uitsluiting"
>abstract="De **uitsluiting** kunt u elementen op basis van bepaalde criteria uitsluiten van één populatie. In de **Stelt in om te verbinden** in, controleert u alle vorige activiteiten waaraan u wilt deelnemen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Selecteer het segmentatietype"
>abstract="Selecteer hoe u het publiek wilt combineren: verenigen, doorsnijden of uitsluiten."

Voer de volgende algemene stappen uit om de configuratie van de **Combineren** activiteit:

1. Voeg meerdere activiteiten toe om minstens twee verschillende uitvoeringstakken te vormen.
1. Voeg een **Combineren** activiteiten aan een van de vorige bijkantoren.
1. Selecteer het segmentatietype: [union](#union), [intersection](#intersection) of [uitsluiting](#exclusion).
1. Klikken **Doorgaan**.
1. In de **Stelt in om te verbinden** in, controleert u alle vorige activiteiten waaraan u wilt deelnemen.

## Samenvoegen {#combine-union}

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Afstemmingsopties voor doorsnede"
>abstract="Selecteer het afstemmingstype om te bepalen hoe duplicaten worden verwerkt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Afstemmingsopties"
>abstract="Selecteer de **Type afstemming** om te definiëren hoe duplicaten moeten worden verwerkt."

In de **Combineren** activiteit, kunt u vormen **Unie**. Hiervoor moet u de optie **Type afstemming** om te bepalen hoe duplicaten worden verwerkt:

* **Alleen toetsen**: dit is de standaardmodus. De activiteit behoudt slechts één element wanneer elementen van de verschillende binnenkomende overgangen dezelfde sleutel hebben. Deze optie kan alleen worden gebruikt als de binnenkomende populaties homogeen zijn.
* **Een selectie van kolommen**: selecteer deze optie om de lijst met kolommen te definiëren waarop de afstemming van gegevens wordt toegepast. U moet eerst de primaire set (de set met de brondata) selecteren en vervolgens de kolommen die u voor de samenvoeging wilt gebruiken.

## Doorsnede {#combine-intersection}

In de **Combineren** activiteit, kunt u vormen **Intersectie**. Hiervoor voert u de volgende extra stappen uit:

1. Selecteer de **Type afstemming** om te bepalen hoe duplicaten worden verwerkt. Zie de [Unie](#union) sectie.
1. U kunt de **Voltooiing genereren** als u de resterende populatie wilt verwerken. Het complement zal de samenvoeging bevatten van de resultaten van alle binnenkomende activiteiten min de doorsnede. Een extra uitgaande overgang zal dan aan de activiteit worden toegevoegd.

## Uitsluiting {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Uitsluitingsregels"
>abstract="Indien nodig, kunt u binnenkomende lijsten manipuleren. Om een doel van een andere dimensie uit te sluiten, moet dit doel worden teruggebracht naar dezelfde doeldimensie als het hoofddoel. Om dit te doen, klik **Een regel toevoegen** in de **uitsluitingsregels** en geeft u de voorwaarden voor het wijzigen van de dimensie op. Afstemming van gegevens vindt plaats via een attribuut of een join-functie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Te combineren sets selecteren"
>abstract="In de **Stelt in om te verbinden** selecteert u de **Primaire set** van de binnenkomende overgangen. Dit is de set waaruit elementen worden uitgesloten. De andere sets komen overeen met de elementen voordat deze worden uitgesloten van de primaire set."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Uitsluitingsregels"
>abstract="Indien nodig, kunt u binnenkomende lijsten manipuleren. Om een doel van een andere dimensie uit te sluiten, moet dit doel worden teruggebracht naar dezelfde doeldimensie als het hoofddoel. Om dit te doen, klik **Een regel toevoegen** in de **Uitsluitingsregels** en geeft u de voorwaarden voor het wijzigen van de dimensie op. Afstemming van gegevens vindt plaats via een attribuut of een join-functie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Combineren genereert een complement"
>abstract="In-/uitschakelen **Complement genereren** de mogelijkheid om de resterende populatie in een aanvullende overgang te verwerken."

In de **Combineren** activiteit, kunt u vormen **Uitsluiting**. Hiervoor moet u de volgende extra stappen volgen:

1. In de **Stelt in om te verbinden** selecteert u de **Primaire set** van de binnenkomende overgangen. Dit is de set waaruit elementen worden uitgesloten. De andere sets komen overeen met de elementen voordat deze worden uitgesloten van de primaire set.
1. Indien nodig, kunt u binnenkomende lijsten manipuleren. Om een doel van een andere dimensie uit te sluiten, moet dit doel worden teruggebracht naar dezelfde doeldimensie als het hoofddoel. Om dit te doen, klik **Een regel toevoegen** in de **Uitsluitingsregels** en geeft u de voorwaarden voor het wijzigen van de dimensie op. Afstemming van gegevens vindt plaats via een attribuut of een join-functie.
1. U kunt de **Voltooiing genereren** als u de resterende populatie wilt verwerken. Zie de [Intersectie](#intersection) sectie.

<!--
## Examples{#combine-examples}

In the following example, we are using a **Combine** activity and we add a **union** to retrieves all the profiles of the two queries: persons between 18 and 27 years old and persons between 34 and 40 years old.

![](../assets/workflow-union-example.png)

The following example shows the **intersection** between two query activities. It is being used here to retrieve profiles who are between 18 to 27 years old and whose email address has been provided.

![](../assets/workflow-intersection-example.png)

The following **exclusion** example shows two queries configured to filter profiles who are between 18 and 27 years old and have an Adobe email domain. The profiles with an Adobe email domain are then excluded from the first set. 

![](../assets/workflow-exclusion-example.png)
-->
