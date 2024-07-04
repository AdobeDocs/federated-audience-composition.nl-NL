---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
source-git-commit: 4a73702c99762a5e9ab73485fa46916b9c28fcc3
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Uw compositie starten en controleren {#start-monitor}

Nadat u de compositie hebt gemaakt en de taken hebt ontworpen die u op het canvas wilt uitvoeren, kunt u deze starten en controleren hoe deze wordt uitgevoerd.

## De compositie starten {#start}

Als u een compositie wilt starten, klikt u op de knop **[!UICONTROL Start]** rechtsboven in het scherm. Wanneer de samenstelling loopt, wordt elke activiteit in het canvas uitgevoerd in een opeenvolgende orde, tot het eind van de samenstelling wordt bereikt.

U kunt de voortgang van doelprofielen in real time volgen gebruikend een visuele stroom. Hierdoor kunt u snel de status van elke activiteit en het aantal profielen identificeren dat tussen de activiteiten overgaat.

![](assets/composition-visual-flow.png)

## Compositieovergangen {#transitions}

In samenstellingen worden gegevens die van de ene activiteit naar de andere worden vervoerd via overgangen opgeslagen in een tijdelijke werktabel. Deze gegevens kunnen voor elke overgang worden weergegeven. Selecteer hiertoe een overgang om de eigenschappen ervan in de rechterkant van het scherm te openen.

* Klikken **[!UICONTROL Preview schema]** om het schema van de het werklijst te tonen.
* Klikken **[!UICONTROL Preview results]** om de gegevens te visualiseren die in de geselecteerde overgang worden vervoerd.

![](assets/transition-preview.png)

## Activiteitenuitvoering controleren {#activities}

De visuele indicatoren in de hoger-juiste hoek van elke activiteitendoos staan u toe om hun uitvoering te controleren:

| Visuele indicator | Beschrijving |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | De activiteit wordt momenteel uitgevoerd. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | De activiteit vereist uw aandacht. Dit kan inhouden dat de verzending van een levering wordt bevestigd of dat de nodige actie wordt ondernomen. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Er is een fout opgetreden in de activiteit. Om de kwestie op te lossen, open samenstellingslogboeken voor meer informatie. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | De activiteit is met succes uitgevoerd. |

## Logboeken en taken controleren {#logs-tasks}

Het controleren van samenstellingenlogboeken en taken is een zeer belangrijke stap om uw samenstellingen te analyseren en ervoor te zorgen zij behoorlijk lopen. Ze zijn toegankelijk vanuit de **[!UICONTROL Logs]** Deze knop is beschikbaar in de werkbalk Handeling en in het deelvenster Eigenschappen van elke activiteit.

![](assets/logs-button.png)

De **[!UICONTROL Composition logs and tasks]** het scherm verstrekt een geschiedenis van de samenstellingsuitvoering, registrerend alle gebruikersacties en ondervonden fouten.

<!-- à confirmer, pas trouvé dans les options = The workflow history is saved for the duration specified in the workflow execution options. During this duration, all the messages are therefore saved, even after a restart. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the ![](assets/delete_darkgrey-24px.png) button.-->

De historie wordt ingedeeld in verschillende tabbladen, die hieronder worden beschreven:

* De **[!UICONTROL Log]** bevat de uitvoeringsgeschiedenis van alle compositieactiviteiten. De uitgevoerde bewerkingen en uitvoeringsfouten worden chronologisch geïndexeerd.
* De **[!UICONTROL Tasks]** tabblad bevat informatie over de volgorde van uitvoering van de activiteiten. Met de knop aan het einde van elke taak kunt u de gebeurtenisvariabelen weergeven die door de activiteit worden doorgegeven.
* De **[!UICONTROL Variables]** worden alle variabelen weergegeven die in de compositie worden doorgegeven. Het is beschikbaar wanneer het toegang tot van de logboeken en de taken van het samenstellingscanvas slechts. Het is nu beschikbaar wanneer u de logboeken opent vanuit het deelvenster met eigenschappen van een activiteit.  <!-- à confirmer-->

![](assets/logs-tasks.png)

Op alle tabbladen kunt u de weergegeven kolommen en hun volgorde kiezen, filters toepassen en het zoekveld gebruiken om snel de gewenste informatie te zoeken.

## Opdrachten voor het uitvoeren van composities {#execution-commands}

De actiebalk in de rechterbovenhoek biedt opdrachten waarmee u de uitvoering van de compositie kunt beheren.

![](assets/execution-actions.png)

Beschikbare acties zijn:

* **Start**: Start de uitvoering van de compositie, die vervolgens het **In uitvoering** status. De samenstelling is begonnen en de eerste activiteiten worden geactiveerd.

* **[!UICONTROL Resume]**: Hiermee hervat u de uitvoering van de compositie die was gepauzeerd. De samenstelling neemt de **In uitvoering** status.

* **[!UICONTROL Pause]** de uitvoering van de samenstelling, die vervolgens de **Gepauzeerd** status. Er zullen geen nieuwe activiteiten worden geactiveerd totdat de activiteiten worden hervat, maar de lopende activiteiten worden niet opgeschort.

* **[!UICONTROL Stop]** een samenstelling die wordt uitgevoerd, die dan de **Voltooid** status. De lopende bewerkingen worden indien mogelijk onderbroken. U kunt de compositie niet hervatten vanaf dezelfde plaats als waar deze is gestopt.

* **Opnieuw starten**: Stopt en start vervolgens een compositie opnieuw. In de meeste gevallen kunt u de toepassing sneller opnieuw starten, omdat het stoppen enige tijd in beslag neemt en de instelling **Start** Deze knop is alleen beschikbaar wanneer de stop effectief is.
