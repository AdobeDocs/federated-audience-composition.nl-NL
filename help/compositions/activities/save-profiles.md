---
audience: end-user
title: De activiteit Profielen opslaan gebruiken
description: Leer hoe u de activiteit Profielen opslaan gebruikt
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: ca975be136155f69bc84362fde8c283b1c4edffe
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# Profielen opslaan {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Profielen opslaan"
>abstract="Met de activiteit Profielen opslaan kunt u Experience Platform-profielen verrijken door gegevens van externe opslagruimten te federaliseren, zodat u klantprofielen kunt verfraaien met extra kenmerken. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Experience Platform-schema selecteren"
>abstract="Kies het Experience Platform-schema voor de profielen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Selecteer het veld Primaire identificatie"
>abstract="Selecteer de primaire identiteit die u wilt gebruiken om de doelprofielen in de database te identificeren."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Experience Platform-schema selecteren"
>abstract="Kies het Experience Platform-schema voor de profielen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode"
>title="Profielupdatemodus opslaan"
>abstract="De beschikbare updatemodi voor sparen profielactiviteit omvatten volledige update en stijgende update."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="Volledige update"
>abstract="De volledige updatemodus werkt de volledige set profielen voor verrijking bij."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="Incrementele update"
>abstract="De incrementele updatemodus werkt de profielen bij die zijn gewijzigd sinds de laatste verrijking is uitgevoerd."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="Primair identiteitsveld"
>abstract="In het veld primaire identiteit wordt de bron van de waarheid aangegeven wanneer profielen voor de verrijking worden samengevoegd."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="Vereiste veldcriteria"
>abstract="Een vereist veld is een kenmerk dat voor elk profiel of elke record moet worden ingevuld bij het exporteren van gegevens. Als een vereist veld ontbreekt, is het exporteren niet voltooid of geldig."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="Criteria van primair identiteitsveld"
>abstract="De unieke id voor elk profiel of elke record. Dit zorgt ervoor dat elke record duidelijk herkend en op elkaar afgestemd kan worden, zodat dubbele gegevens voorkomen worden."

**sparen profielen** activiteit staat u toe om de profielen van Adobe Experience Platform met gegevens te verrijken die van externe pakhuizen worden gefederaliseerd.

Deze activiteit wordt typisch gebruikt om klantenprofielen te verbeteren door extra attributen en inzichten in te brengen zonder de gegevens fysiek te bewegen of te dupliceren in het platform.

## De activiteit Profielen opslaan configureren {#save-profile-configuration}

Volg deze stappen om **te vormen sparen profielen** activiteit:

1. Voeg a **sparen profielen** activiteit aan uw samenstelling toe.

   ![](../assets/save-profile.png)

1. Geef het label op van de profielen die u wilt maken.

   >[!IMPORTANT]
   >
   >Het label van het publiek moet uniek zijn binnen de huidige sandbox. Het mag niet hetzelfde label hebben als een bestaand publiek.

1. Selecteer het Adobe Experience Platform-schema dat u wilt gebruiken.

   ![](../assets/save-profile-2.png)

1. Kies het primaire identiteitsveld waarmee de profielen in de database worden geïdentificeerd.

1. Als u extra gegevensattributen wilt met elkaar in overeenstemming brengen, **voegt attributen** toe.

   Dan, specificeer het **Source** gebied (externe gegevens) en het **3&rbrace; gebied van de Bestemming &lbrace;(schemagebied) voor elk attribuut u wilt in kaart brengen.**

   ![](../assets/save-profile-3.png)

1. Zodra gevormd, klik **Begin**.
