---
audience: end-user
title: De publieksactiviteit Opslaan gebruiken
description: Leer hoe u de publieksactiviteit Opslaan gebruikt
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: 8cc7a4cb8cf5e98496ddf366b9212c25acfdbbd0
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---


# Doelgroep opslaan {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Een publiek opslaan"
>abstract="Gebruik deze activiteit om een nieuw publiek van de bevolking tot stand te brengen die stroomopwaarts in de samenstelling wordt berekend. Het gecreeerde publiek wordt toegevoegd aan de lijst van publiek, en beschikbaar via het **Publiek** menu."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Uitgaande overgang genereren"
>abstract="Gebruik deze optie als u een overgang na **wilt toevoegen sparen publiek** activiteit."

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

**sparen publiek** activiteit staat u toe om een nieuw publiek van de bevolking tot stand te brengen die stroomopwaarts in een samenstelling wordt verwerkt. Het gecreeerde publiek wordt toegevoegd aan de lijst van het publiek van Adobe Experience Platform, en beschikbaar gemaakt via het **publiek** menu. [ leer hoe te met publiek ](../../start/audiences.md) werken

Deze activiteit wordt hoofdzakelijk gebruikt om populatiegroepen in de zelfde samenstelling te berekenen, door hen in herbruikbaar publiek om te zetten. Verbind het met andere het richten activiteiten zoals a **bouwt publiek** of a **combineer** activiteit.

## Vorm sparen publieksactiviteit {#save-audience-configuration}

Volg deze stappen om **te vormen sparen publiek** activiteit:

1. Voeg a **sparen publiek** activiteit aan uw samenstelling toe.

   ![](../assets/save-audience.png)

1. Geef het label op van het publiek dat u wilt maken.

   >[!IMPORTANT]
   >
   >Het label van het publiek moet uniek zijn binnen de huidige sandbox. Het mag niet hetzelfde label hebben als een bestaand publiek.

1. Gebruik de sectie Toewijzingen publiek om de velden te selecteren die u wilt overbrengen met het nieuwe publiek. Om dit te doen, klik **Toewijzing van het publiek** dan toevoegen de bron en doelpublieksgebieden.

   Herhaal de bewerking om zoveel publiek-toewijzingen toe te voegen als u nodig hebt.

1. Selecteer de primaire identiteit en naamruimte die u wilt gebruiken om de doelprofielen in de database te identificeren:

   * **Primair identiteitsgebied**: Selecteer het gebied om de profielen te gebruiken te identificeren. Bijvoorbeeld zijn e-mailadres of telefoonnummer.
   * **Identiteitsnaamruimte**: Selecteer namespace aan gebruik om de profielen, d.w.z. het type van gegevens te identificeren om als identificatiesleutel te gebruiken. Bijvoorbeeld, als het e-mailadres als primair identiteitsgebied is geselecteerd, zou de identiteit namespace **E-mail** moeten worden geselecteerd. Als het unieke herkenningsteken het telefoonaantal is, dan zou de identiteit namespace **Telefoon** moeten worden geselecteerd.

Na het uitvoeren van de samenstelling, wordt het resulterende publiek bewaard in Adobe Experience Platform, en toegankelijk gemaakt in het **Publiek** menu. Het gemaakte publiek bevat alle velden die zijn geselecteerd in de sectie Audience Mappings (Toewijzingen publiek). U kunt het publiek activeren naar elk doel dat door Adobe Experience Platform wordt ondersteund.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
