---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
exl-id: 1f288312-dd6a-4a62-8ee6-fa2417954d5c
source-git-commit: e0bf1f76f7f781fb6fcc3b44898ba805d87a25c9
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Uw compositie starten en controleren {#start-monitor}

Nadat u de compositie hebt gemaakt en de taken hebt ontworpen die u op het canvas wilt uitvoeren, kunt u deze starten en controleren hoe deze wordt uitgevoerd.

## De compositie starten {#start}

Als u een compositie wilt starten, klikt u op de knop **[!UICONTROL Start]** in de rechterbovenhoek van het scherm. Wanneer de samenstelling loopt, wordt elke activiteit in het canvas uitgevoerd in een opeenvolgende orde, tot het eind van de samenstelling wordt bereikt.

U kunt de voortgang van doelprofielen in real time volgen gebruikend een visuele stroom. Hierdoor kunt u snel de status van elke activiteit en het aantal profielen identificeren dat tussen de activiteiten overgaat.

![](assets/composition-visual-flow.png)

## Compositieovergangen {#transitions}

In samenstellingen worden gegevens die van de ene activiteit naar de andere worden vervoerd via overgangen opgeslagen in een tijdelijke werktabel. Deze gegevens kunnen voor elke overgang worden weergegeven. Selecteer hiertoe een overgang om de eigenschappen ervan in de rechterkant van het scherm te openen.

* Klik op **[!UICONTROL Preview schema]** om het schema van de werktabel weer te geven.
* Klik op **[!UICONTROL Preview results]** om de gegevens te visualiseren die in de geselecteerde overgang worden verzonden. Deze optie is alleen beschikbaar als de optie **[!UICONTROL Keep the result of interim populations between two executions]** is ingeschakeld. [Meer informatie](create-composition.md#settings).

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

Het controleren van samenstellingenlogboeken en taken is een zeer belangrijke stap om uw samenstellingen te analyseren en ervoor te zorgen zij behoorlijk lopen. Ze zijn toegankelijk via de knop **[!UICONTROL Logs]** die beschikbaar is in de werkbalk Handeling en in het deelvenster Eigenschappen van elke activiteit.

![](assets/logs-button.png)

Het scherm **[!UICONTROL Composition logs and tasks]** biedt een geschiedenis van de uitvoering van de compositie, waarbij alle handelingen van de gebruiker worden opgenomen en fouten worden aangetroffen.

<!-- à confirmer, pas trouvé dans les options = The workflow history is saved for the duration specified in the workflow execution options. During this duration, all the messages are therefore saved, even after a restart. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the ![](assets/delete_darkgrey-24px.png) button.-->

De historie wordt ingedeeld in verschillende tabbladen, die hieronder worden beschreven:

* Het tabblad **[!UICONTROL Log]** bevat de uitvoeringsgeschiedenis van alle compositieactiviteiten. De uitgevoerde bewerkingen en uitvoeringsfouten worden chronologisch geïndexeerd.
* Het tabblad **[!UICONTROL Tasks]** bevat details over de uitvoeringsvolgorde van de activiteiten. Met de knop aan het einde van elke taak kunt u de gebeurtenisvariabelen weergeven die door de activiteit worden doorgegeven.
* Het tabblad **[!UICONTROL Variables]** bevat een lijst met alle variabelen die in de compositie worden doorgegeven. Het is beschikbaar wanneer het toegang tot van de logboeken en de taken van het samenstellingscanvas slechts. Het is nu beschikbaar wanneer u de logboeken opent vanuit het deelvenster met eigenschappen van een activiteit.  <!-- à confirmer-->

![](assets/logs-tasks.png)

Op alle tabbladen kunt u de weergegeven kolommen en hun volgorde kiezen, filters toepassen en het zoekveld gebruiken om snel de gewenste informatie te zoeken.

## Abonneren op waarschuwingen {#alerts}

Daarnaast kunt u zich abonneren op waarschuwingen om meldingen te ontvangen als de uitvoering van uw gefedereerde compositie is geslaagd of mislukt.

Om aan alarm in te tekenen, selecteer het ![ berichtpictogram ](/help/assets/icons/bell.png), dat door het ![ montagespictogram ](/help/assets/icons/settings.png) wordt gevolgd.

![ zowel worden het bericht als de montagespictogrammen benadrukt.](assets/monitor/select-notifications.png){zoomable="yes"}{width="70%"}

De pagina met instellingen voor meldingen wordt weergegeven. Selecteer op deze pagina **[!UICONTROL Experience Platform]** en kies de gewenste kanalen voor waarschuwingen. Selecteer **[!UICONTROL In-app]** als u de meldingen in de gebruikersinterface wilt weergeven.

![ checkbox in-app wordt geselecteerd binnen de sectie van Experience Platform.](assets/monitor/add-alerts.png){zoomable="yes"}{width="50%"}

Als **[!UICONTROL In-app]** is geselecteerd, krijgt u nu een melding voor het uitvoeren van composities.

![ het alarm wordt getoond, tonend de samenstellingssuccessen en mislukkingen.](assets/monitor/view-alerts.png){zoomable="yes"}{width="70%"}

## Opdrachten voor het uitvoeren van composities {#execution-commands}

De actiebalk in de rechterbovenhoek biedt opdrachten waarmee u de uitvoering van de compositie kunt beheren.

![](assets/execution-actions.png)

Beschikbare acties zijn:

* **[!UICONTROL Start]**: hiermee wordt de uitvoering van de compositie gestart, die vervolgens de status **[!UICONTROL In progress]** krijgt. De samenstelling is begonnen en de eerste activiteiten worden geactiveerd.

* **[!UICONTROL Resume]**: hiermee hervat u de uitvoering van de compositie die was gepauzeerd. De compositie neemt de status **[!UICONTROL In progress]** over.

* **[!UICONTROL Pause]** de uitvoering van de compositie, die dan de **[!UICONTROL Paused]** status krijgt. Er zullen geen nieuwe activiteiten worden geactiveerd totdat de activiteiten worden hervat, maar de lopende activiteiten worden niet opgeschort.

* **[!UICONTROL Stop]** Een compositie die wordt uitgevoerd en die vervolgens de status **[!UICONTROL Finished]** krijgt. De lopende bewerkingen worden indien mogelijk onderbroken. U kunt de compositie niet hervatten vanaf dezelfde plaats als waar deze is gestopt.

* **[!UICONTROL Restart]**: stopt en start vervolgens een compositie opnieuw. In de meeste gevallen kunt u de toepassing sneller opnieuw starten, aangezien het stoppen een bepaalde hoeveelheid tijd in beslag neemt en de knop **[!UICONTROL Start]** alleen beschikbaar is wanneer de stop effectief is.

