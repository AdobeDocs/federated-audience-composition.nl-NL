---
audience: end-user
title: Werken met activiteiten
description: Leer hoe u met activiteiten kunt werken
exl-id: 1e4e5f53-636f-4f1c-bf2f-cc3b5d6d6dda
source-git-commit: 2a21dcde345febdaad0934c8835df5f7ae8c30f6
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---

# Werken met activiteiten {#activities}

In Federated Audience Composition, kunt u samenstellingen tot stand brengen gebruikend twee soorten activiteiten:

* **het richten activiteiten** laat u één of meerdere doelstellingen bouwen door een publiek te bepalen en deze doelgroepen te splitsen of te combineren gebruikend doorsnede, vereniging of uitsluitingsverrichtingen.
* **de controle van de Stroom** activiteiten zijn specifiek aan het organiseren van en het uitvoeren van samenstellingen. Hun belangrijkste taak is de coördinatie van de andere activiteiten.

## Targetingactiviteiten

* [&#x200B; bouwt publieksactiviteit &#x200B;](build-audience.md): Bepaal uw doelbevolking. U kunt of een bestaand publiek selecteren of de vraagmodeler gebruiken om uw eigen vraag te bepalen.
* [&#x200B; gegevensbron van de Verandering &#x200B;](./change-data-source.md): Verander de gegevensbron die door uw samenstelling wordt gebruikt.
* [&#x200B; dimensie van de Verandering &#x200B;](change-dimension.md): Verander het schema, dat ook als het richten dimensie wordt bekend, aangezien u uw samenstelling bouwt.
* [&#x200B; combineren &#x200B;](combine.md): Voer segmentatie op uw binnenkomende bevolking uit. U kunt een samenvoeging, een doorsnede of een uitsluiting gebruiken.
* [&#x200B; Deduplicatie &#x200B;](deduplication.md): Schrap duplicaten in het resultaat(en) van de binnenkomende activiteiten.
* [&#x200B; Verrijking &#x200B;](enrichment.md): Bepaal extra gegevens om in uw samenstelling te verwerken. Met deze activiteit, kunt u hefboomwerking de binnenkomende overgang en de activiteit vormen om de outputovergang met extra gegevens te voltooien.
* [&#x200B; Verzoening &#x200B;](reconciliation.md): Bepaal het verband tussen de gegevens in het gegevensbestand en de gegevens in een het werklijst, bijvoorbeeld gegevens die van een extern dossier worden geladen.
* [&#x200B; sparen publiek &#x200B;](save-audience.md): Werk een bestaand publiek bij of creeer een nieuw publiek van de bevolking die stroomopwaarts in een samenstelling wordt berekend.
* [&#x200B; Gesplitst &#x200B;](split.md): De inkomende bevolking van het segment in verscheidene ondergroepen.

## Workflowbeheeractiviteiten

* [&#x200B; EN-sluit zich aan &#x200B;](and-join.md): Synchroniseer veelvoudige uitvoeringstakken van een samenstelling.
* **Eind**: Merk grafisch het eind van een samenstelling. Deze activiteit heeft geen functioneel effect en is daarom optioneel.
* [&#x200B; Fork &#x200B;](fork.md): Creeer uitgaande overgangen om verscheidene activiteiten tezelfdertijd te beginnen.
* [&#x200B; Planner &#x200B;](scheduler.md): Plan wanneer de samenstelling begonnen wordt.
* [&#x200B; wacht &#x200B;](wait.md): Onderbreek tijdelijk uitvoering van een deel van een samenstelling.
