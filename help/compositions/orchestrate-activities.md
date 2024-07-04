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

In dit stadium van de configuratie, wordt het diagram getoond met een beginpictogram, dat het begin van uw werkschema vertegenwoordigt. Als u uw eerste activiteit wilt toevoegen, klikt u op de knop **+** die is verbonden met het startpictogram.

Er wordt een lijst met activiteiten weergegeven die aan het diagram kunnen worden toegevoegd. De beschikbare activiteiten hangen van uw positie binnen het samenstellingsdiagram af. Wanneer u bijvoorbeeld uw eerste activiteit toevoegt, kunt u uw compositie starten door zich te richten op een publiek, het workflowpad te splitsen, een planner te installeren om de uitvoering van de workflow te vertragen of een **Wachten** activiteit om de uitvoering van de workflow uit te stellen. Aan de andere kant **publiek opbouwen** activiteit, kunt u uw doel met het richten van activiteiten verfijnen of het samenstellingsproces met debietcontroleactiviteiten organiseren.

Zodra een activiteit aan het diagram is toegevoegd, verschijnt een juiste ruit, toestaand u om de onlangs toegevoegde activiteit met specifieke montages te vormen. Gedetailleerde informatie over hoe te om elke activiteit te vormen is beschikbaar in [deze sectie](activities/about-activities.md).

![](assets/composition-create-add.png)

Herhaal dit proces om zoveel activiteiten toe te voegen als gewenst afhankelijk van de taken die u wilt uitvoeren uw samenstelling. U kunt ook een nieuwe activiteit invoegen tussen twee activiteiten. Om dit te doen, klik **+** op de overgang tussen de activiteiten, selecteer de gewenste activiteit en vorm het in de juiste ruit.

>[!TIP]
>
>U kunt de naam van de overgangen tussen elke activiteit aanpassen. U doet dit door de overgang te selecteren en het label ervan te wijzigen in het rechterdeelvenster.

## De werkbalk Canvas {#toolbar}

De werkbalk in de rechterbovenhoek van het canvas bevat opties waarmee u de activiteiten eenvoudig kunt manipuleren en op het canvas kunt navigeren.

![](assets/canvas-toolbar.png)

Beschikbare acties zijn:

* **Meerdere selecties**: Selecteer meerdere activiteiten om deze allemaal tegelijk te verwijderen of kopieer en plak ze. Zie [deze sectie](#copy).
* **Roteren**: Verander het canvas verticaal.
* **Aanpassen aan scherm**: Pas het zoomniveau van het canvas aan op het scherm.
* **Uitzoomen** / **Inzoomen**: Uitzoomen of op het canvas.
* **Kaart weergeven**: Hiermee opent u een opname van het canvas waarop u uw locatie ziet.

## Activiteiten beheren {#manage}

Wanneer u activiteiten toevoegt, zijn er actieknoppen beschikbaar in het deelvenster Eigenschappen, zodat u meerdere bewerkingen kunt uitvoeren.

![](assets/activity-actions.png)

U kunt:

* **Verwijderen** de activiteit van het canvas.
* **Uitschakelen/inschakelen** de activiteit. Wanneer de workflow wordt uitgevoerd, worden uitgeschakelde activiteiten en de volgende activiteiten op hetzelfde pad niet uitgevoerd en wordt de workflow gestopt.
* **Pauzeren/hervatten** de activiteit. Wanneer de workflow wordt uitgevoerd, wordt de gepauzeerde activiteit gepauzeerd. De bijbehorende taak en alle taken die deze in hetzelfde pad volgen, worden niet uitgevoerd.
* **Kopiëren** de activiteit om het op een andere plaats in de samenstelling te kleven. Om dit te doen, klik **+** en selecteer &quot;X-activiteit plakken&quot;. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configureren **Uitvoeropties** voor de geselecteerde activiteit. Vouw de onderstaande sectie uit voor meer informatie over de beschikbare opties.

  +++Beschikbare uitvoeringsopties

  De **Eigenschappen** sectie staat u toe om generische montages betreffende de uitvoering van de activiteit te vormen:

   * **Uitvoering**: Definieer de handeling die moet worden uitgevoerd wanneer de handeling wordt gestart.
   * **Maximale uitvoeringstermijn**: Geef een duur op, bijvoorbeeld &quot;30s&quot; of &quot;1h&quot;. Als de activiteit niet wordt gebeëindigd nadat de gespecificeerde duur is verstreken, wordt een alarm teweeggebracht. Dit heeft geen invloed op de werking van de workflow.
   * **Tijdzone**: Selecteer de tijdzone van de activiteit. De federatieve Samenstelling van de Auditie staat u toe om de tijdverschillen tussen veelvoudige landen op het zelfde geval te beheren. De toegepaste instelling wordt geconfigureerd wanneer de instantie wordt gemaakt.
   * **Affiniteit**: De compositieactiviteit forceren om op een bepaalde machine uit te voeren. Hiervoor moet u een of meer affiniteiten voor de desbetreffende activiteit opgeven.
   * **Gedrag**: Definieer de procedure die moet worden gevolgd wanneer asynchrone taken worden gebruikt.

  De **Foutbeheer** kunt u opgeven welke actie moet worden uitgevoerd als er een fout optreedt.

  De **Initialisatiescript** in deze sectie kunt u variabelen initialiseren of activiteitseigenschappen wijzigen. Klik op de knop **Code bewerken** en typ het uit te voeren codefragment. Het script wordt aangeroepen wanneer de activiteit wordt uitgevoerd.

+++

* Toegang krijgen tot de activiteiten **Logboeken en taken**.
