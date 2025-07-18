---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
exl-id: 861440ab-ce14-46aa-a215-b86fc9ffeef0
source-git-commit: b73eba776e3e75f3ff7107bcf48f7b2f60048d08
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Belangrijkste beginselen voor het creëren van compositie {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Compositie-eigenschappen"
>abstract="Kies in dit scherm de sjabloon die u wilt gebruiken om de compositie te maken en geef een label op. Vouw de sectie ADDITIONAL OPTIONS uit om meer instellingen te configureren, zoals de interne naam van de compositie, de map, de tijdzone en de supervisorgroep. Het wordt hoogst geadviseerd om een supervisorgroep te selecteren zodat de exploitanten worden gealarmeerd als een fout voorkomt."

## Wat zit er in een compositie {#gs-composition-inside}

Experience Platform Federated Audience Composition biedt een visueel canvas dat u in staat stelt een publiek te maken door gebruik te maken van verschillende activiteiten (splitsen, verrijken, enz.).

Het compositiediagram is een weergave van wat er moet gebeuren. Hierin worden de verschillende taken beschreven die moeten worden uitgevoerd en hoe deze aan elkaar zijn gekoppeld.

![](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

Elke compositie bevat:

* **[!UICONTROL Activities]**: Een activiteit is een taak die moet worden uitgevoerd. De verschillende activiteiten worden op het diagram weergegeven door pictogrammen. Elke activiteit heeft specifieke eigenschappen en andere eigenschappen die voor alle activiteiten gemeenschappelijk zijn.
* **[!UICONTROL Transitions]**: Overgangen koppelen een bronactiviteit aan een doelactiviteit en definiëren hun volgorde.
* **[!UICONTROL Worktables]**: De werktabel bevat alle gegevens die door de overgang worden overgedragen. Elke samenstelling gebruikt verscheidene werklijsten. De gegevens die in deze lijsten worden overgebracht kunnen gedurende de het levenscyclus van de samenstelling worden gebruikt.

## Belangrijke stappen om een compositie te maken {#gs-composition-steps}

De belangrijkste stappen om een samenstelling tot stand te brengen zijn als volgt:

1. [Creeer en vorm de samenstelling](../compositions/create-composition.md)
1. [Orchestraten](../compositions/orchestrate-activities.md)
1. [De compositie uitvoeren en de uitvoering ervan controleren](../compositions/start-monitor-composition.md)
