---
audience: end-user
title: De planningsactiviteit gebruiken
description: Leer hoe u de planningsactiviteit gebruikt
source-git-commit: 4dca96ae81d1f70c8f20509fdbd9ec31e05c01dc
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 8%

---


# Planner {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Planningsactiviteit"
>abstract="De **Planner** Met deze activiteit kunt u plannen wanneer de workflow wordt gestart. Deze activiteit moet worden beschouwd als een geplande start. Deze kan alleen worden gebruikt als de eerste activiteit van de workflow."

De **Planner** activiteit is **Stroomregeling** activiteit. Het staat u toe om te plannen wanneer de samenstelling wordt begonnen. Deze activiteit moet worden beschouwd als een geplande start. Het kan slechts als eerste activiteit van de samenstelling worden gebruikt.

## De planningsactiviteit configureren {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Geldigheid van planner"
>abstract="U kunt een geldigheidsperiode voor de planner bepalen. Deze kan permanent zijn (standaard) of geldig zijn tot een bepaalde datum."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Planningsopties"
>abstract="Bepaal de frequentie van de planner. Het kan op een specifiek moment, één keer of verscheidene keren per dag, week of maand worden uitgevoerd."

Voer de volgende stappen uit om de **Planner** activiteit:

1. Voeg een **Planner** activiteit aan uw werkschema.

1. Vorm **Uitvoerfrequentie**:

   * **Eenmaal**: de compositie wordt één keer uitgevoerd.

   * **Dagelijks**: de compositie wordt op een specifiek tijdstip, eenmaal per dag, uitgevoerd.

   * **Meerdere keren per dag:** de samenstelling wordt regelmatig verscheidene keren per dag uitgevoerd. U kunt uitvoeringen instellen op specifieke tijdstippen of periodiek.

     >[!NOTE]
     >
     >Plan geen samenstelling om meer dan om de 15 minuten in werking te stellen aangezien het algemene systeemprestaties kan belemmeren en tot blokken in het gegevensbestand kan leiden.

   * **Wekelijks**: de samenstelling wordt uitgevoerd op een bepaald moment, één keer of meerdere keren per week.

   * **Maandelijks**: de compositie wordt uitgevoerd op een bepaald moment, één keer of meerdere keren per maand. U kunt maanden selecteren wanneer u de compositie nodig hebt die moet worden uitgevoerd. U kunt uitvoeringen ook instellen op bepaalde weekdagen van de maand, zoals de tweede dinsdag van de maand.

1. Definieer de details van de uitvoering op basis van de geselecteerde frequentie. De detailvelden variëren, afhankelijk van de gebruikte frequentie (tijd, herhalingsfrequentie, opgegeven dagen, enz.).

1. Klikken **Voorvertoning van opstartij** om het programma van de volgende tien uitvoeringen van uw samenstelling te controleren.

1. Bepaal de geldigheidsperiode van de planner:

   * **Permanent (nooit verlopen)**: de compositie wordt uitgevoerd volgens de opgegeven frequentie, zonder enige beperking van het tijdkader of het aantal herhalingen.

   * **Geldigheidsperiode**: de samenstelling wordt uitgevoerd volgens de gespecificeerde frequentie, tot een specifieke datum. U moet begin- en einddatums opgeven.

>[!NOTE]
>
>Als u de compositie meteen wilt starten, klikt u op de knop **Taak in behandeling uitvoeren** in de hoogste actiebar van de planner. Deze knoop is slechts beschikbaar wanneer u de samenstelling bent begonnen.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->

