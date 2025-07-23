---
title: Nieuw in Experience Platform Federated Audience Composition
description: Nieuwste updates en opmerkingen bij de release
hide: true
hidefromtoc: true
exl-id: 23ea1a5d-a0e4-4f47-b0f8-56009bbc0a4a
source-git-commit: a568024516cec999e1e22b6f6deec926fe7083f8
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 3%

---

# Aanvullende informatie {#rn-new}

[!DNL Federated Audience Composition] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in deze releaseopmerkingen. [!DNL Federated Audience Composition] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target="_blank"}.

## Release juli 2025 {#fac-25-7}

Deze release bevat de volgende wijzigingen en verbeteringen:

* **de schakelaarbeschikbaarheid van Oracle**

  De Oracle-connector is nu beschikbaar voor gebruik met Federated Audience Composition.

* **de statusalarm van de Samenstelling**

  U kunt aan Alarm intekenen om voor het succes en de mislukkingen van uw samenstellingslooppas worden gealarmeerd.

## Release juni 2025 {#fac-25-6}

Deze release bevat de volgende verbeteringen:

* **Algemene Beschikbaarheid voor de Klanten van het Schild van de Gezondheidszorg van Adobe**

  Federated Audience Composition zal eind juni beschikbaar zijn voor klanten van het Adobe Healthcare Shield voor het creëren van publiek, verrijking en het gebruik van profielverrijking.

* **voorwerp-vlakke toegangsbeheer**

  Federated Audience Composition ondersteunt nu toegangsbeheer op objectniveau om toegangslabels toe te passen op de opgegeven composities.

* **Standaardrollen**

  U kunt één van de standaardrollen nu gebruiken om gebruikerstoestemmingen voor de toegang van de Samenstelling van de Federatieve Publiek te beheren.

* **Incrementele Updates in de gebruiksgevallen van de profielverrijking**

  De activiteit Profielen opslaan ondersteunt nu incrementele updates. Met stijgende updates, kunt u stijgende gegevens vragen en bijwerken terwijl het verrijken van profielen met gegevens van externe gegevenspakhuizen.

## Release van april 1925 {#fac-25-4}

### Verbeteringen {#fac-25-4-improvements}

Deze release bevat de onderstaande verbeteringen.

* **de mening van het ModelCanvas van Gegevens**

  De mening van het Canvas voor de sectie van de Modellen van Gegevens verbetert de ervaring door de visualisatie van gegevensmodellen en hun verbindingen in een canvaslay-out, naast de bestaande tabelmening toe te laten. [Meer informatie](../data-management/gs-models.md)

* **AI Medewerker**

  AI Assistant is een gebruikersinterfacefunctie waarmee u door Adobe-concepten kunt navigeren en deze kunt begrijpen en operationele inzichten voor uw specifieke omgeving kunt krijgen. Het is beschikbaar in verscheidene producten door Adobe Experience Cloud, met inbegrip van Federated Audience Composition. [Meer informatie](../start/audiences.md)

* **Naam van het Model van Gegevens**

  Van het menu van het publiek, toont het **Verdeelde samenstellingen** lusje nu de Naam van het Model van Gegevens in plaats van identiteitskaart, die helderheid en algemene bruikbaarheid verbetert.

* **Doelgroep**

  In het menu Publiek wordt nu de naam of het label van het geselecteerde gegevensmodel weergegeven wanneer een gebruiker een gegevensmodel selecteert dat niet aan het gegevensmodel is gekoppeld.

### Compatibiliteit {#fac-25-4-compat}

