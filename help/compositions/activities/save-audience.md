---
audience: end-user
title: De publieksactiviteit Opslaan gebruiken
description: Meer informatie over het gebruik van de vorkactiviteit
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

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

1. In de **Modus** selecteert u de actie die u wilt uitvoeren:

   * **Een bestaand publiek maken of bijwerken**: definieer een **Label publiek**. Als het publiek reeds bestaat, zal het worden bijgewerkt, anders zal een nieuw publiek worden gecreeerd.

   * **Een bestaand publiek bijwerken**: kies de optie **Publiek** U wilt een update uitvoeren in de lijst met bestaande doelgroepen.

1. Selecteer de **Modus Bijwerken** die van toepassing zijn op bestaande doelgroepen:

   * **De inhoud van het publiek vervangen door nieuwe gegevens**: alle publieksinhoud wordt vervangen. De oude data gaan verloren. Alleen de gegevens van de binnenkomende overgang van de activiteit voor het opslaan van het publiek blijven behouden. Met deze optie wist u het publiekstype en de doeldimensie van het bijgewerkte publiek.

   * **Volledige doelgroep met nieuwe gegevens**: de oude publieksinhoud wordt bewaard en de gegevens van de binnenkomende overgang van de activiteit van het sparen publiek worden toegevoegd aan het.

1. Controleer de **Een uitgaande overgang genereren** als u een overgang wilt toevoegen na de **Adviezen opslaan** activiteit.

De inhoud van het opgeslagen publiek is dan beschikbaar in de gedetailleerde weergave van het publiek, die toegankelijk is vanuit het **Soorten publiek** -menu. De kolommen beschikbaar uit deze mening beantwoorden aan de kolommen van de binnenkomende overgang van **Adviezen opslaan** activiteit.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
