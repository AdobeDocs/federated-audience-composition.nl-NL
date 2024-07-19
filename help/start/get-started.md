---
title: Aan de slag met Federatieve Audience Composition
description: Leer wat Adobe Federated Audience Composition is en hoe u deze in Adobe Experience Platform kunt gebruiken
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: 33fbb9a2b2d3fa631619fa213d2dffafa153fa05
workflow-type: tm+mt
source-wordcount: '1328'
ht-degree: 1%

---


# Aan de slag met Federatieve Audience Composition {#gs-fac}

Federated Audience Composition is een Adobe Real-time Customer Data Platform- en Adobe Journey Optimizer-invoegtoepassing waarmee de klant het publiek van de externe gegevensopslagruimten kan opbouwen en verrijken en het publiek naar Adobe Experience Platform kan importeren.

Adobe Experience Platform Federated Audience Composition biedt een eenvoudige en krachtige oplossing om uw bedrijfsgegevenspakhuis direct binnen Adobe Real-time Customer Data Platform en/of Adobe Journey Optimizer aan te sluiten en query&#39;s uit te voeren op de tabellen van uw gegevenspakhuis.

Met Adobe Federated Audience Composition kunnen gebruikers van Adobe Experience Platform-apps toegang krijgen tot hun klantgegevens die zijn opgeslagen in hun gegevenspakhuizen en platforms voor cloudopslag, zoals Amazon Redshift, Azure synapse Analytics en meer. De gegevens van de klant kunnen in veelvoudige gegevenspakhuizen leven en zijn nu onmiddellijk toegankelijk, zonder replicatie. De gesteunde platforms zijn vermeld in [ deze pagina ](../connections/federated-db.md#supported-db).


## Gebruiksscenario’s {#rn-uc}

Door marketing-vriendschappelijke UI, creeer segmentregels die uw gegevenspaket voor een lijst van gebruikers vragen die voor een specifiek segment nodig voor marketing campagnes, toegang tot bestaand publiek in het pakhuis voor activering kwalificeren, of verrijken het publiek van Adobe Experience Platform met extra datapoints die in het pakhuis bestaan.

In deze versie zijn twee gebruiksgevallen beschikbaar: segmentatie van het publiek en verrijking van het publiek. De verrijking van het profiel zal in een toekomstige versie beschikbaar zijn.

![ diagram ](assets/fac-use-cases.png){zoomable="yes"}

## Belangrijkste stappen {#gs-steps}

Met Adobe Federated Audience Composition kunt u Adobe Experience Platform-soorten publiek rechtstreeks vanuit uw database maken en bijwerken, zonder dat er iets hoeft te worden ingevoerd.

![ diagram ](assets/steps-diagram.png){zoomable="yes"}

Belangrijkste stappen:

* **Configuratie**

   1. Connect Adobe Experience Platform en uw zakelijke gegevenspaket.
De volgende databases worden ondersteund: Snowflake, Google Big Query, Azure synapse, Redshift.
Leer meer in [ deze pagina ](../connections/federated-db.md)
   1. Maak schema&#39;s om te selecteren welke gegevens toegankelijk moeten zijn vanuit de gebruikersinterface.
Leer meer in [ deze pagina ](../customer/schemas.md)
   1. Maak koppelingen voor uw datamodel.
Leer meer in [ deze pagina ](../data-management/gs-models.md)

* **stel publiek** samen

   1. Ontwerp en voer composities uit om een publiek te maken.
Leer meer in [ deze pagina ](../compositions/gs-compositions.md)
   1. Bestaande doelgroepen bijwerken of opnieuw gebruiken via het Adobe Experience Platform Audience-portaal en -bestemmingen.
Leer meer in [ deze pagina ](../connections/destinations.md)

## Veelgestelde vragen {#faq}

Hieronder volgt een lijst met veelgestelde vragen over Federated Audience Composition. Een globale FAQ is ook beschikbaar voor de Dienst van de Segmentatie van Adobe Experience Platform in [ deze pagina ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq) {target="_blank"}.


+++Wat zijn de toestemmingen die worden vereist om tot de Federatieve Samenstelling van het Publiek toegang te hebben?

Er zijn geen specifieke toestemmingen voor de Samenstelling van het Publiek Federated. De enige vereiste om toegang tot dit vermogen te hebben is de Federated Audience Composition toe:voegen-op te kopen.

+++

+++Welke wolkenpakhuizen worden gesteund?

Voor deze release is Federated Audience Composition compatibel met:

* Amazon Redshift
* Azure synapse
* Google Big Query
* Snowflake
* Vertica Analytics

+++


+++Kunnen de veelvoudige gegevenspakhuizen in de zelfde samenstelling worden gevraagd?

Ja, kunnen de veelvoudige pakhuizen in de zelfde samenstelling worden gevraagd, en kunnen gegevens uit veelvoudige bronnen combineren.  Typisch, elke [ samenstellingsactiviteit ](../compositions/orchestrate-activities.md) (Vraag, Verrijking, Splitsen, enz.) Voert één of verscheidene SQL verklaringen afhankelijk van de activiteitenconfiguratie, de gerichte gegevensbestanden (er kunnen veelvoudige gevallen van gefederaliseerde gegevenstoegang zijn), en output van één of meerdere aanpasbare met het resultaat van de uitvoering uit. Deze werktabellen worden gebruikt als input voor opeenvolgende activiteiten.

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

Nee, Federated Audience Composition slaat alleen metagegevens (schemabeschrijvingen) op. Er worden geen klantgegevens doorgestuurd. De de uitvoerstroom van het Publiek wordt gedaan direct van het Portaal van het Publiek van Adobe Experience Platform (via [ Bestemming ](../connections/destinations.md)) aan het klantengegevensbestand. De creatie en updatestroom wordt gedaan direct van uw gegevensopslaggegevensbestand aan het Portaal van de Publiek van Adobe Experience Platform.

+++

+++slaat Federated Audience Composition een fysiek exemplaar van die lijst van mensen op om naar stroomafwaartse systemen te verzenden?

Federated Audience Composition bewaart geen fysieke kopie van de gegevens. De frequentie wordt gevormd in de samenstelling om te bepalen hoe vaak dit gegeven zal worden verfrist. De resulterende publieksgegevens worden niet langer door Adobe Experience Platform opgeslagen dan vereist door de gebruiksgevallen of handelingen van de klant.

Bijvoorbeeld:

* In het geval van een Segmentatie van het Publiek, wordt het publiek gecreeerd in uw pakhuis, en u kunt de Samenstelling van de Publiek van de Federatie voor extra samenstellingstaken en gegevensmanipulatie gebruiken alvorens het resulterende publiek en de bijbehorende attributen via het Portaal van de Publiek van Adobe Experience Platform te publiceren. De publieksdefinitie en de bijbehorende kenmerken komen naar Adobe Experience Platform.
De huidige gegevensvervaldatum voor extern gegenereerde doelgroepen is 30 dagen. Deze gegevensvervaldatum vermindert de hoeveelheid overtollige gegevens die binnen een organisatie worden opgeslagen. Nadat de gegevensvervalperiode overgaat, is de bijbehorende dataset nog zichtbaar binnen de datasetinventaris, maar u kunt niet het publiek activeren en de profieltelling zal als nul tonen. Leer meer in [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for) {target="_blank"}.

* In het geval van een Publiek Verrijking, is het uitgangspunt een bestaand publiek van Adobe Experience Platform. Hier kunnen twee scenario&#39;s worden bekeken:
   1. Breng extra attributen van de publiekslading van het gefedereerde gegevenspakhuis: in dit geval, zullen de extra attributen die worden toegevoegd als deel van deze publieksdefinitie overkomen. De vervaldatum van gegevens voor extern gegenereerde doelgroepen is gelijk aan de hierboven beschreven vervaldatum, 30 dagen.
   1. Verfijn het bestaande publiek van Adobe Experience Platform dat op extra attributen wordt gebaseerd die in uw gegevenspakje bestaan. U hebt bijvoorbeeld een publiek met klanten die de afgelopen twee maanden belangstelling hebben getoond voor een bepaald product op de website. U wilt dit publiek nu nemen en het verder segmenteren gebruikend de Samenstelling van de Publiek Federated om slechts klanten te omvatten die een hoge creditscore hebben. De creditscore wordt als gevoelig beschouwd en de individuele punten van de creditscore worden niet over van het gegevenspakhuis gekopieerd.
+++

+++Als de gegevens voor de Segmentatie van het Publiek en de gebruikspatronen van de Verrijking van de Publiek niet worden voortgeduurd, hoe wordt het tijdelijk opgeslagen?

De resulterende gegevens van het Publiek blijven niet eindeloos in Adobe Experience Platform of in Federated Audience Composition voortbestaan. Het wordt niet langer bewaard dan nodig is voor uw gebruiksgeval. De publiekskenmerken die als onderdeel van de payload voor het publiek worden geïntroduceerd, blijven alleen behouden als onderdeel van de publieksdefinitie. De duur van persistentie is gebaseerd op TTL voor om het even welk publiek, gebrek is 30 dagen.

+++

+++Kan ik een aangepast geüpload publiek verwijderen?

U kunt publiek schrappen dat niet in stroomafwaartse activering direct in de Portaal van het Publiek wordt gebruikt door eenvoudig schrapping van het actiemenu te selecteren. Leer meer in [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state) {target="_blank"}.

+++

+++Als ik gegevens uit veelvoudige bronnen combineer, hoe verbinden wij ons bij de gegevens? Gebruiken we de identiteitsdienst?

Nee, de identiteitsservice wordt niet gebruikt tijdens een samenstelling. De gegevens tussen de verschillende bronnen die in de compositie worden gebruikt, worden samengevoegd via door de gebruiker gedefinieerde logica (zoals uitgedrukt in het onderliggende model), bijvoorbeeld CRM-id, gebruikersaccountnummer enz. U moet de identiteit selecteren die als herkenningsteken in het publiek voor selectie in uw gegevenspakhuis wordt gebruikt. Voor een resulterend publiek van de Samenstelling van de Publiek Federated, moet u de identiteit namespace voor de identiteit in de resulterende dataset identificeren.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->

## Meer informatie {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Instellingen voor uitvoering"
>abstract="In deze sectie, kunt u montages met betrekking tot de uitvoering van het werkschema vormen, zoals het aantal dagen de samenstellingsgeschiedenis wordt gehouden."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Activiteit niet bewerkbaar"
>abstract="Wanneer de a **Vraag** of een **Verrijking** activiteit met extra gegevens in de console wordt gevormd, wordt het verrijkingsgegeven genomen en overgegaan in de uitgaande overgang, maar het kan niet worden uitgegeven."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Een koppeling maken"
>abstract="Geef de koppelingsinstellingen op."
