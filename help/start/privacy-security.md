---
title: Privacy en beveiliging in Federale Audience Composition
description: Leer hoe Federated Audience Composition omgaat met privacy en beveiliging voor gebruikersgegevens, waaronder functies zoals gegevensbeheer, handhaving van toestemming, toegangsbeheer, gegevenscodering en privacynaleving.
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 0%

---


# Privacy en beveiliging in Federale Audience Composition

De Federated Audience Composition voldoet aan talrijke veiligheidspraktijken om uw gegevens tijdens verwerking te beschermen.

## Privacyservice {#privacy}

Federated Audience Composition biedt de gefederaliseerde gegevens die Adobe Experience Platform en Adobe Journey Optimizer kunnen gebruiken. Nochtans, slaat de Federatieve Samenstelling van het Publiek **geen** om het even welke klantengegevens van om het even welke gegevenspakhuizen op. Dit betekent dat u Adobe Experience Platform Privacy Service kunt gebruiken om te voldoen aan aanvragen voor het verwijderen van gegevens en het onderwerp.

Wanneer u bijvoorbeeld een publiek maakt met het blok met opslagactiviteit in het compositiescanvas, wordt het resulterende publiek als een extern publiek opgeslagen in het datumpeer in Experience Platform. Dit externe publiek wordt gemarkeerd met het naamveld en de naamruimte van de identiteit. Als gevolg hiervan kunt u Privacy Service gebruiken om die profielen met een extern publiek te openen en te verwijderen.

Alternatief, na het creëren van een profielverrijking door sparen profielactiviteit in het samenstellingscanvas te gebruiken, wordt de resulterende verrijking opgeslagen in Experience Platform als profiel-toegelaten schema en profiel-toegelaten dataset. Deze verrijkingsgegevens worden gemarkeerd met een identiteitsveld en naamruimte. Dit betekent dat u Privacy Service kunt gebruiken om deze profielen te openen en schoon te maken.

Voor meer informatie over Privacy Service, gelieve het [ overzicht van Privacy Service ](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/home){target="_blank"} te lezen.

### Privacyverzoeken {#privacy-requests}

In Privacy Service kunt u individuele privacyverzoeken maken en beheren om klantgegevens te benaderen en te verwijderen uit de Federated Audience Composition. Privacy Service verstrekt zowel a [ gebruikersinterface ](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html){target="_blank"} als a [ RESTful API ](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/overview){target="_blank"} om u te helpen verzoeken van klantengegevens beheren.

