---
audience: end-user
title: De publieksactiviteit Opslaan gebruiken
description: Leer hoe u de publieksactiviteit Opslaan gebruikt
source-git-commit: c151cc316eb9b5df6fa1d09f01455313195dfd07
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# Doelgroep opslaan {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Een publiek opslaan"
>abstract="Gebruik deze activiteit om een bestaand publiek bij te werken of een nieuw publiek van de bevolking tot stand te brengen die stroomopwaarts in de samenstelling wordt berekend. Het publiek dat wordt gemaakt, wordt toegevoegd aan de lijst met doelgroepen en is beschikbaar via de **Soorten publiek** -menu."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Uitgaande overgang genereren"
>abstract="Gebruik deze optie als u een overgang wilt toevoegen na het dialoogvenster **Adviezen opslaan** activiteit."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Primair identiteitsveld"
>abstract="Selecteer de primaire identiteit die u voor profielen wilt gebruiken."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Meer informatie in de documentatie bij Experience Platforms"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Naamruimte identiteit"
>abstract="Selecteer de naamruimte die u wilt gebruiken voor profielen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces" text="Meer informatie in de documentatie bij Experience Platforms"

De **Adviezen opslaan** met activiteit kunt u een bestaand publiek bijwerken of een nieuw publiek maken van de bevolking die stroomopwaarts in een compositie is berekend. Het publiek dat wordt gemaakt, wordt toegevoegd aan de lijst met doelgroepen van toepassingen en wordt beschikbaar gesteld via de **Soorten publiek** -menu.

Deze activiteit wordt hoofdzakelijk gebruikt om populatiegroepen in de zelfde samenstelling te berekenen, door hen in herbruikbaar publiek om te zetten. Verbind het met andere gerichte activiteiten zoals **publiek opbouwen** of **Combineren** activiteit.

## Vorm sparen publieksactiviteit {#save-audience-configuration}

Voer de volgende stappen uit om de **Adviezen opslaan** activiteit:

1. Voeg een **Adviezen opslaan** activiteit aan uw samenstelling.

   ![](../assets/save-audience.png)

1. Geef het label op van het publiek dat u wilt maken.

1. Klikken **Toewijzing publiek toevoegen** Kies vervolgens de velden voor de bron en het doelpubliek:

   * **Source Audience Field**:
   * **Doelpubliek veld**:

   Herhaal de bewerking om zoveel publiek-toewijzingen toe te voegen als u nodig hebt.

1. Selecteer de primaire identiteit en naamruimte die u wilt gebruiken om de doelprofielen in de database te identificeren:

   * **Primair identiteitsveld**: Selecteer het veld dat u wilt gebruiken om de profielen te identificeren. Bijvoorbeeld zijn e-mailadres of telefoonnummer.
   * **Naamruimte identiteit**: Selecteer de naamruimte die u wilt gebruiken om de profielen te identificeren, dat wil zeggen het type gegevens dat u als identificatietoets wilt gebruiken. Als het e-mailadres bijvoorbeeld is geselecteerd als primair identiteitsveld, wordt de naamruimte van de identiteit **E-mail** moet worden geselecteerd. Als het unieke herkenningsteken het telefoonaantal is, dan identiteit namespace **Telefoon** moet worden geselecteerd.

Na het uitvoeren van de samenstelling, wordt het resulterende publiek bewaard in Adobe Experience Platform, en toegankelijk gemaakt in **Soorten publiek** -menu.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