* **veilige verbinding van Snowflake**

  Met deze nieuwe release biedt Federated Audience Composition ondersteuning voor veilige privékoppelingsverbindingen met Amazon Redshift-databases die worden gehost op Microsoft Azure. [Meer informatie](../connections/federated-db.md#amazon-redshift)

## Release van maart 1925 {#fac-25-3}

### Verbeteringen {#fac-25-3-improvements}

Deze release bevat de onderstaande verbeteringen.

* {de toestemmingen van de Samenstelling van het 0} Federatieve publiek **&#x200B;**

  Beginnende Maart versie, [!DNL Federated Audience Composition] zal beginnen de toegang van **Federated gegevensbeheer** en **Federated Composities** interfaces aan gebruiker af te dwingen die de **hebben gekregen leiden Federatieve Gegevens** toestemming.

  We raden gebruikers aan contact op te nemen met de beheerders om deze machtiging aan hun rol toe te voegen en de gebruikersinterface van [!DNL Federated Audience Composition] te blijven gebruiken.

  Leren hoe te om deze toestemming toe te wijzen, verwijs naar de [ gedetailleerde documentatie ](/help/governance-privacy-security/access-control.md).

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)

* **AI Assistant**

    AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. [Learn more](ai-assistant.md)
-->


### Compatibiliteit {#fac-25-3-compat}

* **Verbinding van Gegevensbestanden**

  Met deze nieuwe versie, steunt de Federatieve Samenstelling van het Publiek nu privé verbindingsconnectiviteit voor Databricks gegevensbestandverbindingen.
