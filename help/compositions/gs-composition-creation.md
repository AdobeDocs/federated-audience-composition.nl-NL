---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# Belangrijkste beginselen voor het creëren van compositie {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Compositie-eigenschappen"
>abstract="Kies in dit scherm de sjabloon die u wilt gebruiken om de compositie te maken en geef een label op. Vouw de sectie EXTRA OPTIONS uit om meer instellingen te configureren, zoals de interne naam van de compositie, de map, de tijdzone en de supervisorgroep. Het wordt hoogst geadviseerd om een supervisorgroep te selecteren zodat de exploitanten worden gealarmeerd als een fout voorkomt."

De Federale Samenstelling van Gegevens verstrekt een visueel canvas dat u toestaat om publiek tot stand te brengen door diverse activiteiten (gespleten, verrijkt, etc.) te gebruiken.

## Wat zit er in een compositie? {#gs-composition-inside}

Het compositiediagram is een weergave van wat er moet gebeuren. Hierin worden de verschillende taken beschreven die moeten worden uitgevoerd en hoe deze aan elkaar zijn gekoppeld.

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

Elke compositie bevat:

* **Activiteiten**: Een activiteit is een uit te voeren taak. De verschillende activiteiten worden op het diagram weergegeven door pictogrammen. Elke activiteit heeft specifieke eigenschappen en andere eigenschappen die voor alle activiteiten gemeenschappelijk zijn.

  In een samenstellingsdiagram, kan een bepaalde activiteit veelvoudige taken veroorzaken, in het bijzonder wanneer er een lijn of terugkomende acties is.

* **Overgangen**: Overgangen koppelen een bronactiviteit aan een doelactiviteit en definiëren hun volgorde.

* **Worktables**: De werktabel bevat alle informatie die door de overgang wordt overgedragen. Elke samenstelling gebruikt verscheidene werklijsten. De gegevens die in deze lijsten worden overgebracht kunnen gedurende de het levenscyclus van de samenstelling worden gebruikt.

## Belangrijke stappen om een compositie te maken {#gs-composition-steps}

De belangrijkste stappen om een samenstelling tot stand te brengen zijn als volgt:

1. [De compositie maken](#create)
1. [Vorm de montages van de samenstelling](#starting-audience)
1. [Activiteiten toevoegen en configureren](#action-activities)
1. [De compositie uitvoeren en de uitvoering ervan controleren](#save)
