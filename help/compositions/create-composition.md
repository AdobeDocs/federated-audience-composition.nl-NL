---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: 036dcb96d2d831e3a1d6ab50afef5b87e25b564b
workflow-type: tm+mt
source-wordcount: '1508'
ht-degree: 0%

---

# Een compositie maken

Met Federatieve compositie voor publiek kunt u composities maken, waarbij u verschillende activiteiten kunt gebruiken in een visueel canvas om een publiek te maken. Nadat u de compositie hebt gemaakt, worden de resulterende doelgroepen opgeslagen in Adobe Experience Platform en kunnen ze worden gebruikt in Experience Platform-bestemmingen en Adobe Journey Optimizer om klanten als doel in te stellen.

## Definieer uw compositie {#create}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Compositie-eigenschappen"
>abstract="Kies in dit scherm de sjabloon die u wilt gebruiken om de compositie te maken en geef een label op. Vouw de sectie ADDITIONAL OPTIONS uit om meer instellingen te configureren, zoals de interne naam van de compositie, de map, de tijdzone en de supervisorgroep. Het wordt hoogst geadviseerd om een supervisorgroep te selecteren zodat de exploitanten worden gealarmeerd als een fout voorkomt."

Om een samenstelling tot stand te brengen, zult u eerst zijn etiket moeten bepalen en naar keuze extra montages vormen.

Als u een compositie wilt maken, selecteert u **[!UICONTROL Audiences]** in de sectie **[!UICONTROL Customer]** , gevolgd door de tab **[!UICONTROL Federated compositions]** .

