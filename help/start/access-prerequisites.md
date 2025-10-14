---
title: Vereisten en instructies voor Federatieve Audience Composition
description: Ervaar vereisten, toestemmingen, en gidsen voor de Samenstelling van de Publiek van de Federatieve
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: c133ddb2b1d2a75e7f9614d7623fad63aa24eb55
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 3%

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
* Google BigQuery
* Snowflake
* Vertica Analytics
* Microsoft Fabric

Leer hoe te om een verbinding met deze systemen op [&#x200B; tot stand te brengen deze pagina &#x200B;](../connections/home.md).

## Sandboxes

Wanneer u Federated Audience Composition aanschaft, hebt u recht op twee sandboxen. Neem contact op met uw Adobe-vertegenwoordiger voor aanvullende aanvragen voor sandboxprovisioning.

Voer de onderstaande stappen uit om de lijst met actieve sandboxen voor Federatieve Audience weer te geven:

1. Via Federated Audience Composition opent u het menu **[!UICONTROL License usage]** onder **[!UICONTROL Administration]** .

1. Klik op het pictogram ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) van **[!UICONTROL Total volume of data egress]** om toegang te krijgen tot de eigenschappen van uw sandbox.

   ![](assets/sandbox_1.png)

1. Informatie over de sandbox wordt weergegeven in de keuzelijst Eigenschappen.

   ![](assets/sandbox_2.png)

## Machtigingen {#permissions}

Als u Federated Audience Composition wilt openen, moeten gebruikers worden toegevoegd aan het sandbox-specifieke productprofiel dat bij de aankoop wordt gemaakt en moet aan hen de machtiging **[!UICONTROL Manage Federated Data]** worden toegewezen. [Meer informatie](/help/governance-privacy-security/access-control.md)

## IP-aanbieding toestaan {#ip}

Om Federated Audience Composition veilig toe te laten om tot uw gegevensbestanden toegang te hebben, moet u de IP adressen van de servers van de Samenstelling van de Federatieve Publiek machtigen die tot hen zullen toegang hebben. Deze IP-adressen worden weergegeven wanneer u een gefedereerde database toevoegt in de gebruikersinterface van Adobe Experience Platform. [Meer informatie](../connections/home.md)

Voeg deze IP adressen aan uw lijst van gewenste personen toe om toegang voor Federatieve Samenstelling van het Publiek te verlenen.

## Beleid samenvoegen {#merge-policies}

Als uw zandbak de belangrijkheid van de a **dataset** samenvoegbeleid gebruikt, gelieve de Zorg van de Klant van Adobe te contacteren om de `Halos UPS` dataset aan uw fusiebeleid toe te voegen.

Voor meer informatie over fusiebeleid, te lezen gelieve het [&#x200B; overzicht van het samenvoegbeleid &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/profile/merge-policies/overview).

## Afvoerkanalen en beperkingen {#fac-guardrails}

* De rechten, de productbeperkingen en de prestatiegaranties die in de [&#x200B; documentatie van Adobe Real-Time Customer Data Platform &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/profile/guardrails){target="_blank"} worden vermeld zijn op de Federatieve Samenstelling van het Publiek van toepassing.

* Federated Audience Composition biedt ondersteuning voor het exporteren van grote doelgroepen, met bestanden van meer dan 1 GB. Voor optimale prestaties is de maximale aanbevolen bestandsgrootte maximaal 20 GB.
