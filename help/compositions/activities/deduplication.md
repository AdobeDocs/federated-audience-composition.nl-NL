---
audience: end-user
title: De deduplicatieactiviteit gebruiken
description: Leer hoe u de deduplicatieactiviteit gebruikt
source-git-commit: 56d9cc6489557c12761cd3fe8f3b7a61a71ece21
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 19%

---


# Deduplicatie {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Velden om duplicaten te identificeren"
>abstract="In de **Gebieden om duplicaten** sectie te identificeren, klik **voegt attribuut** knoop toe om de gebieden te specificeren waarvoor de identieke waarden toestaan om worden geïdentificeerd de duplicaten, zoals: e-mailadres, voornaam, achternaam, enz. In de volgorde van de velden kunt u opgeven welke velden eerst moeten worden verwerkt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Deduplicatieactiviteit"
>abstract="De **Deduplicatie** activiteit staat u toe om duplicaten in de resultaten van de binnenkomende activiteiten te schrappen. Het wordt meestal gebruikt na doelgerichte activiteiten en vóór activiteiten die het gebruik van gerichte gegevens mogelijk maken."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Om dit te doen, op **van een knevel voorzien produceer complement** optie"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Instellingen voor deduplicatie"
>abstract="Als u duplicaten van binnenkomende gegevens wilt verwijderen, definieert u de deduplicatiemethode in de onderstaande velden. Standaard wordt slechts één record bewaard. U moet ook de deduplicatiemodus selecteren op basis van een expressie of een kenmerk. Standaard wordt de record die buiten de duplicaten moet blijven, willekeurig geselecteerd."

De **Deduplicatie** activiteit staat u toe om duplicaten in het resultaat(en) van de binnenkomende activiteiten, bijvoorbeeld gedupliceerde profielen in de ontvankelijke lijst te schrappen. De **Deduplicatie** activiteit wordt over het algemeen gebruikt na het richten van activiteiten, en vóór activiteiten die het gebruik van gerichte gegevens toestaan.

## De deduplicatieactiviteit configureren{#deduplication-configuration}

Voer de volgende stappen uit om de **Deduplication** -activiteit te configureren:

1. Voeg de activiteit van de a **Deduplicatie** aan uw samenstelling toe.

1. Als de activiteit verscheidene binnenkomende overgangen heeft, selecteer de overgang om deduplicatie uit te voeren van de **[!UICONTROL Primary set]** drop-down lijst

1. In de **Gebieden om duplicaten** sectie te identificeren, klik **voegt attribuut** knoop toe om de gebieden te specificeren waarvoor de identieke waarden toestaan om worden geïdentificeerd de duplicaten, zoals: e-mailadres, voornaam, achternaam, enz. In de volgorde van de velden kunt u opgeven welke velden eerst moeten worden verwerkt.

   ![](../assets/deduplication.png)

1. In de **montages van de Deduplicatie** sectie, selecteer het aantal unieke **Duplicaten om** te houden. De standaardwaarde voor dit veld is 1. Met de waarde 0 kunt u alle duplicaten behouden.

   Stel bijvoorbeeld dat records A en B worden beschouwd als duplicaten van record Y en dat een record C wordt beschouwd als duplicaat van record Z:

   * Als de waarde van het veld 1 is: alleen de records Y en Z blijven behouden.
   * Als de waarde van het veld 0 is: alle records blijven behouden.
   * Als de waarde van het veld 2 is: de records C en Z blijven behouden en twee records van A, B en Y blijven behouden, bij toeval of afhankelijk van de daarna geselecteerde deduplicatiemethode.

1. Selecteer de **methode van de Deduplicatie** aan gebruik:

   * **Willekeurige selectie**: Selecteert willekeurig het verslag dat uit de duplicaten moet worden gehouden.
   * **Gebruikend een uitdrukking**: Behoud de verslagen waarin de waarde van de ingevoerde uitdrukking de kleinste of grootste is.
   * **Niet-lege waarden**: houd de verslagen waarvoor de uitdrukking niet leeg is.
   * **na een lijst van waarden**: Bepaal een waardeprioriteit voor één of meerdere gebieden. Om de waarden te bepalen, klik **Attribuut** om een gebied te selecteren of een uitdrukking tot stand te brengen, dan voeg de waarde(n) in de aangewezen lijst toe. Om een nieuw gebied te bepalen, klik **toevoegen knoop** boven de lijst van waarden wordt gevestigd die.

1. Controleer **aanvult** optie als u wenst om de resterende bevolking uit te buiten. Het complement bestaat uit alle duplicaten. Er wordt dan een aanvullende overgang toegevoegd aan de activiteit.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