Voor meer informatie bij het creëren van en het beheren van privacyverzoeken, te lezen gelieve de [ privacybanen in de gids van Privacy Service UI ](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Toestemming voor beleidshandhaving {#consent}

Federated Audience Composition, via Experience Platform, biedt tools waarmee u de handhaving van uw toestemming kunt automatiseren, zodat u publiek activeert op basis van de toestemming die aan uw klanten wordt gegeven.

Wanneer u bijvoorbeeld een publiek maakt met het blok met opslagactiviteit in het compositiescanvas, wordt het resulterende publiek als een extern publiek opgeslagen in het datumpeer in Experience Platform. Experience Platform ondersteunt automatisch validatie van toestemming tijdens activering. Voor meer informatie, gelieve te lezen de [ Veelgestelde vragen van de Dienst van de Segmentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Alternatief, nadat u een profielverrijking door sparen profielactiviteit in het samenstellingscanvas te gebruiken creeert, wordt de resulterende verrijking opgeslagen in Experience Platform als profiel-toegelaten schema en profiel-toegelaten dataset. Voor bestaande profielen worden de beschikbare toestemmingskenmerken automatisch gerespecteerd tijdens activering. Voor nieuwe profielen worden de toestemmingskenmerken die tijdens de profielopname worden verstrekt automatisch gerespecteerd tijdens activering. Voor meer informatie bij het toepassen van toestemmingen op profielen, te lezen gelieve de [ handleiding van de toestemmingen en van de voorkeurengebiedgroep ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Voor meer informatie bij het toepassen van toestemmingen, te lezen gelieve [ beleid UI gids ](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"} leidt.

## Levenscyclus van gegevens {#data-lifecycle}

Aangezien de Federatieve Samenstelling van het Publiek **** geen van de klantengegevens van om het even welke gegevenspakhuizen opslaat, kunt u Experience Platform gebruiken om de gegevenslevenscyclus te behandelen. Met het Geavanceerde Beheer van de Levenscyclus van Gegevens, kunt u uw gegevenslevenscyclus op zowel dataset als verslagniveau beheren.

Wanneer u bijvoorbeeld een publiek maakt met het blok met opslagactiviteit in het compositiescanvas, wordt het resulterende publiek als een extern publiek opgeslagen in het datumpeer in Experience Platform. Aangezien dit gegeven **niet** wordt opgeslagen in de Federatieve Samenstelling van het Publiek, worden de publieksgegevens en de overeenkomstige datasets automatisch geschrapt wanneer het publiek in het Portaal van het Publiek wordt geschrapt.

Alternatief, nadat u een profielverrijking door sparen profielactiviteit in het samenstellingscanvas te gebruiken creeert, wordt de resulterende verrijking opgeslagen in Experience Platform als profiel-toegelaten schema en profiel-toegelaten dataset. Hierdoor kunt u de Levenscyclus van gegevens openen en de profielen opschonen.

Voor meer informatie bij het gebruiken van de Levenscyclus van Gegevens, te lezen gelieve het [ overzicht van de Levenscyclus van Gegevens ](https://experienceleague.adobe.com/en/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Labels voor gegevensgebruik {#data-usage-labels}

Met labels voor gegevensgebruik kunt u gegevenssets en velden categoriseren op basis van het beleidsbeleid dat op die gegevens van toepassing is. Nadat u een publiek gebruikend samenstellingen creeert, kunt u de aangewezen gegevensetiketten op het resulterende schema toepassen om het aan de vereiste gebruiksbeperkingen te houden.

Voor meer informatie bij het gebruiken van gegevensetiketten, te lezen gelieve het [ overzicht van de etiketten van het gegevensgebruik ](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Versleuteling {#encryption}

De flexibele Samenstelling van het Publiek verstrekt encryptie door gegeven-bij-rust encryptie, gegeven-in-doorvoerencryptie, en klant-beheerde sleutels.

Gegevens in rust hebben betrekking op de klantgegevens die binnen Federated Audience Composition worden gebruikt. De gegevens worden gecodeerd door het cloudservicebureau en worden in gecodeerde vorm gebruikt in Federated Audience Composition.

De gegevens in doorvoer verwijzen naar de klantengegevens aangezien het zich van één component aan een andere in Federated Audience Composition beweegt. De gegevens blijven versleuteld via Federated Audience Composition-componenten met TLS 1.3 via HTTPS.

Voor meer informatie over hoe Adobe gegevensencryptie behandelt, te lezen gelieve de gids over [ gegevensencryptie in Experience Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Door de klant beheerde sleutels {#customer-managed-keys}

Met door de klant beheerde sleutels hebt u controle over uw gegevens doordat u uw eigen coderingssleutels kunt gebruiken om uw gegevens te coderen. Aangezien de Federatieve Samenstelling van het Publiek **** geen van de klantengegevens opslaat, kunt u klant beheerde sleutels op het resulterende publiek en de verrijking direct gebruiken, aangezien zij in het gegevenshoon op Experience Platform zullen worden opgeslagen.

Voor meer informatie over klant beheerde sleutels, te lezen gelieve de [ klant beheerde sleutelgids ](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Controlelogboek {#audit-log}

Al creeer, lees, werk, en schrappingsverrichtingen bij die in de Samenstelling van de Publiek worden uitgevoerd worden het programma geopend in het auditspoor. U kunt dit controlelogboek gebruiken om deze acties te volgen, verantwoordingsplicht af te dwingen, en nalevingscontroles te steunen.

Voor meer informatie, te lezen gelieve het [ overzicht van het Spoor van de Controle ](/help/admin/audit-trail.md){target="_blank"}.

## Toegangsbeheer {#access-control}

U kunt toegang tot Federated Audience Composition op zowel een gebied als rolgebaseerd niveau controleren. U kunt deze toegangscontroles gebruiken om het beleid van het gegevensbeheer af te dwingen, blootstelling van gevoelige informatie te beperken, en toegang met gebruikersverantwoordelijkheden te richten.

Voor meer informatie over toegangsbeheer in de Federatieve Samenstelling van het Publiek, gelieve te lezen de [ Gids van de Samenstelling van het Publiek Federated van de Toegang ](/help/start/feature-access.md){target="_blank"}.

## Gegevenslokalisatie {#data-localization}

De federated Samenstelling van het publiek slaat **** geen klantengegevens op. Dientengevolge, moet u ervoor zorgen dat u **slechts** uw externe gegevensbestanden met het passende zandbakgebied verbindt om uw gegevens in het zelfde gebied te houden. Als u het gegevensbestand van een verschillend gebied met een zandbak verbindt, is Adobe **niet** verantwoordelijk voor gegevenslocalisatie.

## Volgende stappen {#next-steps}

Nadat u deze handleiding hebt gelezen, hebt u meer inzicht in de privacy- en beveiligingsfuncties die worden gebruikt voor Federated Audience Composition, zoals gegevensbeheer, privacynaleving, handhaving van toestemming, beheer van de gegevenslevenscyclus en toegangscontrole.
