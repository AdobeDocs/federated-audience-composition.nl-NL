---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
source-git-commit: 4b5173a2a0549d6535bccd07c94e521ecde8330b
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 1%

---


# Orchestrische compositieactiviteiten {#activities}

Zodra u een samenstelling hebt gecreeerd, kunt u beginnen de verschillende taken te ordenen het zal uitvoeren. Om dit te doen, wordt een visueel canvas verstrekt, toestaand u om uw samenstellingsdiagram te construeren. Binnen dit diagram, kunt u diverse activiteiten toevoegen en hen in een opeenvolgende orde verbinden.

## Activiteiten toevoegen {#add}

In dit stadium van de configuratie, wordt het diagram getoond met een beginpictogram, dat het begin van uw werkschema vertegenwoordigt. Als u uw eerste activiteit wilt toevoegen, klikt u op de knop **+** die is verbonden met het startpictogram.

Er wordt een lijst met activiteiten weergegeven die aan het diagram kunnen worden toegevoegd. De beschikbare activiteiten hangen van uw positie binnen het samenstellingsdiagram af. Wanneer u bijvoorbeeld uw eerste activiteit toevoegt, kunt u uw compositie starten door zich te richten op een publiek, het workflowpad te splitsen of een **Wachten** activiteit om de uitvoering van de workflow uit te stellen. Aan de andere kant **publiek opbouwen** activiteit, kunt u uw doel met het richten van activiteiten verfijnen, een levering naar uw publiek met kanaalactiviteiten verzenden, of het samenstellingsproces met debietcontroleactiviteiten organiseren.

Zodra een activiteit aan het diagram is toegevoegd, verschijnt een juiste ruit, toestaand u om de onlangs toegevoegde activiteit met specifieke montages te vormen. Gedetailleerde informatie over hoe te om elke activiteit te vormen is beschikbaar in [deze sectie](activities/about-activities.md).

Herhaal dit proces om zoveel activiteiten toe te voegen als gewenst afhankelijk van de taken die u wilt uitvoeren uw samenstelling. U kunt ook een nieuwe activiteit invoegen tussen twee activiteiten. Om dit te doen, klik **+** op de overgang tussen de activiteiten, selecteer de gewenste activiteit en vorm het in de juiste ruit.

Als u een activiteit wilt verwijderen, selecteert u deze op het canvas en klikt u op de knop **Verwijderen** in de eigenschappen activity.

>[!TIP]
>
>U kunt de naam van de overgangen tussen elke activiteit aanpassen. U doet dit door de overgang te selecteren en het label ervan te wijzigen in het rechterdeelvenster.

## De werkbalk {#toolbar}

De werkbalk in de rechterbovenhoek van het canvas bevat opties waarmee u de activiteiten eenvoudig kunt manipuleren en op het canvas kunt navigeren:

