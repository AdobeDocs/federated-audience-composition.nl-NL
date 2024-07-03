---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---


# Uw compositie starten en controleren {#start-monitor}

Nadat u de compositie hebt gemaakt en de taken hebt ontworpen die u op het canvas wilt uitvoeren, kunt u deze starten en controleren hoe deze wordt uitgevoerd.

## De compositie starten {#start}

Als u de compositie wilt starten, navigeert u naar de **[!UICONTROL Compositions]** menu of de bijbehorende campagne en klik op **[!UICONTROL Start]** in de rechterbovenhoek van het canvas

Zodra de samenstelling loopt, wordt elke activiteit in het canvas uitgevoerd in een opeenvolgende orde, tot het eind van de samenstelling wordt bereikt.

U kunt de voortgang van doelprofielen in real time volgen gebruikend een visuele stroom. Hierdoor kunt u snel de status van elke activiteit en het aantal profielen identificeren dat tussen de activiteiten overgaat.

![](assets/composition-execution.png){zoomable="yes"}

## Compositieovergangen {#transitions}

In samenstellingen worden gegevens die van de ene activiteit naar de andere worden vervoerd via overgangen opgeslagen in een tijdelijke werktabel. Deze gegevens kunnen voor elke overgang worden weergegeven. Selecteer hiertoe een overgang om de eigenschappen ervan in de rechterkant van het scherm te openen.

* Klikken **[!UICONTROL Preview schema]** om het schema van de het werklijst te tonen.
* Klikken **[!UICONTROL Preview results]** om de gegevens te visualiseren die in de geselecteerde overgang worden vervoerd.

![](assets/transition.png){zoomable="yes"}

## Activiteitenuitvoering controleren {#activities}

De visuele indicatoren in de hoger-juiste hoek van elke activiteitendoos staan u toe om hun uitvoering te controleren:

| Visuele indicator | Beschrijving |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | De activiteit wordt momenteel uitgevoerd. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | De activiteit vereist uw aandacht. Dit kan inhouden dat de verzending van een levering wordt bevestigd of dat de nodige actie wordt ondernomen. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Er is een fout opgetreden in de activiteit. Om de kwestie op te lossen, open samenstellingslogboeken voor meer informatie. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | De activiteit is met succes uitgevoerd. |

## Logboeken en taken controleren {#logs-tasks}

Het controleren van samenstellingenlogboeken en taken is een zeer belangrijke stap om uw samenstellingen te analyseren en ervoor te zorgen zij behoorlijk lopen. Ze zijn toegankelijk vanuit de **[!UICONTROL Logs]** pictogram dat beschikbaar is in de actiewerkbalk en in het eigenschappenvenster van elke activiteit.

De **[!UICONTROL Logs and tasks]** biedt een geschiedenis van de uitvoering van de compositie, waarbij alle handelingen van de gebruiker worden opgenomen en fouten worden aangetroffen. Deze geschiedenis wordt opgeslagen voor de duur die is opgegeven in de compositie [uitvoeringsopties](composition-settings.md). Tijdens deze duur, worden alle berichten bewaard, zelfs na een nieuw begin van de samenstelling. Als u de berichten uit een vorige uitvoering niet wilt opslaan, klikt u op de knop **[!UICONTROL Purge history]** knop.

![](assets/composition-logs.png){zoomable="yes"}

Er zijn twee soorten informatie beschikbaar:

* De **[!UICONTROL Log]** bevat de uitvoeringsgeschiedenis van alle compositieactiviteiten. De uitgevoerde bewerkingen en uitvoeringsfouten worden chronologisch geïndexeerd.
* De **[!UICONTROL Tasks]** tabblad bevat informatie over de volgorde van uitvoering van de activiteiten.

Op beide tabbladen kunt u de weergegeven kolommen en hun volgorde kiezen, filters toepassen en het zoekveld gebruiken om snel de gewenste informatie te zoeken.

## Opdrachten voor het uitvoeren van composities {#execution-commands}

De actiebalk in de rechterbovenhoek biedt opdrachten waarmee u de uitvoering van de compositie kunt beheren. U kunt:

* **[!UICONTROL Start]** / **[!UICONTROL Resume]** de uitvoering van de compositie, die dan de status In uitvoering krijgt. Als de samenstelling is gepauzeerd, wordt zij hervat, anders wordt zij gestart en worden de initiële activiteiten geactiveerd.

* **[!UICONTROL Pause]** de uitvoering van de samenstelling, die dan de pauzestatus krijgt. Er zullen geen nieuwe activiteiten worden geactiveerd totdat de activiteiten worden hervat, maar de lopende activiteiten worden niet opgeschort.

* **[!UICONTROL Stop]** een compositie die wordt uitgevoerd, die dan de voltooide status zal nemen. De lopende bewerkingen worden indien mogelijk onderbroken. U kunt de compositie niet hervatten vanaf dezelfde plaats als waar deze is gestopt.
