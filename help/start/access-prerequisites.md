---
title: Vereisten en instructies voor Federatieve Audience Composition
description: Ervaar vereisten, toestemmingen, en gidsen voor de Samenstelling van de Publiek van de Federatieve
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 5%

---

# Vereisten en geleiders {#fac-access}

De federated Samenstelling van het Publiek vereist Adobe Real-Time Customer Data Platform en/of Adobe Journey Optimizer **Prime** of **Ultimate** pakketten. Om toegang te krijgen tot deze mogelijkheid, moet u de add-on van de Samenstelling van de Federatieve Publiek hebben gekocht.

>[!AVAILABILITY]
>
>Nadat u het welkomstbericht van Adobe hebt ontvangen, kan het nog een paar uur duren voordat de interface is bijgewerkt en er functies beschikbaar zijn voor u.

## Ondersteunde systemen {#supported-systems}

De Federatieve Samenstelling van de Publiek steunt de volgende wolkenpakhuizen:

* Amazon Redshift
* Azure Synapse
* Databricks
* Google Big Query
* Snowflake
* Vertica Analytics
* Microsoft Fabric

Leer hoe te om een verbinding met deze systemen op [ tot stand te brengen deze pagina ](../connections/connections.md).

## Sandboxes

Wanneer u Federated Audience Composition aanschaft, hebt u recht op twee sandboxen. Neem contact op met uw Adobe-vertegenwoordiger voor aanvullende aanvragen voor sandboxprovisioning.

Voer de onderstaande stappen uit om de lijst met actieve sandboxen voor Federatieve Audience weer te geven:

1. Via Federated Audience Composition opent u het menu **[!UICONTROL License usage]** onder **[!UICONTROL Administration]** .

1. Klik op het pictogram ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) van **[!UICONTROL Total volume of data egress]** om toegang te krijgen tot de eigenschappen van uw sandbox.

   ![](assets/sandbox_1.png)

1. Informatie over de sandbox wordt weergegeven in de keuzelijst Eigenschappen.

   ![](assets/sandbox_2.png)

## Machtigingen {#permissions}

Als u Federated Audience Composition wilt openen, moeten gebruikers worden toegevoegd aan het sandbox-specifieke productprofiel dat bij de aankoop wordt gemaakt en moet aan hen de machtiging **[!UICONTROL Manage Federated Data]** worden toegewezen. [Meer informatie](feature-access.md)

## IP-aanbieding toestaan {#ip}

Om Federated Audience Composition veilig toe te laten om tot uw gegevensbestanden toegang te hebben, moet u de IP adressen van de servers van de Samenstelling van de Federatieve Publiek machtigen die tot hen zullen toegang hebben. Deze IP-adressen worden weergegeven wanneer u een gefedereerde database toevoegt in de gebruikersinterface van Adobe Experience Platform. [Meer informatie](../connections/connections.md)

Voeg deze IP adressen aan uw lijst van gewenste personen toe om toegang voor Federatieve Samenstelling van het Publiek te verlenen.

## Afbeeldingen en beperkingen {#fac-guardrails}

* De Federatieve Samenstelling van het Publiek is momenteel niet beschikbaar aan klanten [ die gezondheidsgegevens ](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"} opnemen. [Meer informatie](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* De rechten, de productbeperkingen en de prestatiegaranties die in de [ documentatie van Adobe Real-Time Customer Data Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} worden vermeld zijn op de Federatieve Samenstelling van het Publiek van toepassing.

<!--* Federated Audience Composition supports the export of large audiences, with file sizes greater than 1 GB. For optimal performance, the maximum recommended file size is up to 20 GB.
-->

