---
title: Veelgestelde vragen
description: Veelgestelde vragen over Adobe Experience Platform Federated Audience Composition
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 0b8781b5b33d96db7d7f23b3c399942b9cfe901f
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# Veelgestelde vragen {#faq}

Hieronder volgt een lijst met veelgestelde vragen over Adobe Experience Platform Federated Audience Composition. Een globale FAQ is ook beschikbaar voor de Dienst van de Segmentatie van Adobe Experience Platform in [ deze pagina ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq) {target="_blank"}.


+++Wat zijn de toestemmingen die worden vereist om tot de Federatieve Samenstelling van het Publiek toegang te hebben?

Voor Federated Audience Composition zijn Adobe Real-Time Customer Data Platform- en Adobe Journey Optimizer Prime- of Ultimate-pakketten vereist. U moet ook Federated Audience Composition hebben aangeschaft.

Als u Federated Audience Composition wilt gebruiken, moet elke gebruiker worden toegevoegd aan een specifiek profiel dat voor elke sandbox is gemaakt. Voor meer informatie, verwijs naar de ](access-prerequisites.md) pagina van de Samenstelling van het Publiek van de 1} Verbond van de Toegang.[

+++

+++Welke wolkenpakhuizen worden gesteund?

De lijst van systemen die met de Federatieve Samenstelling van het Publiek worden gesteund is beschikbaar in [ deze pagina ](../start/access-prerequisites.md#supported-systems).

+++


+++Kunnen de veelvoudige gegevenspakhuizen in de zelfde samenstelling worden gevraagd?

Ja, kunnen de veelvoudige pakhuizen in de zelfde samenstelling worden gevraagd, en kunnen gegevens uit veelvoudige bronnen combineren.  Typisch, voert elke [ samenstellingsactiviteit ](../compositions/orchestrate-activities.md) (Vraag, Verrijking, Gesplitst, enz.) één of verscheidene SQL verklaringen afhankelijk van de activiteitenconfiguratie uit, de gerichte gegevensbestanden (er kunnen veelvoudige gevallen van gefederaliseerde gegevenstoegang zijn), en output van één of meerdere werktafels met het resultaat van de uitvoering. Deze werktabellen worden gebruikt als input voor opeenvolgende activiteiten.

+++

+++ Kan ik tot mijn volledige gegevensbestand toegang hebben gebruikend Federated Samenstelling van het Publiek?

Nr, is het aan u om toegang tot een specifiek of gedeeld gegevensbestand/schema te vormen. Wij adviseren u om een specifiek schema voor de Samenstelling van het Federale Publiek, en exemplaar/aandeel bedrijfsgevallenreeksen slechts tot stand te brengen.
+++

+++Heb ik toegang tot alle lijsten in het specifieke schema?

Ja, zodra verbonden, Federated Audience Composition kan worden gebruikt om alle lijsten te ontdekken die op aanvankelijk bepaalde rechten worden gebaseerd, dan kunt u de visuele schemaredacteur gebruiken aan:

* Kolommen en primaire sleutels uit uw tabellen detecteren
* Maak vriendelijke labels voor deze tabellen
* Maak vriendelijke labels voor elke kolom
* Overbodige kolommen verbergen
* De tabelbeschrijving opslaan
+++

+++Is er tijdelijke opslag in de Federated Audience Composition?

Nee, Federated Audience Composition slaat alleen metagegevens (schemabeschrijvingen) op. Er worden geen klantgegevens doorgestuurd. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++slaat Federated Audience Composition een fysiek exemplaar van die lijst van mensen op om naar stroomafwaartse systemen te verzenden?

Federated Audience Composition bewaart geen fysieke kopie van de gegevens. De frequentie wordt gevormd in de samenstelling om te bepalen hoe vaak dit gegeven zal worden verfrist. De resulterende publieksgegevens worden niet langer door Adobe Experience Platform opgeslagen dan vereist door de gebruiksgevallen of handelingen van de klant.

Bijvoorbeeld:

* In het geval van een Making van het Publiek, wordt het publiek gecreeerd in uw pakhuis, en u kunt de Samenstelling van de Publiek van de Federatie voor extra samenstellingstaken en gegevensmanipulatie gebruiken alvorens het resulterende publiek en de bijbehorende attributen via het Portaal van de Publiek van Adobe Experience Platform te publiceren. De publieksdefinitie en de bijbehorende kenmerken komen naar Adobe Experience Platform.
De huidige gegevensvervaldatum voor extern gegenereerde doelgroepen is 30 dagen. Deze gegevensvervaldatum vermindert de hoeveelheid overtollige gegevens die binnen een organisatie worden opgeslagen. Nadat de gegevensvervalperiode overgaat, is de bijbehorende dataset nog zichtbaar binnen de datasetinventaris, maar u kunt niet het publiek activeren en de profieltelling zal als nul tonen. Leer meer in [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for) {target="_blank"}.

* In het geval van een Publiek Verrijking, is het uitgangspunt een bestaand publiek van Adobe Experience Platform. Hier kunnen twee scenario&#39;s worden bekeken:
   1. Breng extra attributen van de publiekslading van het gefedereerde gegevenspakhuis: in dit geval, zullen de extra attributen die worden toegevoegd als deel van deze publieksdefinitie overkomen. De vervaldatum van gegevens voor extern gegenereerde doelgroepen is gelijk aan de hierboven beschreven vervaldatum, 30 dagen.
   1. Verfijn het bestaande publiek van Adobe Experience Platform dat op extra attributen wordt gebaseerd die in uw gegevenspakje bestaan. <!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Als de gegevens voor de Aanmaak van de Publiek en de Verrijking van de Publiek gebruikspatronen niet worden voortgeduurd, hoe wordt het tijdelijk opgeslagen?

De resulterende gegevens van het Publiek blijven niet eindeloos in Adobe Experience Platform of in Federated Audience Composition voortbestaan. Het wordt niet langer bewaard dan nodig is voor uw gebruiksgeval. De publiekskenmerken die als onderdeel van de payload voor het publiek worden geïntroduceerd, blijven alleen behouden als onderdeel van de publieksdefinitie. De duur van persistentie is gebaseerd op TTL voor om het even welk publiek, gebrek is 30 dagen.

+++

+++Kan ik een publiek verwijderen?

Nee, in de huidige versie kunt u geen publiek met een federatieve doelgroep verwijderen.

+++

+++Als ik gegevens uit veelvoudige bronnen combineer, hoe verbinden wij ons bij de gegevens? Gebruiken we de identiteitsdienst?

Nee, de identiteitsservice wordt niet gebruikt tijdens een samenstelling. De gegevens tussen de verschillende bronnen die in de compositie worden gebruikt, worden samengevoegd via door de gebruiker gedefinieerde logica (zoals uitgedrukt in het onderliggende model), bijvoorbeeld CRM-id, gebruikersaccountnummer enz. U moet de identiteit selecteren die als herkenningsteken in het publiek voor selectie in uw gegevenspakhuis wordt gebruikt. Voor een resulterend publiek van de Samenstelling van de Publiek Federated, moet u de identiteit namespace voor de identiteit in de resulterende dataset identificeren.

+++
<!--
+++How are customer consent preferences honored for externally generated audiences that are imported into Federated Audience Composition?

As customer data is captured from multiple channels, identity stitching and merge policies allow this data to be consolidated in a single Real-Time Customer Profile. Information on the customers' consent preferences are stored and evaluated at the profile level.

Downstream Real-Time CDP and Journey Optimizer destinations check each profile for consent preferences prior to activation. Each profile's consent information is compared against consent requirements for a particular destination. If the profile does not satisfy the requirements, that profile is not sent to a destination.

When an external audience is ingested into Federated Audience Composition, it is reconciliated with existing profiles using a primary ID such as email or ECID. As a result, the existing consent policies will remain in force throughout activation.

>[!NOTE]
>
>Since the payload variables are not stored in the profile but in the data lake, you should not include consent information in externally generated audiences. Instead, use other Adobe Experience Platform ingestion channels where profile data is imported.

+++
-->