![&#x200B; de weg om tot de Federatieve compositiesectie toegang te hebben wordt benadrukt.](assets/create/access-compositions.png)

De pagina Bladeren met gefedereerde composities wordt weergegeven. Selecteer **[!UICONTROL Create composition]** om door te gaan met het maken van composities.

![](assets/composition-create.png)

Geef in de sectie **[!UICONTROL Properties]** een label voor de compositie op en selecteer een gegevensmodel. Slechts zullen de schema&#39;s verbonden aan dit gegevensmodel in de activiteiten van uw samenstelling beschikbaar zijn.

![](assets/composition-select-schema.png)

Selecteer **[!UICONTROL Create]**. Het compositicanvas wordt weergegeven. U kunt uw compositie nu configureren door activiteiten en overgangen toe te voegen aan het canvas.

## Compositiecanvas {#canvas}

Boven op het canvas hebt u toegang tot een werkbalk met opties voor het beheren en navigeren van uw activiteiten.

![](assets/canvas-toolbar.png)

Beschikbare opties zijn:

* **[!UICONTROL Multiple selection]**: Selecteer meerdere activiteiten om deze allemaal tegelijk te verwijderen of kopieer en plak ze.
* **[!UICONTROL Rotate]**: schakel het canvas naar verticaal om weer te geven.
* **[!UICONTROL Fit to screen]**: pas het zoomniveau van het canvas aan het scherm aan.
* **[!UICONTROL Zoom in]** / **[!UICONTROL Zoom out]** : zoom in of uit op het canvas.
* **[!UICONTROL Display map]**: hiermee opent u een opname van het canvas waarop wordt aangegeven waar u zich bevindt.

## Activiteiten toevoegen {#add-activities}

In het compositicanvas kunt u activiteiten en overgangen toevoegen die u helpen uw publiek te definiëren. De activiteiten laten u ** de componenten binnen het publiek bepalen terwijl de overgangen u *laten* de stroom van uw samenstelling organiseren.

Voor meer informatie over de activiteiten en de overgangen die voor gebruik beschikbaar zijn, lees het [&#x200B; overzicht van activiteiten &#x200B;](./activities.md).

## Activiteiten beheren {#manage-activities}

U kunt bewerkingen op toegevoegde activiteiten uitvoeren in het deelvenster Eigenschappen.

![](assets/activity-actions.png)

U kunt onder andere de volgende opties kiezen:

* **[!UICONTROL Delete]**: Verwijder de activiteit van het canvas.
* **[!UICONTROL Disable]/[!UICONTROL Enable]**: Schakel de activiteit uit of in. Wanneer de samenstelling wordt uitgevoerd, worden de gehandicapte activiteiten en de volgende activiteiten op de zelfde weg niet uitgevoerd en de samenstelling wordt tegengehouden.
* **[!UICONTROL Pause]/[!UICONTROL Resume]**: Pauze of hervat de activiteit. Wanneer de samenstelling wordt uitgevoerd, pauzeert het bij de gepauzeerde activiteit. De bijbehorende taak en alle taken die deze in hetzelfde pad volgen, worden niet uitgevoerd.
* **[!UICONTROL Copy]**: kopieert de activiteit om het op een andere plaats in de samenstelling te kleven. Selecteer hiertoe de knop **+** op een overgang en selecteer **[!UICONTROL Paste X activity]** . <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configureer **[!UICONTROL Execution options]** voor de geselecteerde activiteit. De volgende opties zijn beschikbaar voor uitvoering:
  +++Beschikbare opties voor uitvoering

  In de sectie **[!UICONTROL Properties]** kunt u algemene instellingen configureren voor de uitvoering van de activiteit:

   * **[!UICONTROL Execution]**: Definieer de handeling die moet worden uitgevoerd wanneer de handeling wordt gestart.
   * **[!UICONTROL Maximum execution duration]**: geef een duur op, bijvoorbeeld &quot;30s&quot; of &quot;1h&quot;. Als de activiteit niet wordt gebeëindigd nadat de gespecificeerde duur is verstreken, wordt een alarm teweeggebracht. Dit heeft geen invloed op de werking van de compositie.
   * **[!UICONTROL Time zone]**: selecteer de tijdzone van de activiteit. De federatieve Samenstelling van de Auditie staat u toe om de tijdverschillen tussen veelvoudige landen op het zelfde geval te beheren. De toegepaste instelling wordt geconfigureerd wanneer de instantie wordt gemaakt.
   * **[!UICONTROL Affinity]**: dwingt u de compositieactiviteit uit te voeren op een bepaalde computer. Hiervoor moet u een of meer affiniteiten voor de desbetreffende activiteit opgeven.
   * **[!UICONTROL Behavior]**: definieer de procedure die moet worden gevolgd wanneer asynchrone taken worden gebruikt.

  In de sectie **[!UICONTROL Error management]** kunt u opgeven welke actie moet worden uitgevoerd als er een fout optreedt.

  In de sectie **[!UICONTROL Initialization script]** kunt u variabelen initialiseren of eigenschappen van activiteiten wijzigen. Selecteer de knop **[!UICONTROL Edit code]** en typ het codefragment dat u wilt uitvoeren. Het script wordt aangeroepen wanneer de activiteit wordt uitgevoerd.

  +++
* **Logboeken en taken**: Bekijk de logboeken en de taken voor de geselecteerde activiteit.

## Uw compositie starten en controleren {#start-and-monitor}

Nadat u klaar bent met het toevoegen van uw activiteiten aan de samenstelling, kunt u de uitvoering van de samenstelling beginnen. Als u een compositie wilt starten, selecteert u de knop **[!UICONTROL Start]** in de rechterbovenhoek van het scherm.

![](assets/execution-actions.png)

| Actie | Beschrijving |
| ------ | ----------- |
| **Begin** | Begint de uitvoering van de samenstelling en beweegt het aan **Bezig** status. |
| **Pauze** | Pauzeert de uitvoering van de samenstelling en plaatst het aan de **Gepauzeerde** status. Geen nieuwe activiteiten zullen worden geactiveerd tot de samenstelling wordt hervat, maar de verrichtingen die lopend zijn worden **niet** opgeschort. |
| **Hervatten** | Hervat de uitvoering van de gepauzeerde samenstelling en plaatst het aan **Bezig** status. |
| **Einde** | Stopt de uitvoering van de samenstelling en plaatst het aan de **Voltooide** staat. U **kunt niet** de samenstelling van de zelfde plaats hervatten van waar het wordt tegengehouden. |
| **Begin** opnieuw | Stopt en herstart de uitvoering van de compositie. |

Wanneer de samenstelling loopt, wordt elke activiteit in het canvas uitgevoerd in een opeenvolgende orde, tot het eind van de samenstelling wordt bereikt. U kunt de voortgang van doelprofielen in real time volgen gebruikend een visuele stroom. Hierdoor kunt u snel de status van elke activiteit en het aantal profielen identificeren dat tussen de activiteiten overgaat.

![](assets/composition-visual-flow.png)

De visuele indicatoren in de rechterbovenhoek van elke activiteit geven de status van de uitvoering aan:

| Visuele indicator | Beschrijving |
| ---------------- | ------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | De activiteit wordt momenteel uitgevoerd. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | De activiteit vereist uw aandacht. Dit kan inhouden dat de verzending van een levering wordt bevestigd of dat de nodige actie wordt ondernomen. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | Er is een fout opgetreden in de activiteit. Om de kwestie op te lossen, open samenstellingslogboeken voor meer informatie. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | De activiteit is uitgevoerd. |

### Logboeken en taken controleren {#monitor-logs}

Bovendien, kunt u de samenstellingslogboeken bekijken om ervoor te zorgen zij behoorlijk lopen. Selecteer **[!UICONTROL Logs]** in de werkbalk Handeling om deze informatie weer te geven.

![](assets/logs-button.png)

Het scherm **[!UICONTROL Composition logs and tasks]** wordt weergegeven. Dit verstrekt een geschiedenis van de samenstellingsuitvoering, registrerend alle gebruikersacties en ondervonden fouten.

De historie wordt ingedeeld in verschillende tabbladen, die hieronder worden beschreven:

* Het tabblad **[!UICONTROL Log]** bevat de uitvoeringsgeschiedenis van alle compositieactiviteiten. De uitgevoerde bewerkingen en uitvoeringsfouten worden chronologisch geïndexeerd.
* Het tabblad **[!UICONTROL Tasks]** bevat details over de uitvoeringsvolgorde van de activiteiten. Met de knop aan het einde van elke taak kunt u de gebeurtenisvariabelen weergeven die door de activiteit worden doorgegeven.
* Het tabblad **[!UICONTROL Variables]** bevat een lijst met alle variabelen die in de compositie worden doorgegeven. Het is beschikbaar wanneer het toegang tot van de logboeken en de taken van het samenstellingscanvas slechts. Het is nu beschikbaar wanneer u de logboeken opent vanuit het deelvenster met eigenschappen van een activiteit.

![](assets/logs-tasks.png)

Op alle tabbladen kunt u de weergegeven kolommen en hun volgorde kiezen, filters toepassen en het zoekveld gebruiken om snel de gewenste informatie te zoeken.

### Abonneren op waarschuwingen {#alerts}

U kunt zich ook abonneren op waarschuwingen om meldingen te ontvangen als de uitvoering van uw gefedereerde compositie is geslaagd of mislukt.

Om aan alarm in te tekenen, selecteer het ![&#x200B; berichtpictogram &#x200B;](/help/assets/icons/bell.png), dat door het ![&#x200B; montagespictogram &#x200B;](/help/assets/icons/settings.png) wordt gevolgd.

![&#x200B; zowel worden het bericht als de montagespictogrammen benadrukt.](assets/monitor/select-notifications.png){zoomable="yes"}{width="70%"}

De pagina met instellingen voor meldingen wordt weergegeven. Selecteer op deze pagina **[!UICONTROL Experience Platform]** en kies de gewenste kanalen voor waarschuwingen. Selecteer **[!UICONTROL In-app]** als u de meldingen in de gebruikersinterface wilt weergeven.

![&#x200B; checkbox in-app wordt geselecteerd binnen de sectie van Experience Platform.](assets/monitor/add-alerts.png){zoomable="yes"}{width="50%"}

Als **[!UICONTROL In-app]** is geselecteerd, krijgt u nu een melding voor het uitvoeren van composities.

![&#x200B; het alarm wordt getoond, tonend de samenstellingssuccessen en mislukkingen.](assets/monitor/view-alerts.png){zoomable="yes"}{width="70%"}

## Vorm de montages van de samenstelling {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Compositie-eigenschappen"
>abstract="Deze sectie verstrekt generische samenstellingseigenschappen die ook toegankelijk zijn wanneer het creëren van de samenstelling."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Samenstellingssegmentatie"
>abstract="Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. U kunt deze optie inschakelen om werktabellen bij te houden voor testdoeleinden. Het moet **slechts** op ontwikkeling of het opvoeren milieu&#39;s worden gebruikt. Het mag nooit worden gecontroleerd in een productieomgeving."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Instellingen voor foutbeheer"
>abstract="In deze sectie kunt u definiëren hoe u fouten tijdens de uitvoering kunt beheren. U kunt ervoor kiezen het proces te pauzeren, een bepaald aantal fouten te negeren of de uitvoering van de compositie te stoppen."

Wanneer het toegang hebben tot van een samenstelling, kunt u tot geavanceerde montages toegang hebben die u, bijvoorbeeld, toestaan om te bepalen hoe de samenstelling zich in het geval van fout zou moeten gedragen.

Als u toegang wilt krijgen tot deze extra opties, selecteert u **[!UICONTROL Settings]** in de bovenste sectie van het scherm voor het maken van composities.

![](assets/composition-create-settings.png)

| Instellingen | Beschrijving |
| -------- | ----------- |
| **[!UICONTROL Label]** | Werk de naam bij die aan de samenstelling wordt gegeven. |
| **[!UICONTROL Keep the result of interim populations between two executions]** | Als deze optie wordt toegelaten, zullen het werken lijsten worden gehouden zelfs nadat de samenstelling is uitgevoerd. Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. De werktabellen van eerdere uitvoeringen worden dagelijks verwijderd. Schakel deze instelling alleen in in een ontwikkelings- of testomgeving. U zou **nooit** dit plaatsen op een productiemilieu moeten toelaten. |
| **[!UICONTROL Error management]** | Bepaalt de acties die als de samenstelling een fout heeft worden genomen. Er zijn drie mogelijke opties: <ul><li>**[!UICONTROL Suspend the process]**: De compositie wordt automatisch gepauzeerd en de status verandert in **[!UICONTROL Failed]** . Nadat het probleem is opgelost, hervat u de compositie met de knoppen **[!UICONTROL Resume]** .</li><li>**[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]** , maar de compositie behoudt de status **[!UICONTROL Started]** .</li><li>**[!UICONTROL Abort the process]**: De compositie wordt automatisch gestopt en de status wordt gewijzigd in **[!UICONTROL Failed]** . Zodra de kwestie wordt opgelost, begin de samenstelling opnieuw gebruikend de **[!UICONTROL Start]** knoop.</li></ul> |
| **[!UICONTROL Consecutive errors]** | Geef het aantal fouten op dat kan worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de samenstellingsstatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de compositie nooit gestopt, ongeacht het aantal fouten. |
