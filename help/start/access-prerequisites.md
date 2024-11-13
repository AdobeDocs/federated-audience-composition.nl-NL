---
title: Vereisten en instructies voor Federatieve Audience Composition
description: Ervaar vereisten, toestemmingen, en gidsen voor de Samenstelling van de Publiek van de Federatieve
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 3%

---

# Vereisten en geleiders {#fac-access}

De Federatieve Samenstelling van het Publiek vereist Adobe Real-time Customer Data Platform en/of Adobe Journey Optimizer **eerste** of **Echte** pakketten. Om toegang te krijgen tot deze mogelijkheid, moet u de add-on van de Samenstelling van de Federatieve Publiek hebben gekocht.

>[!AVAILABILITY]
>
>Nadat u het welkomstbericht via e-mail van de Adobe hebt ontvangen, kan het nog een paar uur duren voordat de interface wordt bijgewerkt en de functies die voor u beschikbaar zijn.

## Ondersteunde systemen {#supported-systems}

De Federatieve Samenstelling van de Publiek steunt de volgende wolkenpakhuizen:

* Amazon Redshift
* Azure synapse
* Databricks
* Google Big Query
* Snowflake
* Vertica Analytics

Leer hoe te om een verbinding met deze systemen in [ tot stand te brengen deze pagina ](../connections/connections.md).

## Machtigingen {#permissions}

Wanneer u de add-on Federated Audience Composition aanschaft, wordt voor elke actieve sandbox op dat moment een productprofiel gemaakt. Dit productprofiel wordt gecreeerd in de Admin Console onder **Adobe Experience Platform** productkaart en volgt deze noemende overeenkomst: `ACP_FAC - <<SandboxName>> - admin.` om tot de Federatieve Samenstelling van de Publiek voor een specifieke zandbak toegang te hebben, moeten de gebruikers aan het productprofiel worden toegevoegd dat voor die zandbak wordt gecreeerd.

Als bijvoorbeeld een nieuwe sandbox met de naam &quot;fac-test&quot; wordt geactiveerd, wordt een overeenkomstig productprofiel &quot;ACP_FAC - fac-test - admin&quot; gemaakt. Gebruikers moeten aan dit productprofiel worden toegevoegd om Federated Audience Composition met deze sandbox te kunnen benaderen.

## IP-aanbieding toestaan {#ip}

Om Federated Audience Composition veilig toe te laten om tot uw gegevensbestanden toegang te hebben, contacteer uw vertegenwoordiger van de Adobe om de IP adressen van de servers van de Samenstelling van de Federatieve Publiek te krijgen die tot hen zullen toegang hebben.

Voeg deze IP adressen aan uw lijst van gewenste personen toe om toegang voor Federatieve Samenstelling van het Publiek te verlenen.

## Afbeeldingen en beperkingen {#fac-guardrails}

* De Federatieve Samenstelling van het Publiek is momenteel niet beschikbaar aan klanten [ die gezondheidsgegevens ](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield) nemen {target="_blank"} en aan de klanten van de Privacy en van het Veiligheidsschild van Adobe Journey Optimizer. [Meer informatie](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* De rechten, de productbeperkingen en de prestatiegaranties die in de [ documentatie van Adobe Real-time Customer Data Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails) worden vermeld {target="_blank"} zijn op dit toe:voegen-op van toepassing.