* **Meerdere selectiemodus**: Selecteer meerdere activiteiten om deze allemaal tegelijk te verwijderen of kopieer en plak ze. Zie [deze sectie](#copy).
* **Roteren**: Verander het canvas verticaal.
* **Aanpassen aan scherm**: Pas het zoomniveau van het canvas aan op het scherm.
* **Uitzoomen** / **Inzoomen**: Uitzoomen of op het canvas.
* **Kaart weergeven**: Hiermee opent u een opname van het canvas waarop u uw locatie ziet.


## Activiteiten beheren {#manage}

Wanneer u activiteiten toevoegt, zijn er actieknoppen beschikbaar in het deelvenster Eigenschappen, zodat u meerdere bewerkingen kunt uitvoeren. U kunt:

* **Verwijderen** de activiteit van het canvas.
* **Uitschakelen/inschakelen** de activiteit. Wanneer de workflow wordt uitgevoerd, worden uitgeschakelde activiteiten en de volgende activiteiten op hetzelfde pad niet uitgevoerd en wordt de workflow gestopt.
* **Kopiëren** de activiteit. Zie [deze sectie](#copy).
* Toegang krijgen tot de activiteiten **Logboeken en taken**.
* **Pauzeren/hervatten** de activiteit. Wanneer de workflow wordt uitgevoerd, wordt de gepauzeerde activiteit gepauzeerd. De bijbehorende taak en alle taken die deze in hetzelfde pad volgen, worden niet uitgevoerd.

Meerdere **Targeting** activiteiten, zoals **Combineren** of **Deduplicatie**, kunt u de resterende populatie verwerken en opnemen in een extra uitgaande overgang. Als u bijvoorbeeld een **Splitsen** de activiteit, bestaat het complement uit de populatie die niet overeenkwam met een van de eerder gedefinieerde subgroepen. Als u deze functie wilt gebruiken, activeert u de **Complement genereren** -optie.

## Activiteiten kopiëren {#copy}

U kunt workflowactiviteiten kopiëren en deze in elke werkstroom plakken. De doelworkflow kan zich op een ander browsertabblad bevinden.

Voor het kopiëren van activiteiten hebt u twee mogelijkheden:

* Kopieer één activiteit gebruikend de actieknoop.

* Kopieer meerdere activiteiten met de werkbalkknop.

Als u de gekopieerde activiteiten wilt plakken, klikt u op de knop **+** en selecteer &quot;X-activiteit plakken&quot;.

## Execution options {#execution}

Met alle activiteiten kunt u de uitvoeropties ervan beheren. Selecteer een activiteit en klik op **Uitvoeropties** knop. Hiermee kunt u de uitvoeringsmodus en het gedrag van de activiteit definiëren in het geval van fouten.

### Properties

De **Uitvoering** in het veld kunt u de actie definiëren die moet worden uitgevoerd wanneer de taak wordt gestart.

De **Maximale uitvoeringstermijn** kunt u een duur opgeven, bijvoorbeeld &#39;&#39;30s&#39;&#39; of &#39;&#39;1h&#39;&#39;. Als de activiteit niet wordt gebeëindigd nadat de gespecificeerde duur is verstreken, wordt een alarm teweeggebracht. Dit heeft geen invloed op de werking van de workflow.

De **Tijdzone** kunt u de tijdzone van de activiteit selecteren. Met Adobe Campaign kunt u de tijdsverschillen tussen meerdere landen op hetzelfde moment beheren. De toegepaste instelling wordt geconfigureerd wanneer de instantie wordt gemaakt.

**De affiniteit** in het veld kunt u een workflow of een werkstroomactiviteit op een bepaalde computer uitvoeren. Hiervoor moet u een of meer affiniteiten opgeven voor de workflow of activiteit in kwestie.

De **Gedrag** kunt u in het veld de procedure definiëren die moet worden gevolgd wanneer asynchrone taken worden gebruikt.

### Foutbeheer

De **In geval van fout** in dit veld kunt u opgeven welke actie moet worden uitgevoerd als er een fout optreedt.

### Initialisatiescript

De **Initialisatiescript** Hiermee kunt u variabelen initialiseren of activiteitseigenschappen wijzigen. Klik op de knop **Code bewerken** en typ het uit te voeren codefragment. Het script wordt aangeroepen wanneer de activiteit wordt uitgevoerd. Zie de sectie over [gebeurtenisvariabelen](../workflows/event-variables.md).

## Voorbeeld {#example}

Hier volgt een voorbeeld van een workflow die is ontworpen om een e-mail naar alle klanten (andere dan VIP klanten) te sturen met een e-mail die geïnteresseerd is in koffiecomputers.

Hiervoor zijn de volgende activiteiten toegevoegd:

* A **[!UICONTROL Fork]** activiteit die de werkstroom in drie wegen (één voor elke reeks klant) verdeelt;
* **[!UICONTROL Build audience]** activiteiten om de drie categorieën klanten te bereiken:

   * Klanten met een e-mail,
   * Klanten die behoren tot het reeds bestaande publiek &quot;Interrested in Coffee Machine(s)&quot;,
   * Klanten die tot het reeds bestaande &quot;VIP of beloning&quot; publiek behoren.

* A **[!UICONTROL Combine]** activiteiten die klanten met een e-mail en degenen die geïnteresseerd zijn in koffiemachines verenigen;
* A **[!UICONTROL Combine]** activiteiten die VIP klanten uitsluiten;
* An **[!UICONTROL Email delivery]** activiteit die een e-mail naar de resulterende klanten verzendt.

Nadat u de workflow hebt voltooid, voegt u **[!UICONTROL End]** activiteit aan het einde van het diagram. Met deze activiteit kunt u visueel het einde van een werkstroom markeren en heeft deze geen invloed op de functionaliteit.

Nadat u het werkstroomdiagram hebt ontworpen, kunt u de werkstroom uitvoeren en de voortgang van de verschillende taken volgen. [Leer hoe u een workflow kunt starten en de uitvoering ervan kunt controleren](start-monitor-workflows.md)
