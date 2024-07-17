---
audience: end-user
title: De activiteit Splitsen gebruiken
description: Leer hoe u de activiteit Splitsen gebruikt
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---


# Splitsen {#split}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="Gesplitste activiteit"
>abstract="De **Gesplitste** activiteit staat u toe om inkomende populaties in veelvoudige subsets te segmenteren die op verschillende selectiecriteria, zoals het filtreren regels of populatiegrootte worden gebaseerd."

De **Gesplitste** activiteit staat u toe om inkomende populaties in veelvoudige subsets te segmenteren die op verschillende selectiecriteria, zoals het filtreren regels of populatiegrootte worden gebaseerd.

## De activiteit Splitsen configureren {#split-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="Segmenten voor splitsingsactiviteit"
>abstract="Voeg zoveel subsets toe als u wilt om de binnenkomende populatie te segmenteren.<br/></br> wanneer de **Gesplitste** activiteit wordt uitgevoerd, wordt de bevolking gesegmenteerd over de verschillende ondergroepen in de orde zij aan de activiteit worden toegevoegd. Voordat u de compositie start, moet u ervoor zorgen dat u de subsets in de gewenste volgorde hebt geplaatst met de pijlknoppen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="Activiteitsfilter splitsen"
>abstract="Als u een filtervoorwaarde op de subset wilt toepassen, klikt u op **[!UICONTROL Create filter]** en configureert u de gewenste filterregel met de querymodelfunctie. Neem bijvoorbeeld profielen op van de binnenkomende populatie waarvan het e-mailadres voorkomt in de database."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="Limiet voor gesplitste activiteit"
>abstract="Als u het aantal profielen wilt beperken dat door de subset wordt geselecteerd, schakelt u de optie **[!UICONTROL Enable limit]** in en geeft u het aantal of de percentages van de populatie op die u wilt opnemen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="Splitsen op activiteit"
>abstract="Wanneer u een populatielimiet voor een subset instelt, kunt u de geselecteerde profielen op basis van een specifiek profielkenmerk in oplopende of aflopende volgorde rangschikken. Om dit te doen, knevel op **het sorteren** optie toe. U kunt bijvoorbeeld een subset beperken tot alleen de bovenste 50 profielen met het hoogste aankoopbedrag."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="Splitsen genereert complement"
>abstract="Zodra u alle subsets hebt gevormd, kunt u de resterende populatie selecteren die geen van de subsets aanpast en hen in een extra uitgaande overgang omvat. Om dit te doen, op **van een knevel te voorzien produceert complement** optie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="Alle subsets in dezelfde tabel genereren"
>abstract="Schakel deze optie in en uit om alle subsets te groeperen in één uitvoerovergang."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="Lege overgang overslaan"
>abstract="Schakel de optie **[!UICONTROL Skip empty transition]** in en uit om de uitvoerovergang voor deze subset uit te schakelen als de binnenkomende populatie leeg is."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="Overlappende uitvoerpopulaties inschakelen"
>abstract="Met de optie **[!UICONTROL Enable overlapping of output populations]** kunt u populaties beheren die tot verschillende subsets behoren. Wanneer het vakje niet wordt gecontroleerd, zorgt de gespleten activiteit ervoor een ontvanger niet in verscheidene outputovergangen kan aanwezig zijn, zelfs als het aan de criteria van verscheidene subsets voldoet. Deze worden als doel ingesteld op het eerste tabblad met overeenkomende criteria. Als het selectievakje is ingeschakeld, kunnen de ontvangers in verschillende subsets worden gevonden als ze voldoen aan hun filtercriteria. Adobe Campaign raadt aan exclusieve criteria te hanteren."

Volg deze stappen om de **Gesplitste** activiteit te vormen:

1. Voeg a **Gesplitste** activiteit aan uw samenstelling toe.

1. Het deelvenster voor activiteitenconfiguratie wordt geopend met een standaardsubset. Klik **toevoegen segment** knoop om zo vele ondergroepen toe te voegen zoals gewenst om de inkomende bevolking te segmenteren.

   >[!IMPORTANT]
   >
   >Wanneer de **Gesplitste** activiteit wordt uitgevoerd, wordt de bevolking gesegmenteerd over de verschillende ondergroepen in de orde zij aan de activiteit worden toegevoegd. Als de eerste subset bijvoorbeeld 70% van de oorspronkelijke populatie herstelt, past de volgende toegevoegde subset zijn selectiecriteria alleen toe op de resterende 30%, enzovoort.
   >
   >Voordat u de compositie start, moet u ervoor zorgen dat u de subsets in de gewenste volgorde hebt geplaatst. Hiervoor gebruikt u de pijlknoppen om de positie van een subset te wijzigen.

