---
audience: end-user
title: Gebruik de het publieksactiviteit van de Bouwstijl
description: Leer hoe u de gebruikersactiviteit van Build gebruikt
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# publiek opbouwen {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Activiteit voor publiek opbouwen"
>abstract="De **publiek opbouwen** de activiteit staat u toe om het publiek te bepalen dat de samenstelling zal ingaan."

De **publiek opbouwen** de activiteit staat u toe om het publiek te bepalen dat de samenstelling zal ingaan.

Om de publieksbevolking te bepalen, kunt u:

<!--* Select an existing audience, created as a list in the client console.-->
* Selecteer een Adobe Experience Platform-publiek.
* Bouw een nieuw publiek met de bouwer van de vraagmodelleur door het filtreren criteria te bepalen en te combineren.

De **publiek opbouwen** activiteit kan aan het begin van de samenstelling of na enige andere activiteit worden geplaatst. Elke activiteit kan na de **publiek opbouwen**.

## Vorm de het publieksactiviteit van de Bouwstijl {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Doelgroep"
>abstract="Selecteer uw publiek."

Voer de volgende stappen uit om de **publiek opbouwen** activiteit:

1. Voeg een **publiek opbouwen** activiteit.
1. Definieer een label.
1. Bepaal het publiekstype: **Maak uw eigen** of **Lees publiek**.
1. Configureer uw publiek door de stappen uit te voeren die in de onderstaande tabbladen worden beschreven.

>[!BEGINTABS]

>[!TAB Uw eigen bestand maken (query)]

Voer de volgende stappen uit om uw eigen query te maken:

1. Selecteren **Uw eigen bestand maken (query)**.
1. Kies de optie **Doeldimensie**. Met de doeldimensie kunt u de doelgroep van de actie definiëren: ontvangers, begunstigden van contracten, exploitant, abonnees, enz. Standaard is het doel geselecteerd bij de ontvangers.<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. Klikken **Doorgaan**.
1. Gebruik de vraagmodeler om uw vraag te bepalen, de zelfde manier u creeert een publiek wanneer het ontwerpen van een nieuwe e-mail. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB Doelgroep lezen]

Voer de volgende stappen uit om een bestaand publiek te selecteren:

1. Selecteren **Lees publiek**.
1. Klikken **Doorgaan**.
1. Selecteer uw publiek, de zelfde manier u een publiek gebruikt wanneer het ontwerpen van een nieuwe levering. <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
