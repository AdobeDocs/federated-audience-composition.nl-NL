---
audience: end-user
title: Aan de slag met composities
description: Leer hoe u begint met composities
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Aan de slag met composities {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Compositie-eigenschappen"
>abstract="Deze sectie verstrekt generische samenstellingseigenschappen die ook toegankelijk zijn wanneer het creëren van de samenstelling."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Samenstellingssegmentatie"
>abstract="Door gebrek, slechts worden de het werk lijsten van de laatste uitvoering van de samenstelling gehouden. U kunt deze optie inschakelen om werktabellen bij te houden voor testdoeleinden. Het moet worden gebruikt **alleen** op ontwikkelings- of staging-omgevingen. Het mag nooit worden gecontroleerd in een productieomgeving."




## Wat is een samenstelling? {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="Composities"
>abstract="In dit scherm, kunt u tot de volledige lijst van samenstellingen toegang hebben, hun huidige status, laatste/volgende uitvoeringsdata controleren, en een nieuwe samenstelling creëren."


## Instellingen voor foutbeheer  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Instellingen voor foutbeheer"
>abstract="In deze sectie kunt u definiëren hoe u fouten tijdens de uitvoering kunt beheren. U kunt ervoor kiezen het proces te pauzeren, een bepaald aantal fouten te negeren of de uitvoering van de compositie te stoppen."

* **[!UICONTROL Error management]**: In dit veld kunt u de handelingen definiëren die moeten worden uitgevoerd als een compositieactiviteit fouten bevat.
Er zijn drie mogelijke opties:

   * **[!UICONTROL Suspend the process]**: De compositie wordt automatisch gepauzeerd en de status wordt gewijzigd in **[!UICONTROL Failed]**. Zodra de kwestie wordt opgelost, hervat de samenstelling gebruikend **[!UICONTROL Resume]** knoppen.
   * **[!UICONTROL Ignore]**: De status van de taak die de fout heeft veroorzaakt, verandert in **[!UICONTROL Failed]**, maar de samenstelling houdt de **[!UICONTROL Started]** status.
   * **[!UICONTROL Abord the process]**: De compositie wordt automatisch gestopt en de status wordt gewijzigd in **[!UICONTROL Failed]**. Zodra de kwestie wordt opgelost, herstart de samenstelling gebruikend **[!UICONTROL Start]** knop.

* **[!UICONTROL Consecutive errors]**: Dit veld is beschikbaar wanneer de **[!UICONTROL Ignore]** waarde is geselecteerd in het dialoogvenster **[!UICONTROL In case of errors]** veld. U kunt opgeven hoeveel fouten kunnen worden genegeerd voordat het proces wordt gestopt. Zodra dit aantal wordt bereikt, verandert de samenstellingsstatus in **[!UICONTROL Failed]**. Als de waarde van dit veld 0 is, wordt de compositie nooit gestopt, ongeacht het aantal fouten.
