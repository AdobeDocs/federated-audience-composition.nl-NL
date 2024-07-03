---
audience: end-user
title: Composities maken
description: Leer hoe u composities maakt
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---


# Vorm de montages van de samenstelling {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Compositie-eigenschappen"
>abstract="Deze sectie verstrekt generische samenstellingseigenschappen die ook toegankelijk zijn wanneer het creëren van de samenstelling."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Samenstellingssegmentatie"
>abstract="Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. U kunt deze optie inschakelen om werktabellen bij te houden voor testdoeleinden. Het moet worden gebruikt **alleen** op ontwikkelings- of staging-omgevingen. Het mag nooit worden gecontroleerd in een productieomgeving."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Instellingen voor foutbeheer"
>abstract="In deze sectie kunt u definiëren hoe u fouten tijdens de uitvoering kunt beheren. U kunt ervoor kiezen het proces te pauzeren, een bepaald aantal fouten te negeren of de uitvoering van de compositie te stoppen."

Wanneer het toegang hebben tot van een samenstelling, kunt u tot geavanceerde montages toegang hebben die u, bijvoorbeeld, toestaan om te bepalen hoe de samenstelling in het geval van fout zou moeten gedragen, of de vertraging beheren waarna de samenstellingsgeschiedenis zou moeten worden gezuiverd.

Klik op de knop **Instellingen** boven het canvas.

![](assets/composition-create-settings.png)

De beschikbare instellingen zijn als volgt:

* **[!UICONTROL Label]**: Wijzig het label van de compositie.

* **[!UICONTROL Keep the result of interim populations between two executions]**: Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. De werktabellen van vorige uitvoeringen worden door een technische samenstelling gezuiverd, die dagelijks loopt.

  Als deze optie wordt toegelaten, zullen het werken lijsten worden gehouden zelfs nadat de samenstelling is uitgevoerd. U kunt het voor testdoeleinden gebruiken en daarom moet het worden gebruikt **alleen** op ontwikkelings- of staging-omgevingen. Het mag nooit in een productiesamenstelling worden gecontroleerd.

* **[!UICONTROL Error management]**: In deze sectie kunt u de handelingen definiëren die moeten worden uitgevoerd als een compositieactiviteit fouten bevat. Er zijn drie mogelijke opties:

   * **[!UICONTROL Suspend the process]**: De compositie wordt automatisch gepauzeerd en de status wordt gewijzigd in **[!UICONTROL Failed]**. Zodra de kwestie wordt opgelost, hervat de samenstelling gebruikend **[!UICONTROL Resume]** knoppen.
   * **[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]**, maar de samenstelling houdt de **[!UICONTROL Started]** status.
   * **[!UICONTROL Abord the process]**: De compositie wordt automatisch gestopt en de status wordt gewijzigd in **[!UICONTROL Failed]**. Zodra de kwestie wordt opgelost, herstart de samenstelling gebruikend **[!UICONTROL Start]** knop.

* **[!UICONTROL Consecutive errors]**: Geef het aantal fouten op dat kan worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de samenstellingsstatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de compositie nooit gestopt, ongeacht het aantal fouten.
