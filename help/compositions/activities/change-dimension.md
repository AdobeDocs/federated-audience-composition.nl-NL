---
audience: end-user
title: De activiteit Dimensie wijzigen gebruiken
description: Leer hoe u de activiteit Dimensie wijzigen gebruikt
source-git-commit: 44be467650e2329a1fce6c5adb6d266d94efd1e2
workflow-type: tm+mt
source-wordcount: '185'
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
>abstract="Met deze activiteit kunt u de doeldimensie, dat wil zeggen het schema, wijzigen terwijl u een publiek maakt. Het verschuift de as afhankelijk van het gegevensmalplaatje en de inputdimensie. U kunt bijvoorbeeld van de dimensie &quot;contracten&quot; naar de dimensie &quot;clients&quot; schakelen."

De **Dimensie wijzigen** Met activiteit kunt u tijdens het opbouwen van uw publiek de doeldimensie, dat wil zeggen het schema, wijzigen. Het verschuift de as afhankelijk van het gegevensmalplaatje en de inputdimensie. <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

## Vorm de de afmetingsactiviteit van de Verandering {#configure}

Voer de volgende stappen uit om de **Dimensie wijzigen** activiteit:

1. Voeg een **Dimensie wijzigen** activiteit aan uw samenstelling.

   ![](../assets/change-dimension.png)

1. Definieer de **Nieuw schema**. Tijdens het wijzigen van het schema worden alle records bewaard.

1. Voer de samenstelling uit om het resultaat te bekijken. Vergelijk de gegevens in de lijsten vóór en na de activiteit van de veranderingsdimensie, en vergelijk de structuur van de samenstellingstabellen.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->