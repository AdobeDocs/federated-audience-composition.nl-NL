---
audience: end-user
title: Werken met activiteiten
description: Leer hoe u met activiteiten kunt werken
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---


# Werken met activiteiten {#activities}

In Federated Audience Composition, kunt u samenstellingen tot stand brengen gebruikend twee soorten activiteiten:

* **Gerichte activiteiten** Hiermee kunt u een of meer doelen maken door een publiek te definiëren en deze doelgroepen te splitsen of te combineren met behulp van doorsnede-, samenvoegings- of uitsluitingsacties.
* **Stroomregeling** de activiteiten zijn specifiek gericht op het organiseren en uitvoeren van composities. Hun belangrijkste taak is de coördinatie van de andere activiteiten.

## Gerichte activiteiten

* [Activiteit voor publiek opbouwen](build-audience.md): Definieer de doelpopulatie. U kunt of een bestaand publiek selecteren of de vraagmodeler gebruiken om uw eigen vraag te bepalen.
* [Dimensie wijzigen](change-dimension.md): Wijzig het schema, ook wel afmeting aanwijzen genoemd, terwijl u uw compositie samenstelt.
* [Combineren](combine.md): Voer segmentatie op uw binnenkomende bevolking uit. U kunt een samenvoeging, een doorsnede of een uitsluiting gebruiken.
* [Deduplicatie](deduplication.md): Verwijder duplicaten van de resultaten van de binnenkomende activiteiten.
* [Verrijking](enrichment.md): Definieer aanvullende gegevens die in uw compositie moeten worden verwerkt. Met deze activiteit, kunt u hefboomwerking de binnenkomende overgang en de activiteit vormen om de outputovergang met extra gegevens te voltooien.
* [Verzoening](reconciliation.md): Definieer de koppeling tussen de gegevens in de database en de gegevens in een werktabel, bijvoorbeeld gegevens die uit een extern bestand zijn geladen.
* [Adviezen opslaan](save-audience.md): Werk een bestaand publiek bij of maak een nieuw publiek van de populatie die stroomopwaarts in een samenstelling wordt berekend.
* [Splitsen](split.md): Segmenteer de binnenkomende populatie in verschillende subsets.

## Stroombeheeractiviteiten

* [AND-join](and-join.md): Meerdere uitvoeringstakken van een workflow synchroniseren.
* **Einde** : Geeft grafisch het einde van een workflow aan. Deze activiteit heeft geen functioneel effect en is daarom optioneel.
* [Vork](fork.md): Maak uitgaande overgangen om meerdere activiteiten tegelijk te starten.
* [Planner](scheduler.md): Plan wanneer de workflow wordt gestart.
* [Wachten](wait.md): Onderbreek tijdelijk de uitvoering van een deel van een workflow.
