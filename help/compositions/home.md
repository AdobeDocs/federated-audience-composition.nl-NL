---
audience: end-user
title: Aan de slag met composities
description: Leer hoe u begint met composities
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: e82f1c237927af983a32c848cb9d45d84f9cf3fe
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# Overzicht van composities

>[!AVAILABILITY]
>
>Voor toegang tot composities hebt u een van de volgende machtigingen nodig:
>
>- **beheer Federale Samenstellingen**
>- **Mening Federatieve Samenstellingen**
>
>Voor meer informatie over de vereiste toestemmingen, te lezen gelieve de [&#x200B; gids van de toegangscontrole &#x200B;](/help/governance-privacy-security/access-control.md).

Met Federatieve compositie voor publiek kunt u composities maken, waarbij u verschillende activiteiten kunt gebruiken in een visueel canvas om een publiek te maken. Nadat u de compositie hebt gemaakt, worden de resulterende doelgroepen opgeslagen in Adobe Experience Platform en kunnen ze worden gebruikt in Experience Platform-bestemmingen en Adobe Journey Optimizer om klanten als doel in te stellen.

![&#x200B; het werkschema van de steekproefsamenstelling van A wordt getoond binnen de Federatieve Samenstelling van het Publiek.](assets/compositions/composition-example.png){zoomable="yes"}{width="70%"}

## Compositieonderdelen {#components}

Een samenstelling binnen Federated Audience Composition bestaat uit de volgende delen:

- **[!UICONTROL Activities]**: Een activiteit is een taak die moet worden uitgevoerd en die binnen de compositie door pictogrammen wordt vertegenwoordigd.
- **[!UICONTROL Transitions]**: Overgangen koppelen een bronactiviteit aan een doelactiviteit en definiëren hun volgorde. De informatie in de overgangen wordt opgeslagen binnen een het werklijst. Elke samenstelling gebruikt verscheidene werklijsten. De gegevens die in deze lijsten worden overgebracht kunnen gedurende de het levenscyclus van de samenstelling worden gebruikt.

## Composities openen en beheren {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composities"
>abstract="In dit scherm, kunt u tot de volledige lijst van samenstellingen toegang hebben, hun huidige status, laatste/volgende uitvoeringsdata controleren, en een nieuwe samenstelling creëren."

Composities zijn toegankelijk via het menu Adobe Experience Platform **[!UICONTROL Audiences]** op het tabblad **[!UICONTROL Federated compositions]** in de sectie **[!UICONTROL Customers]** .

Vanuit dit scherm kunt u nieuwe composities maken en bestaande composities openen. U kunt een bestaande samenstelling ook dupliceren of schrappen door de ![&#x200B; ellipsen &#x200B;](/help/assets/icons/more.png) knoop naast zijn naam te selecteren.

U kunt ook informatie weergeven over de composities, zoals de naam, de status, de maker en de datum die als laatste is gewijzigd.

| Status | Beschrijving |
| ------ | ----------- |
| **[!UICONTROL Draft]** | De compositie is gemaakt en opgeslagen. |
| **[!UICONTROL In progress]** | De compositie is uitgevoerd en wordt momenteel uitgevoerd. |
| **[!UICONTROL Stopped]** | De uitvoering van de compositie is voltooid en is gestopt. |
| **[!UICONTROL Paused]** | De uitvoering van de compositie is gepauzeerd. |
| **[!UICONTROL Erroneous]** | Er is een fout opgetreden tijdens het uitvoeren van de compositie. Voor meer informatie over de fout opent u de compositie en opent u de logbestanden. |

U kunt leren hoe te om een samenstelling in te beginnen of tegen te houden [&#x200B; creeer samenstellingsgids &#x200B;](./create-composition.md#monitor-logs).

![&#x200B; een lijst van A van de beschikbare samenstellingen wordt getoond.](assets/compositions/compositions-list.png){zoomable="yes"}{width="70%"}

Als u de lijst wilt verfijnen en de compositie wilt zoeken die u zoekt, kunt u de lijst doorzoeken en composities filteren op basis van de status of de laatste verwerkingsdatum.

U kunt de lijst ook aanpassen door kolommen toe te voegen of te verwijderen. Selecteer hiertoe de knop **[!UICONTROL Configure columns]** en voeg de gewenste uitvoerkolommen toe of verwijder deze.

![&#x200B; A lijst van de beschikbare kolommen u aan composities kunt toevoegen doorbladert pagina wordt getoond.](assets/compositions/compositions-columns.png){zoomable="yes"}{width="70%"}

### Toegangslabels toepassen {#access-labels}

Om toegangslabels op een specifieke samenstelling toe te passen, selecteer de samenstelling, die door **[!UICONTROL Manage access]** wordt gevolgd.

![&#x200B; de &quot;beheert toegang&quot;knoop wordt benadrukt binnen het samenstellingscanvas.](assets/compositions/select-manage-access.png){zoomable="yes"}{width="70%"}

De pop-up **[!UICONTROL Manage access]** wordt weergegeven. Op deze pagina, kunt u de toepasselijke toegang en de etiketten van het gegevensbeheer op uw samenstelling toepassen.

![&#x200B; Beheert toegangspopover wordt getoond. Dit toont een lijst van alle beschikbare etiketten u op de samenstelling kunt toepassen.](assets/compositions/manage-access.png){zoomable="yes"}{width="70%"}

| Type label | Beschrijving |
| ---------- | ----------- |
| Contractlabels | De etiketten van het contract (&quot;C&quot;etiketten) worden gebruikt om gegevens te categoriseren die contractuele verplichtingen hebben of met het beleid van het gegevensbeheer van uw organisatie verwant zijn. |
| Identiteitslabels | De etiketten van de identiteit (&quot;I&quot;etiketten) worden gebruikt om gegevens te categoriseren die een specifieke persoon kunnen identificeren of contacteren. |
| Gevoelige labels | Gevoelige labels (&quot;S&quot;-labels) worden gebruikt om u te categoriseren en/of om te bepalen of uw organisatie gevoelig is. |
| Partnerecosysteemlabels | De etiketten van het Ecosysteem van de partner worden gebruikt om gegevens uit bronnen buiten uw organisatie te categoriseren. |

Voor meer informatie over toegang en de etiketten van het gegevensbeheer, te lezen gelieve de [&#x200B; verklarende woordenlijst van het het etiketetiket van het gegevensgebruik &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference).

## Maken {#create}

Met Audience Composition kunt u een compositie voor Adobe Experience Platform maken. Voor meer informatie, lees [&#x200B; tot een samenstellingsgids &#x200B;](./create-composition.md) leiden.

## Volgende stappen

Na het lezen van deze gids, hebt u geleerd om, tot toegangslabels voor uw samenstellingen toegang te hebben te leiden en te leiden. Voor meer informatie bij het werken met publiek als geheel, gelieve te lezen de [&#x200B; gids van het publiek &#x200B;](../start/audiences.md).
