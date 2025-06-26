---
audience: end-user
title: Aan de slag met gegevensmodellen
description: Leer hoe u begint met gegevensmodellen
exl-id: 7e1f74c4-b89a-480c-8e12-0257a71e629d
source-git-commit: b39fc9ed99a799d6ef6d5821554ebd2a409a652f
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---


# Aan de slag met gegevensmodellen {#data-model-beta}

>[!AVAILABILITY]
>
>Voor toegang tot gegevensmodellen hebt u een van de volgende machtigingen nodig:
>
>- **beheer Federated Gegevensmodel**
>&#x200B;>- **Bekijk het Verbond Model van Gegevens**
>
>Voor meer informatie over de vereiste toestemmingen, te lezen gelieve de [ gids van de toegangscontrole ](/help/governance-privacy-security/access-control.md).

## Wat is een gegevensmodel {#data-model-start}

Een gegevensmodel is een reeks schema&#39;s, publiek, en de verbindingen tussen hen. Het wordt gebruikt om publiek met gegevensbestandgegevens te verbinden.

In Federated Audience Composition kunt u gegevensmodellen rechtstreeks in de Canvasweergave maken en beheren. Dit omvat het toevoegen van schema&#39;s en publiek, evenals het bepalen van de verbindingen tussen hen die op uw gebruiksgeval worden gebaseerd.

Leer meer over [ schema&#39;s ](../customer/schemas.md#schema-start) en [ publiek ](../start/audiences.md).

U ziet bijvoorbeeld onder een weergave van een gegevensmodel de tabellen met hun naam en de koppelingen daartussen.

![](assets/datamodel.png){zoomable="yes"}

## Een gegevensmodel maken {#data-model-create}

Ga als volgt te werk om een gegevensmodel te maken:

1. Open in de sectie **[!UICONTROL Federated Data]** het menu **[!UICONTROL Models]** en blader naar de tab **[!UICONTROL Data model]** .

   Klik op de knop **[!UICONTROL Create data model]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Definieer de naam van het gegevensmodel en klik op de knop **[!UICONTROL Create]** .

1. Klik op het dashboard van het gegevensmodel op **[!UICONTROL Add schemas]** om het schema te kiezen dat aan het gegevensmodel is gekoppeld.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

1. Bovendien kunt u een publiek toevoegen aan uw gegevensmodel. Selecteer **[!UICONTROL Add Audiences]** om de doelgroepen te definiëren.

   ![](assets/datamodel-audiences.png){zoomable="yes"}

1. Vestig verbindingen tussen lijsten in uw gegevensmodel om nauwkeurige gegevensverhoudingen te verzekeren. [Meer informatie](#data-model-links)

1. Nadat u de configuratie hebt voltooid, klikt u op **[!UICONTROL Save]** om de wijzigingen toe te passen.

## Koppelingen maken {#data-model-links}

>[!BEGINTABS]

>[!TAB  mening van de Lijst ]

Ga als volgt te werk als u koppelingen wilt maken tussen tabellen in uw datamodel op het tabblad Tabeloptie:

1. Klik op het menu **[!UICONTROL Create link]** van een van de tabellen of klik op de knop **[!UICONTROL Create links]** en kies de twee tabellen:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Vul het opgegeven formulier in om de koppeling te definiëren.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Kardinaliteit**

   &#x200B;* **1-n**: één voorkomen van de bronlijst kan verscheidene overeenkomstige voorkomen van de doellijst hebben, maar één voorkomen van de doellijst kan hoogstens één overeenkomstige voorkomen van de bronlijst hebben.

   &#x200B;* **n-1**: één voorkomen van de doellijst kan verscheidene overeenkomstige voorkomen van de bronlijst hebben, maar één voorkomen van de bronlijst kan hoogstens één overeenkomstige voorkomen van de doellijst hebben.

   &#x200B;* **1-1**: één voorkomen van de bronlijst kan hoogstens één overeenkomstige voorkomen van de doellijst hebben.

Alle koppelingen die voor uw datamodel zijn gedefinieerd, worden hieronder weergegeven:

![](assets/datamodel_alllinks.png){zoomable="yes"}

>[!TAB  mening van het Canvas ]

Ga als volgt te werk als u koppelingen wilt maken tussen tabellen in uw datamodel op het tabblad Canvasweergave:

1. Open de Canvasweergave van uw gegevensmodel en kies de twee tabellen die u wilt koppelen

1. Klik op de knop ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) naast Source Join en sleep de pijl naar Target Join om de verbinding tot stand te brengen.

   ![](assets/datamodel.gif){zoomable="yes"}

1. Vul het opgegeven formulier in om de koppeling te definiëren en klik op **[!UICONTROL Apply]** zodra dit is geconfigureerd.

   ![](assets/datamodel-canvas-1.png){zoomable="yes"}

   **Kardinaliteit**

   &#x200B;* **1-n**: één voorkomen van de bronlijst kan verscheidene overeenkomstige voorkomen van de doellijst hebben, maar één voorkomen van de doellijst kan hoogstens één overeenkomstige voorkomen van de bronlijst hebben.

   &#x200B;* **n-1**: één voorkomen van de doellijst kan verscheidene overeenkomstige voorkomen van de bronlijst hebben, maar één voorkomen van de bronlijst kan hoogstens één overeenkomstige voorkomen van de doellijst hebben.

   &#x200B;* **1-1**: één voorkomen van de bronlijst kan hoogstens één overeenkomstige voorkomen van de doellijst hebben.

1. Alle koppelingen die in het gegevensmodel zijn gedefinieerd, worden als pijlen weergegeven in de canvasweergave. Klik op een pijl tussen twee tabellen om details weer te geven, wijzigingen aan te brengen of de koppeling naar wens te verwijderen.

   ![](assets/datamodel-canvas-2.png){zoomable="yes"}

1. Gebruik de werkbalk om het canvas aan te passen en aan te passen.

   ![](assets/datamodel-canvas-3.png)

   &#x200B;* **[!UICONTROL Zoom in]**: vergroot het canvas om de details van uw gegevensmodel duidelijker te zien.
   &#x200B;* **[!UICONTROL Zoom out]**: verklein de canvasgrootte voor een bredere weergave van uw gegevensmodel.
   &#x200B;* **[!UICONTROL Fit view]**: pas het zoomniveau aan zodat alle schema&#39;s en/of doelgroepen in het zichtbare gebied passen.
   &#x200B;* **[!UICONTROL Toggle interactivity]**: Schakel gebruikersinteractie met het canvas in of uit.
   &#x200B;* **[!UICONTROL Filter]**: kies welk schema u wilt weergeven binnen het canvas.
   &#x200B;* **[!UICONTROL Force auto layout]**: schema&#39;s en/of publiek automatisch rangschikken voor een betere organisatie.

>[!ENDTABS]

## Video {#data-model-video}

Leer hoe u een gegevensmodel maakt in deze video:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
