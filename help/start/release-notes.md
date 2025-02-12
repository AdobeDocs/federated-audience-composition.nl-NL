---
title: Nieuw in Experience Platform Federated Audience Composition
description: Nieuwste updates en opmerkingen bij de release
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 81ac7595196aeff30f1d09d66779ca4392f7bb19
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 2%

---

# Aanvullende informatie {#rn-new}

[!DNL Federated Audience Composition] biedt voortdurend nieuwe functies, verbeteringen aan bestaande functies en foutoplossingen. Alle wijzigingen worden geconsolideerd in deze releaseopmerkingen. [!DNL Federated Audience Composition] is native gebaseerd op [!DNL Adobe Experience Platform] en neemt de nieuwste innovaties en verbeteringen over. Leer meer over deze veranderingen in [ de Nota&#39;s van de Versie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html) {target="_blank"}.


## Bijwerken februari &#39;25 {#fac-25-01}

Beginnende Maart versie, [!DNL Federated Audience Composition] zal beginnen de toegang van **Federated gegevensbeheer** en **Federated Composities** interfaces aan gebruiker af te dwingen die de **hebben gekregen leiden Federatieve Gegevens** toestemming.

We raden gebruikers aan contact op te nemen met de beheerders om deze machtiging aan hun rol toe te voegen en de gebruikersinterface van [!DNL Federated Audience Composition] te blijven gebruiken.

Leren hoe te om deze toestemming toe te wijzen, verwijs naar de [ gedetailleerde documentatie ](feature-access.md).

## Release van november 1924 {#fac-24-11}

### Verbeteringen {#fac-24-11-improvements}

Deze release gaat vergezeld van de onderstaande verbetering.

* **IP adres lijst van gewenste personen**

  Wanneer u een gefederaliseerde database toevoegt in de Adobe Experience Platform-gebruikersinterface, kunt u nu rechtstreeks de IP-adressen weergeven die zijn gekoppeld aan de instanties van de Federatieve compositie van het publiek. Dit laat u toe om deze IPs gemakkelijk te kopiëren en te machtigen om met uw gegevensbestand voor betere veiligheid en flexibiliteit te verbinden. [Meer informatie](../connections/connections.md)

## Release oktober 1924 {#fac-24-10}

>[!AVAILABILITY]
>
>Eerder beschikbaar voor een reeks organisaties (LA), is de Federated Audience Composition van Adobe Experience Platform nu beschikbaar aan alle gebruikers (GA). Deze invoegtoepassing wordt geactiveerd op basis van uw aanbieding en is alleen zichtbaar met de bijbehorende machtigingen. [Meer informatie](access-prerequisites.md)
>

### Compatibiliteit {#fac-24-10-compat}

Met deze nieuwe release is Federated Audience Composition nu compatibel met de hieronder vermelde systemen.

* **de steun van Gegevensbestanden**

  U kunt verbindingen aan gegevensbestanden van Gegevensbestanden door de Samenstelling van de Publiek van de Federatieve nu vestigen. [Meer informatie](../connections/federated-db.md#databricks)

* **Steun voor veilige toegang tot Snowflake door AWS PrivateLink**

  Beveiligde toegang tot uw externe Snowflake-gegevenspakhuis via een persoonlijke koppeling wordt nu ondersteund. Je Snowflake-account moet worden gehost op Amazon Web Services (AWS) en zich in dezelfde regio bevinden als de omgeving van je Federated Audience Composition. Neem contact op met uw Adobe-vertegenwoordiger voor hulp bij het instellen van veilige toegang tot uw Snowflake-account. [Meer informatie](../connections/federated-db.md#snowflake)

* **Amazon Redshift Serverless steun**

  Met deze nieuwe versie, steunt de Federatieve Samenstelling van het Publiek [ Amazon reshift Serverless ](https://aws.amazon.com/redshift/redshift-serverless/) {target="_blank"}.

### Verbeteringen {#fac-24-10-improvements}

Deze release bevat de verbeteringen die hieronder worden vermeld.

* **verfrist bestaande schema&#39;s**

  Wanneer een kolom wordt gecreeerd, gewijzigd of geschrapt in een gefedereerde gegevensbestand, kunt u de veranderingen nu ontdekken en toepassen door op de **[!UICONTROL Refresh schema]** knoop in het overeenkomstige schema te klikken. [Meer informatie](../customer/schemas.md#schema-refresh)

* **associeer een gegevensmodel met een nieuwe samenstelling**

  Wanneer u een compositie maakt, kunt u nu het gegevensmodel selecteren dat u eraan wilt koppelen. Met deze nieuwe optie, is de configuratie van uw activiteiten gemakkelijker aangezien slechts de lijsten van het bijbehorende gegevensmodel beschikbaar zijn. [Meer informatie](../compositions/create-composition.md)

## Release van 24 juli - Federated Audience Composition (LA) {#fac-la}

Federated Audience Composition is een add-on mogelijkheid waarmee bedrijven flexibele en uitgebreide toegang krijgen tot datacenters van bedrijven om een publiek samen te stellen met behulp van kritische bedrijfsgegevenssets en ervaringen op het gebied van energiemerken en actuele ervaringen. Met deze nieuwe benadering, als [ Adobe Real-Time Customer Data Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) {target="_blank"} en/of [ Adobe Journey Optimizer ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/ajo-home) {target="_blank"} gebruiker, kunt u publieksgegevens van uw bestaand gegevenspakhuis direct federeren om het publiek van Adobe Experience Platform in één systeem te verrijken.

Federated Audience Composition richt zich op de groeiende vraag naar markten voor ondernemingen die de flexibiliteit nodig hebben om een publiek samen te stellen met opslagdatasets. Hierdoor kunnen bedrijven de gegevensbeweging verminderen en tegelijkertijd kritieke publieksgegevens beschikbaar stellen aan marketingteams om te voldoen aan de vereisten voor gebruikssituaties en persoonlijke ervaringen. 

Leer meer over de mogelijkheden van de Samenstelling van de Federale Publiek in [ deze pagina ](get-started.md) en in [ Veelgestelde Vragen ](faq.md).

De gedetailleerde informatie over de eerste vereisten om tot Verbond van de Samenstellingen van het Publiek en de huidige guardrails toegang te hebben, verwijst naar [ deze pagina ](access-prerequisites.md).

