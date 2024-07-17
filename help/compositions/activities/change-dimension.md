---
audience: end-user
title: De activiteit Dimensie wijzigen gebruiken
description: Leer hoe u de activiteit Dimensie wijzigen gebruikt
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Dimensie wijzigen {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Schakel hiertoe de optie **[!UICONTROL Generate complement]** in"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Dimensieactiviteit wijzigen"
>abstract="Deze activiteit staat u toe om het schema, dat ook als het richten dimensie wordt bekend te veranderen, aangezien u een publiek bouwt. Het verschuift de as afhankelijk van het gegevensmalplaatje en het inputschema. U kunt bijvoorbeeld van het schema &quot;contracten&quot; overschakelen op het schema &quot;clients&quot;."

De **dimensie van de Verandering** activiteit staat u toe om het schema te veranderen, dat ook als het richten van dimensie wordt bekend, aangezien u uw publiek bouwt. Het verschuift de as afhankelijk van het gegevensmalplaatje en het inputschema.

## Vorm de de afmetingsactiviteit van de Verandering {#configure}

Volg deze stappen om de **dimensie van de Verandering** activiteit te vormen:

1. Voeg de dimensie van de a **Verandering** activiteit aan uw samenstelling toe.

   ![](../assets/change-dimension.png)

1. Bepaal het **Nieuwe schema**. Tijdens het wijzigen van het schema worden alle records bewaard.

1. Voer de samenstelling uit om het resultaat te bekijken. Vergelijk de gegevens in de lijsten vóór en na de **dimensie van de Verandering** activiteit, en vergelijk de structuur van de samenstellingstabellen.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->