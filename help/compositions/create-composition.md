---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
source-git-commit: 194ae763f5040f11eba0fe30aa302064f5d0606a
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---


# Een compositie maken en uitvoeren {#create-compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_creation_properties"
>title="Workfloweigenschappen"
>abstract="Kies in dit scherm de sjabloon die u wilt gebruiken om de workflow te maken en geef een label op. Vouw de sectie EXTRA OPTIONS uit om meer instellingen te configureren, zoals de interne naam van de workflow, de map, de tijdzone en de supervisorgroep. Het wordt hoogst geadviseerd om een supervisorgroep te selecteren zodat de exploitanten worden gealarmeerd als een fout voorkomt."

## De compositie maken {#create}

Ga als volgt te werk om een compositie te maken:

1. Toegang krijgen tot de **[!UICONTROL Audiences]** en selecteert u de **[!UICONTROL Federated compositions]** tab.

1. Klik op de knop **[!UICONTROL Create composition]**.

1. In de **[!UICONTROL Properties]** , geeft u een label voor uw compositie op en klikt u op **[!UICONTROL Create]**.

1. Het compositicanvas wordt weergegeven. U kunt uw samenstelling nu vormen door zo vele activiteiten toe te voegen zoals nodig om uw behoeften aan te passen alvorens het uit te voeren. U kunt extra montages zoals het etiket van de samenstelling of opties met betrekking tot foutenbeheer bij de uitvoering van de samenstelling ook vormen.

Meer informatie vindt u in de volgende secties:

* [Vorm de montages van de samenstelling](#starting-audience)
* [Activiteiten toevoegen](#action-activities)
* [De compositie uitvoeren en de uitvoering ervan controleren](#save)

## Vorm de montages van de samenstelling {#settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Compositie-eigenschappen"
>abstract="Deze sectie verstrekt generische samenstellingseigenschappen die ook toegankelijk zijn wanneer het creëren van de samenstelling."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Samenstellingssegmentatie"
>abstract="Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. U kunt deze optie inschakelen om werktabellen bij te houden voor testdoeleinden. Het moet worden gebruikt **alleen** op ontwikkelings- of staging-omgevingen. Het mag nooit worden gecontroleerd in een productieomgeving."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Instellingen voor foutbeheer"
>abstract="In deze sectie kunt u definiëren hoe u fouten tijdens de uitvoering kunt beheren. U kunt ervoor kiezen het proces te pauzeren, een bepaald aantal fouten te negeren of de uitvoering van de compositie te stoppen."

Klik op de knop **Instellingen** knoop om tot extra opties voor de samenstelling toegang te hebben:

* **[!UICONTROL Label]**: Wijzig het label van de compositie.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. De werklijsten van vorige uitvoeringen worden gezuiverd door een technische werkschema, die op een dagelijkse basis loopt.

  Als deze optie wordt toegelaten, zullen het werken lijsten worden gehouden zelfs nadat de samenstelling is uitgevoerd. U kunt het voor testdoeleinden gebruiken en daarom moet het worden gebruikt **alleen** op ontwikkelings- of staging-omgevingen. Deze mag nooit in een productiewerkstroom worden gecontroleerd.

* **[!UICONTROL Error management]**: In deze sectie kunt u de handelingen definiëren die moeten worden uitgevoerd als een compositieactiviteit fouten bevat. Er zijn drie mogelijke opties:

   * **[!UICONTROL Suspend the process]**: De compositie wordt automatisch gepauzeerd en de status wordt gewijzigd in **[!UICONTROL Failed]**. Zodra de kwestie wordt opgelost, hervat de samenstelling gebruikend **[!UICONTROL Resume]** knoppen.
   * **[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]**, maar de samenstelling houdt de **[!UICONTROL Started]** status.
   * **[!UICONTROL Abord the process]**: De compositie wordt automatisch gestopt en de status wordt gewijzigd in **[!UICONTROL Failed]**. Zodra de kwestie wordt opgelost, herstart de samenstelling gebruikend **[!UICONTROL Start]** knop.

* **[!UICONTROL Consecutive errors]**: Geef het aantal fouten op dat kan worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de samenstellingsstatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de compositie nooit gestopt, ongeacht het aantal fouten.

## Activiteiten toevoegen {#activities}

Het samenstellingscanvas staat u toe om zo vele activiteiten toe te voegen zoals nodig in de samenstelling om uw behoeften aan te passen.

Om dit te doen, klik + knoop op de samenstellingsweg dan voeg de gewenste activiteit toe. Het juiste paneel opent, toestaand u om de onlangs toegevoegde activiteit te vormen. [Meer informatie over de activiteiten in composities en hoe u deze configureert](../compositions/activities/about-activities.md)

Als u een activiteit wilt verwijderen uit het canvas, selecteert u de activiteit en klikt u op de knop Verwijderen in het rechterdeelvenster. Als de activiteit die u wilt schrappen een ouder van andere activiteiten in de samenstelling is, toont een berichtvertoningen, toestaand u om te specificeren als u de geselecteerde activiteit slechts, of al zijn kindactiviteiten wilt schrappen.

## De compositie uitvoeren {#execute}

Zodra uw samenstelling klaar is, klik **[!UICONTROL Start]** om het uit te voeren en het resulterende publiek op te slaan in Adobe Experience Platform. &quot;U kunt de uitvoering van de workflow controleren met de **Logboeken** knop. Er zijn drie tabbladen beschikbaar waarmee u de uitvoering kunt controleren:

* **[!UICONTROL Logs]**:
* **[!UICONTROL Tasks]**:
* **[!UICONTROL Variables]**:
