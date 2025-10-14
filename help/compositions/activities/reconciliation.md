---
audience: end-user
title: De afstemmingsactiviteit gebruiken
description: Leer hoe u de verzoeningsactiviteit kunt gebruiken
exl-id: 933c3cba-9120-4a93-a668-866fb65ee197
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Afstemming {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Afstemmingsactiviteit"
>abstract="De **Verzoening** activiteit staat u toe om het verband tussen de gegevens in het gegevensbestand en de gegevens in een het werklijst te bepalen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Selectieveld Afstemmen"
>abstract="Selectieveld Afstemmen"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Afstemming maken, voorwaarde"
>abstract="Afstemming maken, voorwaarde"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Afstemming genereren"
>abstract="Afstemming genereren"

De **Verzoening** activiteit staat u toe om het verband tussen de gegevens in het gegevensbestand en de gegevens in een het werklijst te bepalen, bijvoorbeeld gegevens die van een extern systeem worden geladen.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

Hierdoor kunt u niet-geïdentificeerde gegevens koppelen aan bestaande bronnen. De verzoeningsverrichting impliceert dat de gegevens u zich aansluit bij reeds in het gegevensbestand zijn. Als u bijvoorbeeld de aankoopgegevens wilt afstemmen met het product dat u hebt gekocht, op welk tijdstip, op welke client enzovoort, moeten het product en de client al in de database aanwezig zijn.

## De afstemmingsactiviteit configureren {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Schema"
>abstract="Selecteer het nieuwe schema dat op de gegevens moet worden toegepast. Met een schema, ook wel doeldimensie genoemd, kunt u de doelpopulatie definiëren: ontvangers, abonnementen op apps, operators, abonnees, enz. Door gebrek, wordt de samenstelling huidige schema geselecteerd."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Afstemmingsregels"
>abstract="Selecteer afstemmingsregels die u wilt gebruiken voor de deduplicatie. Om attributen te gebruiken, selecteer de **Eenvoudige attributen** optie en kies de bron en bestemmingsgebieden. Om uw eigen verzoeningsvoorwaarde tot stand te brengen gebruikend de vraagmodeler, selecteer de **Geavanceerde verzoeningsvoorwaarden** optie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Doeldimensie selecteren"
>abstract="Selecteer het schema, dat ook als het richten dimensie wordt bekend, voor uw binnenkomende gegevens met elkaar in overeenstemming te brengen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Niet-compatibele gegevens behouden"
>abstract="Door gebrek, worden de niet in overeenstemming gebrachte gegevens gehouden in de uitgaande overgang en beschikbaar in de werklijst voor toekomstig gebruik. Om onverenigde gegevens te verwijderen, desactiveer **houden unconiled gegevens** optie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Afstemmingskenmerk"
>abstract="Selecteer het kenmerk dat u wilt gebruiken om gegevens met elkaar te verzoenen en bevestig de gegevens."

Volg deze stappen om de **Verzoening** activiteit te vormen:

1. Voeg de activiteit van de a **Verzoening** in uw samenstelling toe.

1. Selecteer het **Nieuwe schema**. Met een schema, ook wel doeldimensie genoemd, kunt u de doelpopulatie definiëren: ontvangers, abonnementen op apps, operators, abonnees, enz.

1. Selecteer de velden die u wilt gebruiken voor de afstemming. U kunt een of meer verzoeningscriteria gebruiken.

   1. Om attributen te gebruiken om gegevens te combineren, selecteer de **Eenvoudige attributen** optie dan **toevoegen regel** knoop.
   1. Selecteer de **Source** en **3&rbrace; gebieden van de Bestemming &lbrace;voor de verzoening.** Het **gebied van de Bestemming** beantwoordt aan de gebieden van het geselecteerde schema.

      De gegevens worden in overeenstemming gebracht wanneer bron en bestemming gelijk zijn. Bijvoorbeeld, selecteer de **E-mail** gebieden om profielen te dedupliceren die op hun e-mailadres worden gebaseerd.

      Om andere verzoeningscriteria toe te voegen, klik **regel** toevoegen knoop. Als er meerdere samenvoegvoorwaarden zijn opgegeven, moeten deze ALLES worden gecontroleerd zodat de gegevens aan elkaar kunnen worden gekoppeld.

      ![](../assets/reconciliation-rules.png)

   1. Om andere attributen te gebruiken om gegevens te combineren, selecteer de **Geavanceerde verzoeningsvoorwaarden** optie dan **creeer voorwaarden** knoop. U kunt dan uw eigen verzoeningsvoorwaarde tot stand brengen gebruikend de vraagmodeler. [&#x200B; Leer hoe te met de vraagmodelaar &#x200B;](../../query/query-modeler-overview.md) te werken

      ![](../assets/reconciliation-advanced.png)

1. U kunt gegevens filtreren om het gebruiken van **te combineren filter** knoop creëren. Hiermee kunt u een aangepaste voorwaarde maken met behulp van de querymodelfunctie.

Door gebrek, worden de niet in overeenstemming gebrachte gegevens gehouden in de uitgaande overgang en beschikbaar in de werkbare lijst voor toekomstig gebruik. Om onverenigde gegevens te verwijderen, desactiveer **houden unconiled gegevens** optie.

<!--
## Example {#reconciliation-example}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

The workflow is designed as follows:

![](../assets/workflow-reconciliation-sample-1.0.png)

 
It is built with the following activities:

* A [Load file](load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

    For example:

    ```
    lastname;firstname;email;birthdate;
    JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
    PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
    WEAVER;Justin;justin_w@testmail.com;11/15/1990;
    MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
    REESE;Richard;rreese@testmail.com;02/08/1987;
    ```

* A **Reconciliation** activity which identifies the incoming data as profiles, by using the **email** and **Date of birth** fields as reconciliation criteria.

    ![](../assets/workflow-reconciliation-sample-1.1.png)

* A [Save audience](save-audience.md) activity to create a new audience based on these updates. You can also replace the **Save audience** activity by an **End** activity if no specific audience needs to be created or updated. Recipient profiles are updated in any case when you run the workflow.


## Compatibility {#reconciliation-compat}

The **Reconciliation** activity does not exist in the Client console. All **Enrichments** activities created in the Client console with the reconciliation options enabled are displayed as **Reconciliation** activities in Campaign Web user interface.
-->