Dit omvat veilige verbindingen met Databricks-databases die worden gehost op Amazon Web Services (AWS) via privékoppelingen en databases die worden gehost op Microsoft Azure via VPN. [Meer informatie](../connections/federated-db.md#databricks)

* **Steun voor B2B CDP Klanten**

  Federated Audience Composition is nu beschikbaar voor klanten van het Customer Data Platform (CDP) van de Klant van zaken-aan-Zaken (B2B) voor op mensen-gebaseerde publieksgebruiksgevallen.

* **veilige verbinding van Snowflake**

  Met deze nieuwe release biedt Federated Audience Composition ondersteuning voor veilige verbindingen met privékoppelingen naar Snowflake-databases die worden gehost op Microsoft Azure. [Meer informatie](../connections/federated-db.md#snowflake)

## Release van februari &#39;25 {#fac-25-2}

Deze release wordt geleverd met de onderstaande wijzigingen.

* **de Steun van de Stof van Microsoft**

  U kunt nu verbindingen met Microsoft Fabric-databases tot stand brengen via Federated Audience Composition. [Meer informatie](../connections/federated-db.md)

* **Amazon Redshift de steun van het Spectrum**

  Amazon Redshift-spectrum wordt nu ondersteund voor Amazon Redshift-databaseverbindingen. [Meer informatie](../connections/federated-db.md#amazon-redshift)

* **Verbeterde Ervaring van de Aanmaak van het Schema**

  Het proces voor het maken van schema&#39;s is verbeterd via een bijgewerkte gebruikersinterface die intuïtiever en eenvoudiger te navigeren is. Deze verbeteringen bieden gegevensgebruikers een vloeiender en efficiëntere manier om gegevensmodellen te ontwikkelen. [Meer informatie](../customer/schemas.md)

* **Steun van de Verrijking van de Publiek voor Gegevensbestanden**

  U kunt Gegevensbestanden in de Gelezen stroom van het Publiek nu gebruiken, toelatend activiteit voor gegevensbestanden Databricks en toestaand het om als nieuwe bestemming worden opgesteld. [Meer informatie](../connections/destinations.md)

## Release van november 1924 {#fac-24-11}

### Verbeteringen {#fac-24-11-improvements}

Deze release gaat vergezeld van de onderstaande verbetering.

* **IP adres lijst van gewenste personen**

  Wanneer u een gefederaliseerde database toevoegt in de Adobe Experience Platform-gebruikersinterface, kunt u nu rechtstreeks de IP-adressen weergeven die zijn gekoppeld aan de instanties van de Federatieve compositie van het publiek. Dit laat u toe om deze IPs gemakkelijk te kopiëren en te machtigen om met uw gegevensbestand voor betere veiligheid en flexibiliteit te verbinden. [Meer informatie](../connections/connections.md)

## Release oktober 1924 {#fac-24-10}

>[!AVAILABILITY]
>
>Eerder beschikbaar voor een reeks organisaties (LA), is de Federated Audience Composition van Adobe Experience Platform nu beschikbaar aan alle gebruikers (GA). Deze mogelijkheid wordt geactiveerd op basis van uw aanbieding en is alleen zichtbaar met de bijbehorende machtigingen. [Meer informatie](access-prerequisites.md)
>

### Compatibiliteit {#fac-24-10-compat}

Met deze nieuwe release is Federated Audience Composition nu compatibel met de hieronder vermelde systemen.

* **de steun van Gegevensbestanden**

  U kunt verbindingen aan gegevensbestanden van Gegevensbestanden door de Samenstelling van de Publiek van de Federatieve nu vestigen. [Meer informatie](../connections/federated-db.md#databricks)

* **Steun voor veilige toegang tot Snowflake door AWS PrivateLink**

  Beveiligde toegang tot uw externe Snowflake-gegevenspakhuis via een persoonlijke koppeling wordt nu ondersteund. Je Snowflake-account moet worden gehost op Amazon Web Services (AWS) en zich in dezelfde regio bevinden als de omgeving van je Federated Audience Composition. Neem contact op met uw Adobe-vertegenwoordiger voor hulp bij het instellen van veilige toegang tot uw Snowflake-account. [Meer informatie](../connections/federated-db.md#snowflake)

* **Amazon Redshift Serverless steun**

  Met deze nieuwe versie, steunt de Federatieve Samenstelling van het Publiek [ Amazon opnieuw verschuift Serverless ](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Verbeteringen {#fac-24-10-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

* **verfrist bestaande schema&#39;s**

  Wanneer een kolom wordt gecreeerd, gewijzigd of geschrapt in een gefedereerde gegevensbestand, kunt u de veranderingen nu ontdekken en toepassen door op de **[!UICONTROL Refresh schema]** knoop in het overeenkomstige schema te klikken. [Meer informatie](../customer/schemas.md#schema-refresh)

* **associeer een gegevensmodel met een nieuwe samenstelling**

  Wanneer u een compositie maakt, kunt u nu het gegevensmodel selecteren dat u eraan wilt koppelen. Met deze nieuwe optie, is de configuratie van uw activiteiten gemakkelijker aangezien slechts de lijsten van het bijbehorende gegevensmodel beschikbaar zijn. [Meer informatie](../compositions/create-composition.md)

## Release van 24 juli - Federated Audience Composition (LA) {#fac-la}

De Federated Audience Composition voorziet ondernemingen van flexibele en uitgebreide toegang tot ondernemingsgegevensopslagplaatsen om publiek samen te stellen gebruikend kritieke ondernemingsdatasets en macht merkgeinitieerde en in-de-huidige ervaringen. Met deze nieuwe benadering, als [ Adobe Real-Time Customer Data Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home){target="_blank"} en/of [ Adobe Journey Optimizer ](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/ajo-home){target="_blank"} gebruiker, kunt u publieksgegevens van uw bestaand gegevenspakhuis direct federeren om het publiek van Adobe Experience Platform in één systeem te verrijken.

Federated Audience Composition richt zich op de groeiende vraag naar markten voor ondernemingen die de flexibiliteit nodig hebben om een publiek samen te stellen met opslagdatasets. Hierdoor kunnen bedrijven de gegevensbeweging verminderen en tegelijkertijd kritieke publieksgegevens beschikbaar stellen aan marketingteams om te voldoen aan de vereisten voor gebruikssituaties en persoonlijke ervaringen.

Leer meer over de mogelijkheden van de Samenstelling van de Federale Publiek op [ deze pagina ](get-started.md) en in [ Veelgestelde Vragen ](faq.md).

De gedetailleerde informatie over de eerste vereisten om tot Verbond van de Samenstellingen van het Publiek en de huidige guardrails toegang te hebben, verwijst naar [ deze pagina ](access-prerequisites.md).
