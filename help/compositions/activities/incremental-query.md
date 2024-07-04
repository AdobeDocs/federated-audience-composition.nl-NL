---
audience: end-user
title: De incrementele queryactiviteit gebruiken
description: Leer hoe te om de Incrementele vraagactiviteit te gebruiken
hide: true
hidefromtoc: true
source-git-commit: 13e7e75fe1dc175fce9464fa58c7a50b5e6107d4
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 18%

---

# Incrementele query {#incremental-query}

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Incrementele query"
>abstract="De **Incrementele query** Met de activiteit kunt u query&#39;s uitvoeren op de database met behulp van de Query-modelfunctie. Telkens wanneer deze activiteit wordt uitgevoerd, worden de resultaten van de vorige uitvoeringen uitgesloten. Zo kunt u doelgericht alleen nieuwe elementen benaderen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Incrementele querygeschiedenis"
>abstract="Incrementele querygeschiedenis"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Incrementele query verwerkte gegevens"
>abstract="Incrementele query verwerkte gegevens"

De **Incrementele query** de activiteit staat u toe om het gegevensbestand op een geplande basis te vragen. Telkens wanneer deze activiteit wordt uitgevoerd, worden de resultaten van de vorige uitvoeringen uitgesloten. Zo kunt u doelgericht alleen nieuwe elementen benaderen.

De activiteit **[!UICONTROL Incremental query]** kan voor diverse doeleinden worden gebruikt:

* Individuele gebruikers segmenteren om het doel van een bericht, doelgroep, enz te bepalen.
* Gegevens exporteren. U kunt de activiteit bijvoorbeeld gebruiken om regelmatig nieuwe aanmeldbestanden te exporteren. Het kan nuttig zijn als u uw logboekgegevens in externe rapportering of hulpmiddelen wilt gebruiken BI.

De bevolking die reeds het doelwit was van eerdere executies, wordt in de samenstelling opgeslagen. Dit betekent dat twee samenstellingen die vanaf dezelfde sjabloon zijn gestart, niet hetzelfde logbestand delen. Nochtans, gebruiken twee taken die op de zelfde stijgende vraag in de zelfde samenstelling worden gebaseerd het zelfde logboek.

Als het resultaat van een stijgende vraag aan 0 tijdens één van zijn uitvoeringen gelijk is, wordt de samenstelling gepauzeerd tot de volgende geprogrammeerde uitvoering van de vraag. De overgangen en de activiteiten die volgen op de stijgende vraag worden daarom niet verwerkt vóór de volgende uitvoering.

## Vorm de Incrementele vraagactiviteit {#incremental-query-configuration}

Voer de volgende stappen uit om de **Incrementele query** activiteit:

1. Een **Incrementele query** activiteit in uw samenstelling.

1. In de **[!UICONTROL Audience]** in, kiest u **Doeldimensie** klik vervolgens op **[!UICONTROL Continue]**.

   Met de doeldimensie kunt u de doelgroep van de actie definiëren: ontvangers, begunstigden van contracten, exploitant, abonnees, enz. Standaard is het doel geselecteerd bij de ontvangers. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. Gebruik de vraagmodeler om uw vraag te bepalen, de zelfde manier u creeert een publiek wanneer het ontwerpen van een nieuwe e-mail. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. In de **[!UICONTROL Processed data]** selecteert u de incrementele modus die u wilt gebruiken:

   * **[!UICONTROL Exclude results of previous execution]**: Elke keer dat de activiteit wordt uitgevoerd, worden de resultaten van de vorige uitvoeringen uitgesloten.

     Records die al in eerdere uitvoeringen zijn bedoeld, kunnen worden geregistreerd gedurende een maximumaantal dagen vanaf de dag waarop ze als doel zijn gebruikt. Om dit te doen, gebruik **[!UICONTROL History in days]** veld. Als deze waarde nul is, worden de ontvangers nooit gezuiverd van het logboek.

   * **[!UICONTROL Use a date field]**: Met deze optie kunt u resultaten uitsluiten van eerdere uitvoeringen op basis van een bepaald datumveld. Hiervoor kiest u het gewenste datumveld in de lijst met kenmerken die beschikbaar zijn voor de geselecteerde doeldimensie. Bij de volgende uitvoeringen van de samenstelling, slechts zullen de gegevens die na de laatste uitvoeringsdatum zijn gewijzigd of gecreeerd worden teruggewonnen.

     Na de eerste uitvoering van de compositie **[!UICONTROL Last execution date]** wordt beschikbaar. Het specificeert de datum die voor de volgende uitvoering zal worden gebruikt, en automatisch bijgewerkt telkens als de samenstelling wordt uitgevoerd. U kunt deze waarde ook overschrijven door handmatig een nieuwe waarde in te voeren die beter aan uw behoeften voldoet.

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
