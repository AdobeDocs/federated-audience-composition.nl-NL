---
title: Privacy en beveiliging in Federale Audience Composition
description: Leer hoe Federated Audience Composition omgaat met privacy en beveiliging voor gebruikersgegevens, waaronder functies zoals gegevensbeheer, handhaving van toestemming, toegangsbeheer, gegevenscodering en privacynaleving.
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 7429577d99d2f163e7084db056005fe641d1bcf3
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 1%

---

# Beheer van gegevens, privacy en beveiliging

>[!IMPORTANT]
>
>Federated Audience Composition is volledig HIPAA-compatibel en kan worden gebruikt voor klanten met een gezondheidszorg-, privacy- en beveiligingsschild.

De Federated Samenstelling van het Publiek verstrekt verscheidene diensten en hulpmiddelen die u met uw bedrijfspraktijken, wettelijke verplichtingen, en ontwikkelingsprocessen laten voldoen.

Deze diensten kunnen in drie categorieën worden ingedeeld:

- [Datagovernance](#data-governance)
- [Privacy](#privacy)
- [Beveiliging](#security)

## Datagovernance {#data-governance}

U kunt gegevensbeheer gebruiken om de gegevens van uw klant te beheren en te identificeren, ervoor te zorgen dat deze correct zijn gelabeld om de beperkingen na te leven die door uw organisatie of wettelijke voorschriften zijn gedefinieerd.

### Labels voor gegevensgebruik {#data-usage-labels}

U kunt labels voor gegevensgebruik gebruiken om gegevenssets en velden te categoriseren op basis van het beleid dat van toepassing is op die gegevens. Nadat u een publiek gebruikend samenstellingen creeert, kunt u de aangewezen gegevensetiketten op het resulterende schema toepassen om het aan de vereiste gebruiksbeperkingen te houden.

Voor meer informatie bij het gebruiken van gegevensetiketten in de Federatieve Samenstelling van de Auditie, lees gelieve [ toegangsetiketten sectie ](../compositions/gs-compositions.md#access-labels){target="_blank"} toe te passen.

## Privacy

Federated Audience Composition biedt de gefederaliseerde gegevens die Adobe Experience Platform en Adobe Journey Optimizer kunnen gebruiken en zorgt ervoor dat de privacy van de gegevens van uw gebruiker wordt gerespecteerd.

### Privacyservice {#privacy-service}

Aangezien de Federatieve Samenstelling van het Publiek **&#x200B;**&#x200B;geen van de klantengegevens van om het even welke gegevenspakhuizen opslaat, kunt u Adobe Experience Platform Privacy Service gebruiken om aan de verzoeken van het gegevenssubject en van de gegevensschrapping te voldoen.

Wanneer u bijvoorbeeld een publiek maakt met het blok met opslagactiviteit in het compositiescanvas, wordt het resulterende publiek als een extern publiek opgeslagen in het datumpeer in Experience Platform. Dit externe publiek wordt gemarkeerd met het naamveld en de naamruimte van de identiteit. Als gevolg hiervan kunt u Privacy Service gebruiken om die profielen met een extern publiek te openen en te verwijderen.

Alternatief, na het creëren van een profielverrijking door sparen profielactiviteit in het samenstellingscanvas te gebruiken, wordt de resulterende verrijking opgeslagen in Experience Platform als profiel-toegelaten schema en profiel-toegelaten dataset. Deze verrijkingsgegevens worden gemarkeerd met een identiteitsveld en naamruimte. Dit betekent dat u Privacy Service kunt gebruiken om deze profielen te openen en schoon te maken.

Voor meer informatie over Privacy Service, gelieve het [ overzicht van Privacy Service ](https://experienceleague.adobe.com/nl/docs/experience-platform/privacy/home){target="_blank"} te lezen.

### Privacyverzoeken {#privacy-requests}

In Privacy Service kunt u individuele privacyverzoeken maken en beheren om klantgegevens te benaderen en te verwijderen uit de Federated Audience Composition. Privacy Service verstrekt zowel a [ gebruikersinterface ](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=nl-NL){target="_blank"} als a [ RESTful API ](https://experienceleague.adobe.com/nl/docs/experience-platform/privacy/api/overview){target="_blank"} om u te helpen verzoeken van klantengegevens beheren.

Voor meer informatie bij het creëren van en het beheren van privacyverzoeken, te lezen gelieve de [ privacybanen in de gids van Privacy Service UI ](https://experienceleague.adobe.com/nl/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

### Toestemming voor beleidshandhaving {#consent}

Federated Audience Composition, via Experience Platform, biedt tools waarmee u de handhaving van uw toestemming kunt automatiseren, zodat u publiek activeert op basis van de toestemming die aan uw klanten wordt gegeven.

Wanneer u bijvoorbeeld een publiek maakt met het blok met opslagactiviteit in het compositiescanvas, wordt het resulterende publiek als een extern publiek opgeslagen in het datumpeer in Experience Platform. Experience Platform ondersteunt automatisch validatie van toestemming tijdens activering. Voor meer informatie, gelieve te lezen de [ Veelgestelde vragen van de Dienst van de Segmentatie ](https://experienceleague.adobe.com/nl/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Alternatief, nadat u een profielverrijking door sparen profielactiviteit in het samenstellingscanvas te gebruiken creeert, wordt de resulterende verrijking opgeslagen in Experience Platform als profiel-toegelaten schema en profiel-toegelaten dataset. Voor bestaande profielen worden de beschikbare toestemmingskenmerken automatisch gerespecteerd tijdens activering. Voor nieuwe profielen worden de toestemmingskenmerken die tijdens de profielopname worden verstrekt automatisch gerespecteerd tijdens activering. Voor meer informatie bij het toepassen van toestemmingen op profielen, te lezen gelieve de [ handleiding van de toestemmingen en van de voorkeurengebiedgroep ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Voor meer informatie bij het toepassen van toestemmingen, te lezen gelieve [ beleid UI gids ](https://experienceleague.adobe.com/nl/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"} leidt.

### Levenscyclus van gegevens {#data-lifecycle}

Aangezien de Federatieve Samenstelling van het Publiek **&#x200B;**&#x200B;geen van de klantengegevens van om het even welke gegevenspakhuizen opslaat, kunt u Experience Platform gebruiken om de gegevenslevenscyclus te behandelen. Met het Geavanceerde Beheer van de Levenscyclus van Gegevens, kunt u uw gegevenslevenscyclus op zowel dataset als verslagniveau beheren.

Wanneer u bijvoorbeeld een publiek maakt met het blok met opslagactiviteit in het compositiescanvas, wordt het resulterende publiek als een extern publiek opgeslagen in het datumpeer in Experience Platform. Aangezien dit gegeven **niet** wordt opgeslagen in de Federatieve Samenstelling van het Publiek, worden de publieksgegevens en de overeenkomstige datasets automatisch geschrapt wanneer het publiek in het Portaal van het Publiek wordt geschrapt.

Alternatief, nadat u een profielverrijking door sparen profielactiviteit in het samenstellingscanvas te gebruiken creeert, wordt de resulterende verrijking opgeslagen in Experience Platform als profiel-toegelaten schema en profiel-toegelaten dataset. Hierdoor kunt u de Levenscyclus van gegevens openen en de profielen opschonen.

Voor meer informatie bij het gebruiken van de Levenscyclus van Gegevens, te lezen gelieve het [ overzicht van de Levenscyclus van Gegevens ](https://experienceleague.adobe.com/nl/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Beveiliging {#security}

De veiligheid van gegevens verzekert uw gegevens in Federated Audience Composition worden beschermd.

### Versleuteling {#encryption}

Federated Audience Composition biedt codering via codering van data-at-rest, codering van data-in-transit en door de klant beheerde sleutels.

Gegevens in rust hebben betrekking op de klantgegevens die binnen Federated Audience Composition worden gebruikt. De gegevens worden gecodeerd door het cloudservicebureau en worden in gecodeerde vorm gebruikt in Federated Audience Composition.

De gegevens in doorvoer verwijzen naar de klantengegevens aangezien het zich van één component aan een andere in Federated Audience Composition beweegt. De gegevens blijven versleuteld via Federated Audience Composition-componenten met TLS 1.3 via HTTPS.

Voor meer informatie over hoe Adobe gegevensencryptie behandelt, te lezen gelieve de gids over [ gegevensencryptie in Experience Platform ](https://experienceleague.adobe.com/nl/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Door de klant beheerde sleutels {#customer-managed-keys}

Met door de klant beheerde sleutels hebt u controle over uw gegevens doordat u uw eigen coderingssleutels kunt gebruiken om uw gegevens te coderen. Aangezien de Federatieve Samenstelling van het Publiek **&#x200B;**&#x200B;geen van de klantengegevens opslaat, kunt u klant beheerde sleutels op het resulterende publiek en de verrijking direct gebruiken, aangezien zij in het gegevenshoon op Experience Platform zullen worden opgeslagen.

Voor meer informatie over klant beheerde sleutels, te lezen gelieve de [ klant beheerde sleutelgids ](https://experienceleague.adobe.com/nl/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

### Controlelogboek {#audit-log}

Al creeer, lees, werk, en schrappingsverrichtingen bij die in de Samenstelling van de Publiek worden uitgevoerd worden het programma geopend in het auditspoor. U kunt dit controlelogboek gebruiken om deze acties te volgen, verantwoordingsplicht af te dwingen, en nalevingscontroles te steunen.

Voor meer informatie, te lezen gelieve het [ overzicht van het Spoor van de Controle ](/help/admin/audit-trail.md){target="_blank"}.

### Toegangsbeheer {#access-control}

U kunt toegang tot Federated Audience Composition op zowel een gebied als rolgebaseerd niveau controleren. U kunt deze toegangscontroles gebruiken om het beleid van het gegevensbeheer af te dwingen, blootstelling van gevoelige informatie te beperken, en toegang met gebruikersverantwoordelijkheden te richten.

Voor meer informatie over toegangsbeheer in de Federatieve Samenstelling van het Publiek, gelieve de [ gids van de toegangscontrole ](/help/governance-privacy-security/access-control.md){target="_blank"} te lezen.

### Gegevenslokalisatie {#data-localization}

De federated Samenstelling van het publiek slaat **&#x200B;**&#x200B;geen klantengegevens op. Dientengevolge, moet u ervoor zorgen dat u **slechts** uw externe gegevensbestanden met het passende zandbakgebied verbindt om uw gegevens in het zelfde gebied te houden. Als u het gegevensbestand van een verschillend gebied met een zandbak verbindt, is Adobe **niet** verantwoordelijk voor gegevenslocalisatie.

## Volgende stappen {#next-steps}

Nadat u deze handleiding hebt gelezen, hebt u meer inzicht in de functies voor gegevensbeheer, privacy en beveiliging die worden gebruikt voor Federated Audience Composition, zoals labels voor gegevensgebruik, privacynaleving, handhaving van machtigingen, beheer van de gegevenslevenscyclus en toegangscontrole.
