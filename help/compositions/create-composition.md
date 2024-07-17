---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---


# De compositie maken en configureren {#create}

De eerste stap om een samenstelling tot stand te brengen moet zijn etiket bepalen en extra montages vormen indien nodig.

## De compositie maken {#create-the-composition}

1. Open het menu **[!UICONTROL Audiences]** en selecteer de tab **[!UICONTROL Federated compositions]** .

1. Klik op de knop **[!UICONTROL Create composition]**.

   ![](assets/composition-create.png)

1. Geef in de sectie **[!UICONTROL Properties]** een label voor de compositie op en klik op **[!UICONTROL Create]** .

1. Het compositicanvas wordt weergegeven. U kunt uw samenstelling nu vormen door zo vele activiteiten toe te voegen zoals nodig om uw behoeften aan te passen alvorens het uit te voeren:

   * [Leer hoe u activiteiten kunt ordenen](#action-activities)
   * [ leer hoe te om een samenstelling te beginnen en te controleren ](#save)

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

Voor toegang tot extra opties voor uw compositie klikt u op de knop **[!UICONTROL Settings]** in de bovenste sectie van het scherm voor het maken van composities.

![](assets/composition-create-settings.png)

De beschikbare instellingen zijn als volgt:

* **[!UICONTROL Label]**: wijzig het label van de compositie.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. De werktabellen van vorige uitvoeringen worden door een technische samenstelling gezuiverd, die dagelijks loopt.

  Als deze optie wordt toegelaten, zullen het werken lijsten worden gehouden zelfs nadat de samenstelling is uitgevoerd. U kunt het voor testende doeleinden gebruiken en daarom moet **slechts** op ontwikkeling of het opvoeren milieu&#39;s worden gebruikt. Het mag nooit in een productiesamenstelling worden gecontroleerd.

* **[!UICONTROL Error management]**: met deze optie kunt u de handelingen definiëren die moeten worden uitgevoerd als een compositieactiviteit fouten bevat. Er zijn drie mogelijke opties:

   * **[!UICONTROL Suspend the process]**: De compositie wordt automatisch gepauzeerd en de status verandert in **[!UICONTROL Failed]** . Nadat het probleem is opgelost, hervat u de compositie met de knoppen **[!UICONTROL Resume]** .
   * **[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]** , maar de compositie behoudt de status **[!UICONTROL Started]** .
   * **[!UICONTROL Abord the process]**: De compositie wordt automatisch gestopt en de status verandert in **[!UICONTROL Failed]** . Zodra de kwestie wordt opgelost, begin de samenstelling opnieuw gebruikend de **[!UICONTROL Start]** knoop.

* **[!UICONTROL Consecutive errors]**: geef op hoeveel fouten kunnen worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de samenstellingsstatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de compositie nooit gestopt, ongeacht het aantal fouten.
