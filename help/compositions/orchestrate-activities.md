---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
source-git-commit: 4a73702c99762a5e9ab73485fa46916b9c28fcc3
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---


# Orchestrische compositieactiviteiten {#activities}

Zodra u een samenstelling hebt gecreeerd, kunt u beginnen de verschillende taken te ordenen het zal uitvoeren. Om dit te doen, wordt een visueel canvas verstrekt, toestaand u om uw samenstellingsdiagram te construeren. Binnen dit diagram, kunt u diverse activiteiten toevoegen en hen in een opeenvolgende orde verbinden.

## Activiteiten toevoegen {#add}

In dit stadium van de configuratie, wordt het diagram getoond met een beginpictogram, dat het begin van uw werkschema vertegenwoordigt. Als u uw eerste activiteit wilt toevoegen, klikt u op de knop **+** die is verbonden met het beginpictogram.

Er wordt een lijst met activiteiten weergegeven die aan het diagram kunnen worden toegevoegd. De beschikbare activiteiten hangen van uw positie binnen het samenstellingsdiagram af. Bijvoorbeeld, wanneer het toevoegen van uw eerste activiteit, kunt u uw samenstelling beginnen door een publiek te richten, het werkschemapad te verdelen, montages een planner om de werkschemauitvoering te vertragen of a **te plaatsen wacht** activiteit om de werkschemauitvoering te vertragen. Anderzijds, na a **bouwt publiek** activiteit, kunt u uw doel met het richten van activiteiten verfijnen of het samenstellingsproces met de activiteiten van de stroomcontrole organiseren.

Zodra een activiteit aan het diagram is toegevoegd, verschijnt een juiste ruit, toestaand u om de onlangs toegevoegde activiteit met specifieke montages te vormen. De gedetailleerde informatie over hoe te om elke activiteit te vormen is beschikbaar in [ deze sectie ](activities/about-activities.md).

![](assets/composition-create-add.png)

Herhaal dit proces om zoveel activiteiten toe te voegen als gewenst afhankelijk van de taken die u wilt uitvoeren uw samenstelling. U kunt ook een nieuwe activiteit invoegen tussen twee activiteiten. Om dit te doen, klik **+** knoop op de overgang tussen de activiteiten, selecteer de gewenste activiteit en vorm het in de juiste ruit.

>[!TIP]
>
>U kunt de naam van de overgangen tussen elke activiteit aanpassen. U doet dit door de overgang te selecteren en het label ervan te wijzigen in het rechterdeelvenster.

## De werkbalk Canvas {#toolbar}

De werkbalk in de rechterbovenhoek van het canvas bevat opties waarmee u de activiteiten eenvoudig kunt manipuleren en op het canvas kunt navigeren.

![](assets/canvas-toolbar.png)

Beschikbare acties zijn:

* **Veelvoudige selectie**: Selecteer veelvoudige activiteiten om hen allen in één keer te schrappen of hen te kopiëren en te kleven. Zie [deze sectie](#copy).
* **roteer**: Verdraai verticaal het canvas.
* **Passend aan het scherm**: Pas het het gezoemniveau van het canvas aan uw scherm aan.
* **Gezoem uit** / **Gezoem binnen**: Gezoem uit of in het canvas.
* **kaart van de Vertoning**: Opent een momentopname van het canvas die u toont wordt gevestigd.

## Activiteiten beheren {#manage}

Wanneer u activiteiten toevoegt, zijn er actieknoppen beschikbaar in het deelvenster Eigenschappen, zodat u meerdere bewerkingen kunt uitvoeren.

![](assets/activity-actions.png)

U kunt:

* **Schrap** de activiteit van het canvas.
* **onbruikbaar maken/laat** de activiteit toe. Wanneer de workflow wordt uitgevoerd, worden uitgeschakelde activiteiten en de volgende activiteiten op hetzelfde pad niet uitgevoerd en wordt de workflow gestopt.
* **Pauze/hervat** de activiteit. Wanneer de workflow wordt uitgevoerd, wordt de gepauzeerde activiteit gepauzeerd. De bijbehorende taak en alle taken die deze in hetzelfde pad volgen, worden niet uitgevoerd.
* **Exemplaar** de activiteit om het bij een andere plaats in de samenstelling te kleven. Klik hiertoe op de knop **+** in een overgang en selecteer &quot;X-activiteit plakken&quot;. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Vorm **opties van de Uitvoering** voor de geselecteerde activiteit. Vouw de onderstaande sectie uit voor meer informatie over de beschikbare opties.

  +++Beschikbare uitvoeringsopties

  De **sectie van Eigenschappen** staat u toe om generische montages betreffende de uitvoering van de activiteit te vormen:

   * **Uitvoering**: Bepaal de uit te voeren actie wanneer het is begonnen.
   * **Maximale uitvoeringstijd**: Specificeer een duur zoals &quot;30s&quot;of &quot;1h&quot;. Als de activiteit niet wordt gebeëindigd nadat de gespecificeerde duur is verstreken, wordt een alarm teweeggebracht. Dit heeft geen invloed op de werking van de workflow.
   * **streek van de Tijd**: Selecteer de tijdzone van de activiteit. De federatieve Samenstelling van de Auditie staat u toe om de tijdverschillen tussen veelvoudige landen op het zelfde geval te beheren. De toegepaste instelling wordt geconfigureerd wanneer de instantie wordt gemaakt.
   * **Affinity**: Dwing de samenstellingsactiviteit om op een bepaalde machine uit te voeren. Hiervoor moet u een of meer affiniteiten voor de desbetreffende activiteit opgeven.
   * **Gedrag**: Bepaal de te volgen procedure als de asynchrone taken worden gebruikt.

  Het **beheer van de Fout** sectie staat u toe om de uit te voeren actie te specificeren als de activiteit een fout ontmoet.

  De **sectie van het manuscript van de Initialisatie** laat u variabelen initialiseren of activiteiteneigenschappen wijzigen. Klik **geef code** knoop uit en typ het fragment van uit te voeren code. Het script wordt aangeroepen wanneer de activiteit wordt uitgevoerd.

+++

* Heb toegang tot de Logboeken en de taken van de activiteit ****.
