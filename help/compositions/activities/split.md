---
audience: end-user
title: De activiteit Splitsen gebruiken
description: Leer hoe u de activiteit Splitsen gebruikt
source-git-commit: c4c9eba1dcb3adff3028175a389ff6e4eaf12bc0
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---


# Splitsen {#split}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="Gesplitste activiteit"
>abstract="De **Splitsen** met activiteit kunt u inkomende populaties segmenteren in meerdere subsets op basis van verschillende selectiecriteria, zoals filterregels of populatiegrootte."

De **Splitsen** met activiteit kunt u inkomende populaties segmenteren in meerdere subsets op basis van verschillende selectiecriteria, zoals filterregels of populatiegrootte.

## De activiteit Splitsen configureren {#split-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="Segmenten voor splitsingsactiviteit"
>abstract="Voeg zoveel subsets toe als u wilt om de binnenkomende populatie te segmenteren.<br/></br>Wanneer de **Splitsen** de activiteit wordt uitgevoerd, wordt de populatie over de verschillende subsets verdeeld in de volgorde waarin ze aan de activiteit worden toegevoegd. Voordat u de compositie start, moet u ervoor zorgen dat u de subsets in de gewenste volgorde hebt geplaatst met de pijlknoppen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="Activiteitsfilter splitsen"
>abstract="Als u een filtervoorwaarde op de subset wilt toepassen, klikt u op **[!UICONTROL Create filter]** en vorm de gewenste het filtreren regel gebruikend de vraagmodeler. Neem bijvoorbeeld profielen op van de binnenkomende populatie waarvan het e-mailadres voorkomt in de database."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="Limiet voor gesplitste activiteit"
>abstract="Als u het aantal profielen dat door de subset is geselecteerd, wilt beperken, schakelt u het **[!UICONTROL Enable limit]** en geeft het aantal of de percentages van de populatie aan die moeten worden opgenomen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="Splitsen op activiteit"
>abstract="Wanneer u een populatielimiet voor een subset instelt, kunt u de geselecteerde profielen op basis van een specifiek profielkenmerk in oplopende of aflopende volgorde rangschikken. Om dit te doen, knevel op **Sorteren inschakelen** -optie. U kunt bijvoorbeeld een subset beperken tot alleen de bovenste 50 profielen met het hoogste aankoopbedrag."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="Splitsen genereert complement"
>abstract="Zodra u alle subsets hebt gevormd, kunt u de resterende populatie selecteren die geen van de subsets aanpast en hen in een extra uitgaande overgang omvat. Om dit te doen, knevel op **Complement genereren** -optie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="Alle subsets in dezelfde tabel genereren"
>abstract="Schakel deze optie in en uit om alle subsets te groeperen in één uitvoerovergang."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="Lege overgang overslaan"
>abstract="Schakelen tussen **[!UICONTROL Skip empty transition]** optie aan om de outputovergang voor deze ondergroep onbruikbaar te maken als de inkomende bevolking leeg is."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="Overlappende uitvoerpopulaties inschakelen"
>abstract="De **[!UICONTROL Enable overlapping of output populations]** kunt u populaties beheren die tot verschillende subsets behoren. Wanneer het vakje niet wordt gecontroleerd, zorgt de gespleten activiteit ervoor een ontvanger niet in verscheidene outputovergangen kan aanwezig zijn, zelfs als het aan de criteria van verscheidene subsets voldoet. Deze worden als doel ingesteld op het eerste tabblad met overeenkomende criteria. Als het selectievakje is ingeschakeld, kunnen de ontvangers in verschillende subsets worden gevonden als ze voldoen aan hun filtercriteria. Adobe Campaign raadt aan exclusieve criteria te hanteren."

Voer de volgende stappen uit om de **Splitsen** activiteit:

1. Voeg een **Splitsen** activiteit aan uw samenstelling.

1. Het deelvenster voor activiteitenconfiguratie wordt geopend met een standaardsubset. Klik op de knop **Segment toevoegen** om zoveel subsets toe te voegen als gewenst om de binnenkomende populatie te segmenteren.

   >[!IMPORTANT]
   >
   >Wanneer de **Splitsen** de activiteit wordt uitgevoerd, wordt de populatie over de verschillende subsets verdeeld in de volgorde waarin ze aan de activiteit worden toegevoegd. Als de eerste subset bijvoorbeeld 70% van de oorspronkelijke populatie herstelt, past de volgende toegevoegde subset zijn selectiecriteria alleen toe op de resterende 30%, enzovoort.
   >
   >Voordat u de compositie start, moet u ervoor zorgen dat u de subsets in de gewenste volgorde hebt geplaatst. Hiervoor gebruikt u de pijlknoppen om de positie van een subset te wijzigen.

1. Nadat subsets zijn toegevoegd, toont de activiteit evenveel uitvoerovergangen als er subsets zijn. Wij adviseren sterk veranderend het etiket van elke ondergroep om hen in het samenstellingscanvas gemakkelijk te identificeren.

   ![](../assets/split.png)

1. Vorm hoe elke ondergroep de inkomende bevolking zou moeten filtreren. Ga als volgt te werk om dit te doen:

   1. Vouw de subset uit om de eigenschappen ervan weer te geven.

      ![](../assets/split-subset.png)

   1. Als u een filtervoorwaarde op de subset wilt toepassen, klikt u op **[!UICONTROL Create filter]** en vorm de gewenste het filtreren regel gebruikend de vraagmodeler. Neem bijvoorbeeld profielen op van de binnenkomende populatie waarvan het e-mailadres voorkomt in de database. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

   1. Als u het aantal profielen dat door de subset is geselecteerd, wilt beperken, schakelt u het **[!UICONTROL Enable limit]** en geeft het aantal of de percentages van de populatie aan die moeten worden opgenomen.

   1. Om een overgang onbruikbaar te maken als de inkomende bevolking leeg is, knevel **[!UICONTROL Skip empty transition]** optie ingeschakeld. Als geen profiel overeenkomt met de subset, gaat de compositie niet over naar de volgende activiteit.

   >[!NOTE]
   >
   >Wanneer u een populatielimiet voor een subset instelt, kunt u de geselecteerde profielen op basis van een specifiek profielkenmerk in oplopende of aflopende volgorde rangschikken. Om dit te doen, knevel op **[!UICONTROL Enable sorting]** -optie. U kunt bijvoorbeeld een subset beperken tot alleen de bovenste 50 profielen met het hoogste aankoopbedrag.

1. Zodra u alle subsets hebt gevormd, kunt u de resterende populatie selecteren die geen van de subsets aanpast en hen in een extra uitgaande overgang omvat. Om dit te doen, knevel op **[!UICONTROL Generate complement]** -optie.

   >[!NOTE]
   >
   >De **[!UICONTROL Generate all subsets in the same table]** kunt u alle subsets groeperen in één uitvoerovergang.

1. De **[!UICONTROL Enable overlapping of output populations]** Met deze optie kunt u populaties beheren die tot verschillende subsets behoren:

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
