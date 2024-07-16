---
title: Aan de slag met Federatieve Audience Composition
description: Leer wat Adobe Federated Audience Composition is en hoe u deze in Adobe Experience Platform kunt gebruiken
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---


# Aan de slag met Federatieve Audience Composition {#gs-fac}

Met de Adobe Federated Audience Composition kunnen gebruikers van Adobe Experience Platform-apps toegang krijgen tot hun klantgegevens die in hun zakelijke gegevenspaket zijn opgeslagen. De gegevens van de klant kunnen in veelvoudige gegevenspakhuizen leven en zouden onmiddellijk, zonder replicatie toegankelijk moeten zijn.

Adobe Experience Platform Federated Audience Composition biedt een eenvoudige en krachtige oplossing om uw bedrijfsgegevenspakhuis rechtstreeks in Adobe Real-time Customer Data Platform te verbinden en query&#39;s uit te voeren in de tabellen van uw gegevenspakhuis.

## Belangrijkste stappen {#gs-steps}

Met Adobe Federated Audience Composition kunt u Adobe Experience Platform-soorten publiek rechtstreeks vanuit uw database maken en bijwerken, zonder dat er iets hoeft te worden ingevoerd.

![ diagram ](assets/FAC-diagram.png)

Belangrijkste stappen:

* **Configuratie**

   1. Connect Adobe Experience Platform en uw zakelijke gegevenspaket.
De volgende databases worden ondersteund: Snowflake, Google Big Query, Azure synapse, Redshift.
Leer meer in [ deze pagina ](../connections/federated-db.md)
   1. Maak schema&#39;s om te selecteren welke gegevens toegankelijk moeten zijn vanuit de gebruikersinterface.
Leer meer in [ deze pagina ](../customer/schemas.md)
   1. Maak koppelingen voor uw datamodel.
Leer meer in [ deze pagina ](../data-management/gs-models.md)

* **stel publiek** samen

   1. Ontwerp en voer composities uit om een publiek te maken.
Leer meer in [ deze pagina ](../compositions/gs-compositions.md)
   1. Bestaande doelgroepen bijwerken of opnieuw gebruiken via het Adobe Experience Platform Audience-portaal en -bestemmingen.
Leer meer in [ deze pagina ](../connections/destinations.md)

## Meer informatie {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Instellingen voor uitvoering"
>abstract="In deze sectie kunt u instellingen configureren die betrekking hebben op de uitvoering van de workflow, zoals het aantal dagen dat de werkstroomgeschiedenis wordt bijgehouden."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Activiteit niet bewerkbaar"
>abstract="Wanneer de a **Vraag** of een **Verrijking** activiteit met extra gegevens in de console wordt gevormd, wordt het verrijkingsgegeven genomen en overgegaan in de uitgaande overgang, maar het kan niet worden uitgegeven."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Een koppeling maken"
>abstract="Geef de koppelingsinstellingen op."
