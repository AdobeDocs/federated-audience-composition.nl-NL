---
audience: end-user
title: De activiteit Profielen opslaan gebruiken
description: Leer hoe u de activiteit Profielen opslaan gebruikt
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Profielen opslaan {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Profielen opslaan"
>abstract="Met de activiteit Profielen opslaan kunt u Experience Platform-profielen verrijken door gegevens van externe opslagruimten te federaliseren, zodat u klantprofielen kunt verfraaien met extra kenmerken. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="AEP-schema selecteren"
>abstract="Kies het Experience Platform-schema voor de profielen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Selecteer het veld Primaire identificatie"
>abstract="Selecteer de primaire identiteit die u wilt gebruiken om de doelprofielen in de database te identificeren."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="AEP-schema selecteren"
>abstract="Kies het Experience Platform-schema voor de profielen."

**sparen profielen** activiteit staat u toe om de profielen van Adobe Experience Platform met gegevens te verrijken die van externe pakhuizen worden gefederaliseerd.

Deze activiteit wordt typisch gebruikt om klantenprofielen te verbeteren door extra attributen en inzichten in te brengen zonder de gegevens fysiek te bewegen of te dupliceren in het platform

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