1. Nadat subsets zijn toegevoegd, toont de activiteit evenveel uitvoerovergangen als er subsets zijn. Wij adviseren sterk veranderend het etiket van elke ondergroep om hen in het samenstellingscanvas gemakkelijk te identificeren.

   ![](../assets/split.png)

1. Vorm hoe elke ondergroep de inkomende bevolking zou moeten filtreren. Ga als volgt te werk om dit te doen:

   1. Vouw de subset uit om de eigenschappen ervan weer te geven.

      ![](../assets/split-subset.png)

   1. Als u een filtervoorwaarde op de subset wilt toepassen, klikt u op **[!UICONTROL Create filter]** en configureert u de gewenste filterregel met de querymodelfunctie. Neem bijvoorbeeld profielen op van de binnenkomende populatie waarvan het e-mailadres voorkomt in de database. [ Leer hoe te met de vraagmodelaar ](../../query/query-modeler-overview.md) te werken

   1. Als u het aantal profielen wilt beperken dat door de subset wordt geselecteerd, schakelt u de optie **[!UICONTROL Enable limit]** in en geeft u het aantal of de percentages van de populatie op die u wilt opnemen.

   1. Als u een overgang wilt uitschakelen als de binnenkomende populatie leeg is, schakelt u de optie **[!UICONTROL Skip empty transition]** in of uit. Als geen profiel overeenkomt met de subset, gaat de compositie niet over naar de volgende activiteit.

   >[!NOTE]
   >
   >Wanneer u een populatielimiet voor een subset instelt, kunt u de geselecteerde profielen op basis van een specifiek profielkenmerk in oplopende of aflopende volgorde rangschikken. Schakel hiertoe de optie **[!UICONTROL Enable sorting]** in. U kunt bijvoorbeeld een subset beperken tot alleen de bovenste 50 profielen met het hoogste aankoopbedrag.

1. Zodra u alle subsets hebt gevormd, kunt u de resterende populatie selecteren die geen van de subsets aanpast en hen in een extra uitgaande overgang omvat. Schakel hiertoe de optie **[!UICONTROL Generate complement]** in.

   >[!NOTE]
   >
   >Met de optie **[!UICONTROL Generate all subsets in the same table]** kunt u alle subsets groeperen in één uitvoerovergang.

1. Met de optie **[!UICONTROL Enable overlapping of output populations]** kunt u populaties beheren die tot verschillende subsets behoren:

   * Wanneer het vakje niet wordt gecontroleerd, zorgt de gespleten activiteit ervoor een ontvanger niet in verscheidene outputovergangen kan aanwezig zijn, zelfs als het aan de criteria van verscheidene subsets voldoet. Deze worden als doel ingesteld op het eerste tabblad met overeenkomende criteria.
   * Als het selectievakje is ingeschakeld, kunnen de ontvangers in verschillende subsets worden gevonden als ze voldoen aan hun filtercriteria. Adobe Campaign raadt aan exclusieve criteria te hanteren.

De activiteit wordt nu gevormd. Bij uitvoering wordt de populatie opgesplitst in de verschillende subgroepen, in de volgorde waarin ze aan de activiteit zijn toegevoegd.

<!--
## Example{#split-example}

In the following example, the **[!UICONTROL Split]** activity is used to segment an audience into distinct subsets based on the communication channel that we want to use :

* **Subset 1 "push"**: This subset comprises all profiles who have installed our mobile application.
* **Subset 2 "sms"**: Mobile phone users: For the remaining population that did not fall into Subset 1, subset 2 applies a filtering rule to select profiles with mobile phones in the database.
* **Complement transition**: This transition captures all the remaining profiles that did not match Subset 1 or Subset 2. Specifically, it includes profiles who neither installed the mobile application nor have a mobile phone, such as users who haven't installed the mobile app or lack a registered mobile number.

![](../assets/workflow-split-example.png)
-->
