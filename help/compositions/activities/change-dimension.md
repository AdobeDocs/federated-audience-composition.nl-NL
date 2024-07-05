---
audience: end-user
title: De activiteit Dimensie wijzigen gebruiken
description: Leer hoe u de activiteit Dimensie wijzigen gebruikt
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Dimensie wijzigen {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Om dit te doen, knevel op **Complement genereren** option"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Dimensieactiviteit wijzigen"
>abstract="Deze activiteit staat u toe om het schema, dat ook als het richten dimensie wordt bekend te veranderen, aangezien u een publiek bouwt. Het verschuift de as afhankelijk van het gegevensmalplaatje en het inputschema. U kunt bijvoorbeeld van het schema &quot;contracten&quot; overschakelen op het schema &quot;clients&quot;."

De **Dimensie wijzigen** de activiteit staat u toe om het schema te veranderen, dat ook als het richten dimensie wordt bekend, aangezien u uw publiek bouwt. Het verschuift de as afhankelijk van het gegevensmalplaatje en het inputschema.

## Vorm de de afmetingsactiviteit van de Verandering {#configure}

Voer de volgende stappen uit om de **Dimensie wijzigen** activiteit:

1. Voeg een **Dimensie wijzigen** activiteit aan uw samenstelling.

   ![](../assets/change-dimension.png)

1. Definieer de **Nieuw schema**. Tijdens het wijzigen van het schema worden alle records bewaard.

1. Voer de samenstelling uit om het resultaat te bekijken. Vergelijk de gegevens in de tabellen voor en na de **Dimensie wijzigen** en vergelijk de structuur van de compositietabellen.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->