---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
exl-id: 7b9acfc0-99b6-4f83-b774-3652c811868c
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Orchestrische compositieactiviteiten {#activities}

Zodra u een samenstelling hebt gecreeerd, kunt u beginnen de verschillende taken te ordenen het zal uitvoeren. Om dit te doen, wordt een visueel canvas verstrekt, toestaand u om uw diagram van de publiekssamenstelling te construeren. Binnen dit diagram, kunt u diverse activiteiten toevoegen en hen in een opeenvolgende orde verbinden.

## Activiteiten toevoegen {#add}

In dit stadium van de configuratie, wordt het diagram getoond met een beginpictogram, dat het begin van uw samenstelling vertegenwoordigt. Als u uw eerste activiteit wilt toevoegen, klikt u op de knop **+** die is verbonden met het beginpictogram.

Er wordt een lijst met activiteiten weergegeven die aan het diagram kunnen worden toegevoegd. De beschikbare activiteiten hangen van uw positie binnen het samenstellingsdiagram af. Bijvoorbeeld, wanneer het toevoegen van uw eerste activiteit, kunt u uw samenstelling beginnen door een publiek te richten, die de samenstellingsweg, montages een planner splitsen om de samenstellingsuitvoering te vertragen of a **te plaatsen wacht** activiteit om de samenstellingsuitvoering te vertragen. Anderzijds, na a **bouwt publiek** activiteit, kunt u uw doel met het richten van activiteiten verfijnen of het samenstellingsproces met de activiteiten van de stroomcontrole organiseren.

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

* **[!UICONTROL Multiple selection]**: Selecteer meerdere activiteiten om deze allemaal tegelijk te verwijderen of kopieer en plak ze. Zie [deze sectie](#copy).
* **[!UICONTROL Rotate]**: verander het canvas verticaal.
* **[!UICONTROL Fit to screen]**: pas het zoomniveau van het canvas aan het scherm aan.
* **[!UICONTROL Zoom out]** / **[!UICONTROL Zoom in]** : Uitzoomen of op het canvas.
* **[!UICONTROL Display map]**: hiermee opent u een opname van het canvas waarop wordt aangegeven waar u zich bevindt.

## Activiteiten beheren {#manage}

Wanneer u activiteiten toevoegt, zijn er actieknoppen beschikbaar in het deelvenster Eigenschappen, zodat u meerdere bewerkingen kunt uitvoeren.

![](assets/activity-actions.png)

U kunt:

* **[!UICONTROL Delete]** de activiteit vanaf het canvas.
* **[!UICONTROL Disable]/[!UICONTROL Enable]** de activiteit. Wanneer de samenstelling wordt uitgevoerd, worden de gehandicapte activiteiten en de volgende activiteiten op de zelfde weg niet uitgevoerd en de samenstelling wordt tegengehouden.
* **[!UICONTROL Pause]/[!UICONTROL Resume]** de activiteit. Wanneer de samenstelling wordt uitgevoerd, pauzeert het bij de gepauzeerde activiteit. De bijbehorende taak en alle taken die deze in hetzelfde pad volgen, worden niet uitgevoerd.
* **[!UICONTROL Copy]** de activiteit om het op een andere plaats in de samenstelling te kleven. Klik hiertoe op de knop **+** op een overgang en selecteer **[!UICONTROL Paste X activity]** . <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configureer **[!UICONTROL Execution options]** voor de geselecteerde activiteit. Vouw de onderstaande sectie uit voor meer informatie over de beschikbare opties.

  +++Beschikbare uitvoeringsopties

  In de sectie **[!UICONTROL Properties]** kunt u algemene instellingen configureren voor de uitvoering van de activiteit:

   * **[!UICONTROL Execution]**: Definieer de handeling die moet worden uitgevoerd wanneer de handeling wordt gestart.
   * **[!UICONTROL Maximum execution duration]**: geef een duur op, bijvoorbeeld &quot;30s&quot; of &quot;1h&quot;. Als de activiteit niet wordt gebeëindigd nadat de gespecificeerde duur is verstreken, wordt een alarm teweeggebracht. Dit heeft geen invloed op de werking van de compositie.
   * **[!UICONTROL Time zone]**: selecteer de tijdzone van de activiteit. De federatieve Samenstelling van de Auditie staat u toe om de tijdverschillen tussen veelvoudige landen op het zelfde geval te beheren. De toegepaste instelling wordt geconfigureerd wanneer de instantie wordt gemaakt.
   * **[!UICONTROL Affinity]**: dwingt u de compositieactiviteit uit te voeren op een bepaalde computer. Hiervoor moet u een of meer affiniteiten voor de desbetreffende activiteit opgeven.
   * **[!UICONTROL Behavior]**: definieer de procedure die moet worden gevolgd wanneer asynchrone taken worden gebruikt.

  In de sectie **[!UICONTROL Error management]** kunt u opgeven welke actie moet worden uitgevoerd als er een fout optreedt.

  In de sectie **[!UICONTROL Initialization script]** kunt u variabelen initialiseren of eigenschappen van activiteiten wijzigen. Klik op de knop **[!UICONTROL Edit code]** en typ het codefragment dat u wilt uitvoeren. Het script wordt aangeroepen wanneer de activiteit wordt uitgevoerd.

+++

* Heb toegang tot de Logboeken en de taken van de activiteit ****.
