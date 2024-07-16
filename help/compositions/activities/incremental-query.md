---
audience: end-user
title: De incrementele queryactiviteit gebruiken
description: Leer hoe te om de Incrementele vraagactiviteit te gebruiken
hide: true
hidefromtoc: true
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 17%

---

# Incrementele query {#incremental-query}

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Incrementele query"
>abstract="De **Incrementele vraag** activiteit staat u toe om het gegevensbestand te vragen gebruikend de modelleerling van de Vraag. Telkens wanneer deze activiteit wordt uitgevoerd, worden de resultaten van de vorige uitvoeringen uitgesloten. Zo kunt u doelgericht alleen nieuwe elementen benaderen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Incrementele querygeschiedenis"
>abstract="Incrementele querygeschiedenis"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Incrementele query verwerkte gegevens"
>abstract="Incrementele query verwerkte gegevens"

De **Incrementele vraag** activiteit staat u toe om het gegevensbestand op een geplande basis te vragen. Telkens wanneer deze activiteit wordt uitgevoerd, worden de resultaten van de vorige uitvoeringen uitgesloten. Zo kunt u doelgericht alleen nieuwe elementen benaderen.

De activiteit **[!UICONTROL Incremental query]** kan voor diverse doeleinden worden gebruikt:

* Individuele gebruikers segmenteren om het doel van een bericht, doelgroep, enz te bepalen.
* Gegevens exporteren. U kunt de activiteit bijvoorbeeld gebruiken om regelmatig nieuwe aanmeldbestanden te exporteren. Het kan nuttig zijn als u uw logboekgegevens in externe rapportering of hulpmiddelen wilt gebruiken BI.

De bevolking die reeds het doelwit was van eerdere executies, wordt in de samenstelling opgeslagen. Dit betekent dat twee samenstellingen die vanaf dezelfde sjabloon zijn gestart, niet hetzelfde logbestand delen. Nochtans, gebruiken twee taken die op de zelfde stijgende vraag in de zelfde samenstelling worden gebaseerd het zelfde logboek.

Als het resultaat van een stijgende vraag aan 0 tijdens één van zijn uitvoeringen gelijk is, wordt de samenstelling gepauzeerd tot de volgende geprogrammeerde uitvoering van de vraag. De overgangen en de activiteiten die volgen op de stijgende vraag worden daarom niet verwerkt vóór de volgende uitvoering.

## Vorm de Incrementele vraagactiviteit {#incremental-query-configuration}

Volg deze stappen om de **Incrementele vraag** activiteit te vormen:

1. Voeg een **Incrementele vraag** activiteit in uw samenstelling toe.

1. In de **[!UICONTROL Audience]** sectie, kies de **Doelende afmeting** dan klik **[!UICONTROL Continue]**.

   Met de doeldimensie kunt u de doelgroep van de actie definiëren: ontvangers, begunstigden van contracten, exploitant, abonnees, enz. Standaard is het doel geselecteerd bij de ontvangers. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. Gebruik de vraagmodeler om uw vraag te bepalen, de zelfde manier u creeert een publiek wanneer het ontwerpen van een nieuwe e-mail. [ Leer hoe te met de vraagmodelaar ](../../query/query-modeler-overview.md) te werken

1. Selecteer in de sectie **[!UICONTROL Processed data]** de incrementele modus die u wilt gebruiken:

   * **[!UICONTROL Exclude results of previous execution]**: Telkens wanneer de activiteit wordt uitgevoerd, worden de resultaten van de vorige uitvoeringen uitgesloten.

     Records die al in eerdere uitvoeringen zijn bedoeld, kunnen worden geregistreerd gedurende een maximumaantal dagen vanaf de dag waarop ze als doel zijn gebruikt. Gebruik hiervoor het veld **[!UICONTROL History in days]** . Als deze waarde nul is, worden de ontvangers nooit gezuiverd van het logboek.

   * **[!UICONTROL Use a date field]**: met deze optie kunt u resultaten uitsluiten van vorige uitvoeringen op basis van een bepaald datumveld. Hiervoor kiest u het gewenste datumveld in de lijst met kenmerken die beschikbaar zijn voor de geselecteerde doeldimensie. Bij de volgende uitvoeringen van de samenstelling, slechts zullen de gegevens die na de laatste uitvoeringsdatum zijn gewijzigd of gecreeerd worden teruggewonnen.

     Na de eerste uitvoering van de compositie wordt het veld **[!UICONTROL Last execution date]** beschikbaar. Het specificeert de datum die voor de volgende uitvoering zal worden gebruikt, en automatisch bijgewerkt telkens als de samenstelling wordt uitgevoerd. U kunt deze waarde ook overschrijven door handmatig een nieuwe waarde in te voeren die beter aan uw behoeften voldoet.

   >[!NOTE]
   >
   >In de modus **[!UICONTROL Use a date field]** is meer flexibiliteit mogelijk, afhankelijk van het datumveld dat is geselecteerd. Als het opgegeven veld bijvoorbeeld overeenkomt met een wijzigingsdatum, kunt u in de modus Datumveld gegevens ophalen die onlangs zijn bijgewerkt, terwijl in de andere modus alleen opnamen worden uitgesloten die in een vorige uitvoering al als doel waren ingesteld, zelfs als deze zijn gewijzigd sinds de laatste uitvoering van de compositie.

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
