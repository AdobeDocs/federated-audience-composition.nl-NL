---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
badge: label="Beperkte beschikbaarheid" type="Informative"
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: bd3223a77f490a43487e21662d8f766d4f9b06fc
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# De compositie maken en configureren {#create}

De eerste stap om een samenstelling tot stand te brengen moet zijn etiket bepalen en extra montages vormen indien nodig.

## Create the composition {#create-the-composition}

1. **[!UICONTROL Audiences]****[!UICONTROL Federated compositions]**

1. Klik op de knop **[!UICONTROL Create composition]**.

   ![](assets/composition-create.png)

1. **[!UICONTROL Properties]** Only the schemas associated to this data model will be available in your composition&#39;s activities.

   ![](assets/composition-select-schema.png)

1. Klik op **[!UICONTROL Create]**. The composition canvas displays. You can now configure your composition by adding as many activities as needed to suit your needs before executing it:

   * [Learn how to orchestrate activities](orchestrate-activities.md)
   * [ leer hoe te om een samenstelling te beginnen en te controleren ](start-monitor-composition.md)

## Vorm de montages van de samenstelling {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Compositie-eigenschappen"
>abstract="This section provides generic composition properties that are also accessible when creating the composition."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Composition segmentation"
>abstract="By default, only the working tables of the last execution of the composition are kept. You can enable this option to keep working tables for testing purposes. **** It must never be checked in a production environment."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Error management settings"
>abstract="In this section, you can define how to manage errors during the execution. You can choose to pause the process, ignore a certain number of errors, or stop the composition execution."

Wanneer het toegang hebben tot van een samenstelling, kunt u tot geavanceerde montages toegang hebben die u, bijvoorbeeld, toestaan om te bepalen hoe de samenstelling zich in het geval van fout zou moeten gedragen. Voor toegang tot deze extra opties klikt u op de knop **[!UICONTROL Settings]** in de bovenste sectie van het scherm voor het maken van composities.

![](assets/composition-create-settings.png)

De beschikbare instellingen zijn als volgt:

* **[!UICONTROL Label]**: wijzig het label van de compositie.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. Working tables from previous executions are purged by a technical composition, which runs on a daily basis.

  If this option is enabled, working tables will be kept even after the composition has been executed. **** It must never be checked in a production composition.

* **[!UICONTROL Error management]** There are three possible options:

   * **[!UICONTROL Suspend the process]****[!UICONTROL Failed]** **[!UICONTROL Resume]**
   * **[!UICONTROL Ignore]****[!UICONTROL Failed]****[!UICONTROL Started]**
   * **[!UICONTROL Abort the process]**: De compositie wordt automatisch gestopt en de status wordt gewijzigd in **[!UICONTROL Failed]** . Zodra de kwestie wordt opgelost, begin de samenstelling opnieuw gebruikend de **[!UICONTROL Start]** knoop.

* **[!UICONTROL Consecutive errors]**: geef op hoeveel fouten kunnen worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de samenstellingsstatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de compositie nooit gestopt, ongeacht het aantal fouten.
