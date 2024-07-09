---
audience: end-user
title: Gebruik de het publieksactiviteit van de Bouwstijl
description: Leer hoe u de gebruikersactiviteit van Build gebruikt
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '237'
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
1. Geef op of u een audio wilt maken of een bestaande audio wilt selecteren.
1. Configureer uw publiek door de stappen uit te voeren die in de onderstaande tabbladen worden beschreven.

>[!BEGINTABS]

>[!TAB publiek maken]

Voer de volgende stappen uit om uw eigen publiek te maken:

1. Selecteren **publiek maken**.
1. Kies de optie **Schema**, ook wel bekend als doelgerichte dimensie. Met het schema kunt u de doelgroep voor de bewerking definiëren: ontvangers, begunstigden van contracten, operator, abonnees, enzovoort. Standaard is het schema geselecteerd bij de ontvangers.
1. Klikken **Doorgaan**.
1. Gebruik de vraagmodeler om uw vraag te bepalen. [Leer hoe te met vraagmodeler te werken](../../query/query-modeler-overview.md)

>[!TAB Doelgroep lezen]

Voer de volgende stappen uit om een bestaand publiek te selecteren:

1. Selecteren **Lees publiek**.
1. Klikken **Doorgaan**.
1. Selecteer uw publiek.

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
