---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: cc692662aa30e3263ef2da68ecd571f09c8dc6b8
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Creeer en vorm de samenstelling {#create}

De eerste stap om een samenstelling tot stand te brengen moet zijn etiket bepalen en extra montages vormen indien nodig.

## De compositie maken {#create-the-composition}

Als u een compositie wilt maken, selecteert u **[!UICONTROL Audiences]** in de sectie **[!UICONTROL Customer]** , gevolgd door de tab **[!UICONTROL Federated compositions]** .

![ de weg om tot de Federatieve compositiesectie toegang te hebben wordt benadrukt.](assets/create/access-compositions.png)

De pagina Bladeren met gefedereerde composities wordt weergegeven. Selecteer **[!UICONTROL Create composition]** om door te gaan met het maken van composities.

![](assets/composition-create.png)

In de sectie **[!UICONTROL Properties]** geeft u een label voor de compositie op en selecteert u een gegevensmodel. Slechts zullen de schema&#39;s verbonden aan dit gegevensmodel in de activiteiten van uw samenstelling beschikbaar zijn.

![](assets/composition-select-schema.png)

Selecteer **[!UICONTROL Create]**. Het compositicanvas wordt weergegeven. U kunt uw samenstelling nu vormen door zo vele activiteiten toe te voegen zoals nodig om uw behoeften aan te passen alvorens het uit te voeren:

* [Leer hoe u activiteiten kunt ordenen](orchestrate-activities.md)
* [ leer hoe te om een samenstelling te beginnen en te controleren ](start-monitor-composition.md)

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

De beschikbare instellingen zijn als volgt:

* **[!UICONTROL Label]**: wijzig het label van de compositie.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. De werktabellen van vorige uitvoeringen worden door een technische samenstelling gezuiverd, die dagelijks loopt.

  Als deze optie wordt toegelaten, zullen het werken lijsten worden gehouden zelfs nadat de samenstelling is uitgevoerd. U kunt het voor testende doeleinden gebruiken en daarom moet **slechts** op ontwikkeling of het opvoeren milieu&#39;s worden gebruikt. Het mag nooit in een productiesamenstelling worden gecontroleerd.

* **[!UICONTROL Error management]**: met deze optie kunt u de handelingen definiëren die moeten worden uitgevoerd als een compositieactiviteit fouten bevat. Er zijn drie mogelijke opties:

   * **[!UICONTROL Suspend the process]**: De compositie wordt automatisch gepauzeerd en de status verandert in **[!UICONTROL Failed]** . Nadat het probleem is opgelost, hervat u de compositie met de knoppen **[!UICONTROL Resume]** .
   * **[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]** , maar de compositie behoudt de status **[!UICONTROL Started]** .
   * **[!UICONTROL Abort the process]**: De compositie wordt automatisch gestopt en de status wordt gewijzigd in **[!UICONTROL Failed]** . Zodra de kwestie wordt opgelost, begin de samenstelling opnieuw gebruikend de **[!UICONTROL Start]** knoop.

* **[!UICONTROL Consecutive errors]**: geef op hoeveel fouten kunnen worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de samenstellingsstatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de compositie nooit gestopt, ongeacht het aantal fouten.
