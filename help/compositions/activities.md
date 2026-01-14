---
audience: end-user
title: Overzicht van activiteiten
description: Leer over de verschillende activiteiten en de overgangen beschikbaar voor gebruik binnen de Samenstelling van de Federale Publiek.
source-git-commit: 93f4a16d00c71059672c4c6a51ff36debb6c9cee
workflow-type: tm+mt
source-wordcount: '4594'
ht-degree: 1%

---

# Overzicht van activiteiten

In Federated Audience Composition, kunt u activiteiten en overgangen toevoegen die helpen uw publiek bepalen.

## Activiteiten {#activities}

Met activiteiten kunt u de componenten in het publiek definiëren.

Er zijn **twee** verschillende soorten activiteiten voor gebruik binnen de Federatieve Samenstelling van de Auditie: het richten van activiteiten en de activiteiten van de debietcontrole.

### Targetingactiviteiten {#targeting}

Met doelgerichte activiteiten kunt u definiëren wat uw publiek voor de compositie vormt.

#### publiek opbouwen

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Doelgroep"
>abstract="Selecteer uw publiek."

**bouwt publieksactiviteit** laat u uw doelbevolking voor de samenstelling bepalen. U kunt of een bestaand publiek selecteren of de vraagmodeler gebruiken om uw eigen vraag te bepalen.

+++ Configuratiedetails

Na het toevoegen van **bouwt publiek** activiteit aan het samenstellingscanvas, geef uw publiek een naam. U kunt nu opgeven of u een publiek wilt maken of een bestaand publiek wilt gebruiken.

>[!BEGINTABS]

>[!TAB  creeer nieuw publiek ]

Na het selecteren van **creeer publiek**, kies het **Schema** voor uw publiek. Met het schema kunt u de doelgroep voor de bewerking definiëren, zoals ontvangers, begunstigden van contracten, exploitanten of abonnees. Standaard is het schema geselecteerd bij de ontvangers.

![](./assets/activities/build-audience-create.png)

Na het kiezen van een schema, uitgezochte **gaat** verder. U kunt nu de definitie van uw publiek definiëren in Query Modeler. Voor meer informatie bij het gebruiken van de Vraag Modeler, lees het [ overzicht van Modeler van de Vraag ](../query/home.md).

>[!TAB  Gebruik bestaand publiek ]

Na het selecteren van **Gelezen publiek**, kies **verdergaan**.

![](./assets/activities/build-audience-read.png)

U kunt nu selecteren welk publiek u voor uw samenstelling wilt gebruiken.

>[!ENDTABS]

Nadat u uw opties hebt geselecteerd, kunt u verkiezen om **een uitgaande overgang** te produceren. Als u dit selecteert, kunt u een uitgaande overgang toevoegen die wordt geactiveerd aan het einde van de uitvoering van de activiteit als de doelpopulatie leeg is.

+++

#### Databron wijzigen

De **gegevensbron van de Verandering** activiteit laat u veranderen welke gegevensbron door uw samenstelling wordt gebruikt.

+++ Configuratiedetails

Na het toevoegen van de **gegevensbron van de Verandering** activiteit aan uw samenstellingscanvas, kunt u de gegevensbron bepalen die voor de samenstelling zal worden gebruikt.

![ de gegevensbronoptie wordt benadrukt binnen de Federatieve werkruimte van de Samenstelling van de Publiek.](./assets/activities/configure.png){zoomable="yes"}{width="70%"}

| Bron | Beschrijving |
| ------ | ----------- |
| FDA externe rekening | Een externe cloud-database die is verbonden met Federated Audience Composition. |

Nadat u **[!UICONTROL FDA external account]** hebt geselecteerd, kunt u kiezen met welke externe account u verbinding wilt maken.

![ popover het tonen van de externe rekeningsopties wordt getoond.](./assets/activities/fda-external-account.png){zoomable="yes"}{width="70%"}

+++

#### Dimensie wijzigen

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Schakel hiertoe de optie **[!UICONTROL Generate complement]** in"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Dimensieactiviteit wijzigen"
>abstract="Deze activiteit staat u toe om het schema, dat ook als het richten dimensie wordt bekend te veranderen, aangezien u een publiek bouwt. Het verschuift de as afhankelijk van het gegevensmalplaatje en het inputschema. U kunt bijvoorbeeld van het schema &quot;contracten&quot; overschakelen op het schema &quot;clients&quot;."

De **afmeting van de Verandering** activiteit laat u het schema (ook als het richten afmeting wordt bekend) van uw samenstelling veranderen.

+++ Configuratiedetails

Na het toevoegen van de **dimensie van de Verandering** activiteit aan uw samenstellingscanvas, kunt u een nieuw schema bepalen om het vorige schema te vervangen. Tijdens deze schemawijziging, zullen alle verslagen worden gehouden.

![](./assets/activities/change-dimension.png)

Nadat u de samenstelling uitvoert, zullen uw resultaten worden bijgewerkt.

+++

#### Combineren

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Combineer activiteit"
>abstract="**combineert** activiteit staat u toe om segmentatie op uw binnenkomende bevolking uit te voeren. U kunt dus meerdere populaties combineren, een deel ervan uitsluiten of gegevens alleen gemeenschappelijk houden voor meerdere doelen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Samenvoegopties voor doorsnede"
>abstract="**doorsnede** staat u toe om slechts de elementen gemeenschappelijk voor de verschillende binnenkomende populaties in de activiteit te houden. In de **Reeksen om zich bij** sectie aan te sluiten, controleer alle vorige activiteiten u zich wilt aansluiten bij."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Samenvoegopties voor uitsluiting"
>abstract="De **Uitsluiting** staat u toe om elementen van één bevolking volgens bepaalde criteria uit te sluiten. In de **Reeksen om zich bij** sectie aan te sluiten, controleer alle vorige activiteiten u zich wilt aansluiten bij."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Selecteer het segmentatietype"
>abstract="Selecteer hoe u het publiek wilt combineren: verenigen, doorsnijden of uitsluiten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Afstemmingsopties voor doorsnede"
>abstract="Selecteer het afstemmingstype om te bepalen hoe duplicaten worden verwerkt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Afstemmingsopties"
>abstract="Selecteer het **Type van Verzoening** om te bepalen hoe te om duplicaten te behandelen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Uitsluitingsregels"
>abstract="Indien nodig, kunt u binnenkomende lijsten manipuleren. Immers, om een doel van een ander schema uit te sluiten, dat ook als het richten dimensie wordt bekend, moet dit doel aan het zelfde schema worden teruggekeerd zoals het belangrijkste doel. Om dit te doen, voeg **een regel** in de E **sectie van de uitsluitingsregels** toe en specificeer de voorwaarden van de schemaverandering. Afstemming van gegevens vindt plaats via een attribuut of een join-functie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Te combineren sets selecteren"
>abstract="In de **Reeksen om zich bij** sectie aan te sluiten, selecteer de **Primaire reeks** van de binnenkomende overgangen. Dit is de set waaruit elementen worden uitgesloten. De andere sets komen overeen met de elementen voordat deze worden uitgesloten van de primaire set."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Uitsluitingsregels"
>abstract="Indien nodig, kunt u binnenkomende lijsten manipuleren. Immers, om een doel van een ander schema uit te sluiten, dat ook als het richten dimensie wordt bekend, moet dit doel aan het zelfde schema worden teruggekeerd zoals het belangrijkste doel. Om dit te doen, voeg **een regel** in de **sectie van de Regels van de Uitsluiting** toe en specificeer de voorwaarden van de schemaverandering. Afstemming van gegevens vindt plaats via een attribuut of een join-functie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Combineren genereert een complement"
>abstract="Wisselen op **produceer complementaire** optie om de resterende bevolking in een extra overgang te verwerken."

>[!NOTE]
>
>**combineer** activiteit **moet** na een andere activiteit worden geplaatst en **kan** niet aan het begin van de samenstelling worden geplaatst.

**combineer** activiteit 1} laat u zich bij veelvoudige toehoorders op diverse manieren aansluiten - een unie, een doorsnede, of een uitsluiting.

- **Unie**: Een unie combineert de verschillende soorten publiek in één enkel publiek. Dit is gelijk aan een OR-bewerking.
- **Intersection**: Een doorsnede combineert de verschillende soorten publiek in één enkel publiek met slechts de **gedeelde** inhoud die wordt bewaard. Dit is gelijkwaardig aan een EN verrichting.
- **Uitsluiting**: Een uitsluiting combineert de verschillende soorten publiek in één enkel publiek zonder de gespecificeerde uitsluitingsregels. Dit is gelijk aan een XOR-bewerking.

+++ Configuratiedetails

Na het toevoegen van veelvoudige activiteiten om minstens **twee** verschillende takken te vormen, voeg **** activiteit aan het eind van één van de takken combineren. U kunt nu een van de combinatieopties kiezen: Verenigen, Doorsnede of Uitsluiting.

![](./assets/activities/combine.png)

>[!BEGINTABS]

>[!TAB Samenvoeging]

![](./assets/activities/combine-union.png)

Als u **Unie** selecteert, zult u het **Type van Verzoening** voor de combinatieactiviteit moeten kiezen. Met het afstemmingstype kunt u definiëren hoe dubbele vermeldingen worden verwerkt.

- **Sleutels slechts**: Selecterend **slechts Sleutels** houdt **één** element wanneer de veelvoudige elementen de zelfde sleutel hebben. U kunt deze optie alleen gebruiken als de binnenkomende populaties homogeen zijn.
- **A selectie van kolommen**: Het selecteren van **A selectie van kolommen** laat u een lijst van kolommen bepalen waarop de gegevensverzoening wordt toegepast. U kunt de primaire reeks gegevens selecteren die de brongegevens bevat, die door de kolommen worden gevolgd die voor de verbinding moeten worden gebruikt.

>[!TAB Doorsnede]

![](./assets/activities/combine-intersection.png)

Als u **Intersection** selecteert, zult u het **Type van Afstemming** voor de combinatieactiviteit moeten kiezen. Met het afstemmingstype kunt u definiëren hoe dubbele vermeldingen worden verwerkt.

- **Sleutels slechts**: Selecterend **slechts Sleutels** houdt **één** element wanneer de veelvoudige elementen de zelfde sleutel hebben. U kunt deze optie alleen gebruiken als de binnenkomende populaties homogeen zijn.
- **A selectie van kolommen**: Het selecteren van **A selectie van kolommen** laat u een lijst van kolommen bepalen waarop de gegevensverzoening wordt toegepast.

Na het vormen van uw verzoeningstype, kunt u **ook selecteren vormt complement** optie. Het produceren van een complement verwerkt de resterende bevolking en bevat de gegevens **niet** inbegrepen als deel van de doorsnede. Een extra uitgaande overgang zal aan de activiteit worden toegevoegd.

>[!TAB Uitsluiting]

![](./assets/activities/combine-exclusion.png)

Als u **Uitsluiting** selecteert, zult u de **Primaire reeks** van uw binnenkomende overgangen moeten selecteren. Dit vertegenwoordigt de reeksen waarvan de elementen zullen worden uitgesloten.

Na het kiezen van uw primaire reeks, kunt u opstelling uw **regels van de Uitsluiting**. U kunt of **Gelijke door attribuut** selecteren of **toetreden**.

Zodra u uw uitsluitingsregels hebt gevormd, kunt u **ook selecteren vormt aanvult** optie. Het produceren van een complement verwerkt de resterende bevolking en bevat de gegevens **niet** inbegrepen als deel van de uitsluiting. Een extra uitgaande overgang zal aan de activiteit worden toegevoegd.

+++

#### Deduplicatie

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Velden om duplicaten te identificeren"
>abstract="Selecteer in de sectie **[!UICONTROL Fields to identify duplicates]** de knop **[!UICONTROL Add attribute]** om de velden op te geven waarvoor de duplicaten met identieke waarden kunnen worden geïdentificeerd, zoals: e-mailadres, voornaam, achternaam, enz. In de volgorde van de velden kunt u opgeven welke velden eerst moeten worden verwerkt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Deduplicatieactiviteit"
>abstract="De **Deduplicatie** activiteit staat u toe om duplicaten in de resultaten van de binnenkomende activiteiten te schrappen. Het wordt meestal gebruikt na doelgerichte activiteiten en vóór activiteiten die het gebruik van gerichte gegevens mogelijk maken."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Een complement genereren"
>abstract="U kunt een extra uitgaande overgang met de resterende bevolking produceren, die als duplicaat werd uitgesloten. Schakel hiertoe de optie **[!UICONTROL Generate complement]** in"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Instellingen voor deduplicatie"
>abstract="Als u duplicaten van binnenkomende gegevens wilt verwijderen, definieert u de deduplicatiemethode in de onderstaande velden. Standaard wordt slechts één record bewaard. U moet ook de deduplicatiemodus selecteren op basis van een expressie of een kenmerk. Standaard wordt de record die buiten de duplicaten moet blijven, willekeurig geselecteerd."

De **Deduplicatie** activiteit verwijdert om het even welke dubbele resultaten binnen het publiek.

+++ Configuratiedetails

>[!NOTE]
>
>Als u veelvoudige binnenkomende overgangen hebt, zult u eerst de **Primaire reeks** van dropdown moeten selecteren.

Na het toevoegen van a **Deduplicatie** activiteit, kunt u de gebieden kiezen om duplicaten te identificeren. Selecteer **attributen** toevoegen om de gebieden te identificeren waar de duplicaten kunnen voorkomen.

![](./assets/activities/deduplication.png)

Nadat u de velden hebt geïdentificeerd, kunt u de deduplicatie-instellingen configureren.

| Instelling | Beschrijving |
| ------- | ----------- |
| Duplicaten om te behouden | Het aantal dubbele records dat moet worden bewaard. Als de waarde aan 0 wordt geplaatst, **zullen alle** dubbele verslagen worden bewaard. |
| Deduplicatiemethode | De methode om de dubbele records te verwijderen. <ul><li>**Willekeurige selectie**: Het verwijderde verslag wordt willekeurig gekozen.</li><li>**Gebruikend een uitdrukking**: Het verwijderde verslag is gebaseerd van de voorgelegde uitdrukking. U kunt in oplopende of aflopende volgorde sorteren, afhankelijk van de waarden die u wilt verwijderen.</li><li>**Niet-lege waarden**: Het verwijderde verslag is gebaseerd van de voorgelegde uitdrukking. Records waarvoor de expressie geen waarde heeft, worden verwijderd.</li><li>**na een lijst van waarde**: Het verwijderde verslag is gebaseerd van het voorgelegde gebied of de uitdrukking. U kunt de resterende waarden willekeurig sorteren, in oplopende of aflopende volgorde.</li></ul> |

Bovendien, kunt u **selecteren vormt complementaire** optie. Het produceren van een complementaire processen de resterende bevolking en bevat de gegevens **niet** inbegrepen als deel van deduplicatie. Een extra uitgaande overgang zal aan de activiteit worden toegevoegd.

+++

#### Verrijking

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Verrijkingsactiviteit"
>abstract="De **Verrijking** activiteit staat u toe om de gerichte gegevens met extra informatie van het gegevensbestand te verbeteren. Het wordt algemeen gebruikt in een samenstelling na segmentatieactiviteiten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Verrijkingsactiviteit"
>abstract="Zodra de verrijkingsgegevens aan de samenstelling zijn toegevoegd, kan het in de activiteiten worden gebruikt die na de **Verrijking** activiteit aan segmentprofielen in verschillende groepen worden toegevoegd die op hun gedrag, voorkeur, en keuzen worden gebaseerd."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Koppelingsdefinitie"
>abstract="Maak een koppeling tussen de gegevens van de werktabel en de gefedereerde database."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Verrijkingsverzoening"
>abstract="Stel de afstemmingsparameters in."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Verrijkingsgegevens"
>abstract="Selecteer de gegevens die u wilt gebruiken om uw compositie te verrijken. U kunt twee soorten verrijkingsgegevens selecteren: één enkel verrijkingsattribuut van het schema, dat ook als het richten van afmeting wordt bekend, of een inzamelingsverbinding, die een verbinding met een 1-N kardinaliteit tussen lijsten is."

De **Verrijking** activiteit laat u uw samenstelling verbeteren door extra gegevens van uw gefedereerd gegevensbestand toe te voegen.

Als u een verbinding aan de Federatieve bestemming van de Samenstelling van het Publiek hebt gevormd, kunt u de activiteit van de Verrijking gebruiken om gegevens te verrijken die Adobe Experience Platform met attributen van uw extern gegevensbestand komen. [ Leer hoe te om het publiek van Adobe Experience Platform met externe gegevens te verrijken ](../connections/destinations.md)

+++ Configuratiedetails

>[!NOTE]
>
>Als u veelvoudige binnenkomende overgangen hebt, zult u eerst de **Primaire reeks** van dropdown moeten selecteren.

Na het toevoegen van de **Verrijking** activiteit aan uw samenstelling, kunt u **selecteren verrijkingsgegevens** toevoegen om te kiezen welke attributen u wilt gebruiken om uw samenstelling te verrijken. U kunt **selecteren geef uitdrukking** uit om een geavanceerde uitdrukking te bouwen om de attributen te selecteren.

![](./assets/activities/enrichment.png)

+++

#### Afstemming

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
>abstract="Door gebrek, worden de niet in overeenstemming gebrachte gegevens gehouden in de uitgaande overgang en beschikbaar in de werklijst voor toekomstig gebruik. Om unconiled gegevens te verwijderen, deactiveer **houden unconiled gegevens** optie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Afstemmingskenmerk"
>abstract="Selecteer het kenmerk dat u wilt gebruiken om gegevens met elkaar te verzoenen en bevestig de gegevens."

>[!NOTE]
>
>Standaard worden niet-compatibele gegevens bewaard in de uitgaande overgang en zijn deze beschikbaar in de werktabel voor toekomstig gebruik. Als u **niet** samengevoegde gegevens wilt worden gebruikt, deactiveer de **Levende onverzoenbare gegevens** optie.

De **Verzoening** activiteit laat u het verband tussen gegevens in uw gefedereerde gegevensbestand aan de gegevens in een het werklijst bepalen.

+++ Configuratiedetails

Na het toevoegen van de **Verzoening** activiteit aan uw samenstelling, kunt u kiezen welk schema voor de verzoening te gebruiken.

Zodra u het schema hebt gekozen, zult u opstelling uw verzoeningsregels moeten. U kunt tussen **Eenvoudige attributen** of **Geavanceerde verzoeningsvoorwaarden** kiezen.

>[!BEGINTABS]

>[!TAB  Eenvoudige attributen ]

Na het kiezen van **Eenvoudige attributen**, uitgezocht **voeg regel** toe. U kunt opstelling uw verzoening nu door de **Source** en **gebieden van de Bestemming** toe te voegen. Het **gebied van de Bestemming** beantwoordt aan de gebieden van het geselecteerde schema.

![](./assets/activities/reconciliation-rules.png)

Gegevens worden in overeenstemming gebracht wanneer de bron en het doel gelijk zijn. U kunt meer verzoeningscriteria toevoegen door **te selecteren voegt regel** toe. Als de veelvoudige toetreden voorwaarden worden gespecificeerd, **alle** van hen moeten worden geverifieerd zodat kunnen de gegevens samen worden verbonden.

>[!TAB  Geavanceerde verzoeningsvoorwaarden ]

Na het kiezen van **Geavanceerde verzoeningsvoorwaarden**, uitgezochte **creeer voorwaarden**. U kunt nu uw eigen verzoeningsvoorwaarde maken met de querymodelfunctie. Voor meer informatie bij het gebruiken van de Vraag Modeler, lees het [ overzicht van Modeler van de Vraag ](../query/home.md)

![](./assets/activities/reconciliation-advanced.png)

>[!ENDTABS]

U kunt ook de gegevens filteren die met elkaar in overeenstemming zijn. Selecteer **creeer filter** om een douanetoewijzing tot stand te brengen gebruikend de Vraag Modeler. Voor meer informatie bij het gebruiken van de Vraag Modeler, lees het [ overzicht van Modeler van de Vraag ](../query/home.md)

+++

#### Doelgroep opslaan

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
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Meer informatie in de documentatie van Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Naamruimte identiteit"
>abstract="Selecteer de naamruimte die u wilt gebruiken voor profielen."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces" text="Meer informatie in de documentatie van Experience Platform"

>[!IMPORTANT]
>
>Als uw zandbak de belangrijkheid van de a **dataset** samenvoegbeleid gebruikt, gelieve de Zorg van de Klant van Adobe te contacteren om de `Halos UPS` dataset aan uw fusiebeleid toe te voegen.
>
>Voor meer informatie over fusiebeleid, te lezen gelieve het [ overzicht van het samenvoegbeleid ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview).

**sparen publiek** activiteit laat u een publiek tot stand brengen dat van de samenstelling wordt gebaseerd. Zodra het publiek is gecreeerd, kunt u hen binnen het Portaal van het Publiek in Adobe Experience Platform gebruiken. Voor meer informatie bij het gebruiken van publiek met de Federatieve Samenstelling van het Publiek, lees het [ overzicht van publiek ](../start/audiences.md). Voor meer informatie over publiek in Experience Platform, lees het [ Poortoverzicht van het Poortpubliek van het Publiek ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}.

+++ Configuratiedetails

>[!IMPORTANT]
>
>De naam van het publiek **moet** binnen de huidige zandbak uniek zijn en kan niet de zelfde naam zoals om het even welk bestaand publiek hebben.

Na het toevoegen van **sparen publiek** activiteit aan uw samenstelling, kunt u de naam van uw pas gecreeerd publiek specificeren.

![](./assets/activities/save-audience.png)

Nu kunt u uw toewijzingen opgeven om te selecteren welke velden u wilt overbrengen naar het nieuwe publiek. Selecteer **Toewijzing van het publiek** toevoegen en de bron en doelpublieksgebieden kiezen, die zo vaak als nodig herhalen.

Nadat u de toewijzingen hebt toegevoegd, kunt u de primaire identiteit en naamruimte selecteren om de doelprofielen in de database te identificeren. Het primaire identiteitsveld wordt gebruikt om de profielen te identificeren terwijl de naamruimte van de identiteit fungeert als een sleutel om de identiteit te identificeren.

+++

#### Splitsen

>[!CONTEXTUALHELP]
>id="dc_orchestration_split"
>title="Gesplitste activiteit"
>abstract="De **Gesplitste** activiteit staat u toe om inkomende populaties in veelvoudige subsets te segmenteren die op verschillende selectiecriteria, zoals het filtreren regels of populatiegrootte worden gebaseerd."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_segments"
>title="Segmenten voor splitsingsactiviteit"
>abstract="Voeg zoveel subsets toe als u wilt om de binnenkomende populatie te segmenteren.<br/></br> wanneer de **Gesplitste** activiteit wordt uitgevoerd, wordt de bevolking gesegmenteerd over de verschillende ondergroepen in de orde zij aan de activiteit worden toegevoegd. Voordat u de compositie start, moet u ervoor zorgen dat u de subsets in de gewenste volgorde hebt geplaatst met de pijlknoppen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_filter"
>title="Activiteitsfilter splitsen"
>abstract="Als u een filtervoorwaarde op de subset wilt toepassen, selecteert u **[!UICONTROL Create filter]** en configureert u de gewenste filterregel met de querymodelfunctie. Neem bijvoorbeeld profielen op van de binnenkomende populatie waarvan het e-mailadres voorkomt in de database."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_limit"
>title="Limiet voor gesplitste activiteit"
>abstract="Als u het aantal profielen wilt beperken dat door de subset wordt geselecteerd, schakelt u de optie **[!UICONTROL Enable limit]** in en geeft u het aantal of de percentages van de populatie op die u wilt opnemen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_sorting"
>title="Splitsen op activiteit"
>abstract="Wanneer u een populatielimiet voor een subset instelt, kunt u de geselecteerde profielen op basis van een specifiek profielkenmerk in oplopende of aflopende volgorde rangschikken. Om dit te doen, knevel op **het sorteren** optie toe. U kunt bijvoorbeeld een subset beperken tot alleen de bovenste 50 profielen met het hoogste aankoopbedrag."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_complement"
>title="Splitsen genereert complement"
>abstract="Zodra u alle subsets hebt gevormd, kunt u de resterende populatie selecteren die geen van de subsets aanpast en hen in een extra uitgaande overgang omvat. Om dit te doen, op **van een knevel te voorzien produceert complement** optie."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_generatesubsets"
>title="Alle subsets in dezelfde tabel genereren"
>abstract="Schakel deze optie in en uit om alle subsets te groeperen in één uitvoerovergang."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_emptytransition"
>title="Lege overgang overslaan"
>abstract="Schakel de optie **[!UICONTROL Skip empty transition]** in en uit om de uitvoerovergang voor deze subset uit te schakelen als de binnenkomende populatie leeg is."

>[!CONTEXTUALHELP]
>id="dc_orchestration_split_enable_overlapping"
>title="Overlappende uitvoerpopulaties inschakelen"
>abstract="Met de optie **[!UICONTROL Enable overlapping of output populations]** kunt u populaties beheren die tot verschillende subsets behoren. Wanneer het vakje niet wordt gecontroleerd, zorgt de gespleten activiteit ervoor een ontvanger niet in verscheidene outputovergangen kan aanwezig zijn, zelfs als het aan de criteria van verscheidene subsets voldoet. Deze worden als doel ingesteld op het eerste tabblad met overeenkomende criteria. Als het selectievakje is ingeschakeld, kunnen de ontvangers in verschillende subsets worden gevonden als ze voldoen aan hun filtercriteria. "

De **Gesplitste** activiteit scheidt de inkomende bevolking in veelvoudige delen, afhankelijk van de bepaalde criteria.

+++ Configuratiedetails

>[!IMPORTANT]
>
>Wanneer de **Gesplitste** activiteit wordt uitgevoerd, wordt de bevolking gescheiden over de verschillende ondergroepen in de **orde zij** toegevoegd. Als de eerste subset bijvoorbeeld 70% van de oorspronkelijke populatie splitst, past de volgende subset zijn selectiecriteria toe op de resterende 30%.
>
>Voordat u de compositie uitvoert, moet u ervoor zorgen dat u de subsets hebt geordend in de volgorde waarin u de splitsingen wilt uitvoeren.

Na het toevoegen van de **Gesplitste** activiteit aan uw samenstelling, kunt u nu bepalen hoe te om uw publiek te onderdrukken. Selecteer **segment** toevoegen om uw verschillende vertakkende wegen tot stand te brengen.

U kunt nu details voor elk van deze subpaden opgeven. U kunt het subpad een naam en filtervoorwaarden geven. Om een het filtreren voorwaarde tot stand te brengen, creeer **filter** en vorm de het filtreren regel gebruikend de Vraag Modeler. Voor meer informatie bij het gebruiken van de Vraag Modeler, lees het [ overzicht van Modeler van de Vraag ](../query/home.md).

Zodra u uw het filtreren voorwaarde hebt gecreeerd, kunt u de volgende extra regels toepassen:

- **laat grens** toe: Beperkt het aantal profielen die worden toegestaan om in de ondergroep worden verdeeld. U kunt dit instellen als een getal of als een percentage van de populatie.
   - Als u een limiet inschakelt, kunt u de geselecteerde profielen ook rangschikken op basis van een specifiek profielkenmerk. Zet **toe laat het sorteren**, en u kunt de attributen in het stijgen of dalende orde sorteren.
- **Overslaan lege overgang**: Maakt de overgang onbruikbaar als de inkomende bevolking leeg is.

Nu de subsets zijn geconfigureerd, kunt u nog een aantal extra opties instellen.

| Opties | Beschrijving |
| ------- | ----------- |
| **produceer complement** | Creeert een uitgaande overgang die de resterende bevolking bevat. |
| **laat overlapping van outputpopulaties** toe | Indien toegelaten, kan de ontvanger **niet** in veelvoudige uitgaande overgangen aanwezig zijn en zal **slechts** in de eerste uitgaande overgang aanwezig zijn. Als gehandicapt, kan de ontvanger **** in veelvoudige uitgaande overgangen verschijnen. |
| **produceer alle ondergroepen in de zelfde lijst** | Hiermee groepeert u alle subsets in één uitgaande overgang. |

+++

### Workflowbeheeractiviteiten {#flow-control}

Met behulp van stroombeheeractiviteiten kunt u de organisatie en coördinatie van uw compositie definiëren.

#### en verbinden

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join-activiteit"
>abstract="De **en-sluit zich aan** activiteit staat u toe om veelvoudige uitvoertakken van een samenstelling te synchroniseren. De regeling wordt in werking gesteld zodra alle voorgaande activiteiten zijn beëindigd. Dit staat u toe om ervoor te zorgen dat bepaalde activiteiten alvorens de samenstelling te blijven uitvoeren worden gebeëindigd."

De **EN-sluit zich** activiteit aan laat u veelvoudige takken van een samenstelling samen combineren. Deze activiteit wordt slechts teweeggebracht zodra **allen** de binnenkomende overgangen worden geactiveerd.

+++ Configuratiedetails

Nadat u veelvoudige activiteiten aan vorm minstens twee verschillende takken hebt toegevoegd, kunt u **EN** activiteit toevoegen aan het eind van om het even welke takken.

![](./assets/activities/and-join.png)

Binnen de **het samenvoegen opties** sectie, kunt u alle activiteiten selecteren u wilt synchroniseren. Bovendien, kunt u kiezen welke binnenkomende overgang om binnen de **Primaire reeks** dropdown te houden.

+++

#### Einde

De **activiteit van het 0} Eind {merkt grafisch het eind van de samenstelling en heeft geen functioneel effect.**

#### Vertakking

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork"
>title="Vorkactiviteit"
>abstract="De **activiteit 0} van het Vonk {staat u toe om uitgaande overgangen tot stand te brengen om verscheidene activiteiten tezelfdertijd te beginnen.**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_fork_transitions"
>title="Overgangen naar vorkactiviteit"
>abstract="Door gebrek, worden twee overgangen gecreeerd met de activiteit van het a **Fork**. Selecteer **overgangsknoop** toevoegen om een extra uitgaande overgang te bepalen, en zijn etiket in te gaan."

De **1} activiteit van het Vonk {laat u veelvoudige uitgaande overgangen tot stand brengen die gelijktijdig veelvoudige activiteiten beginnen.**

+++ Configuratiedetails

Zodra u de **activiteit 0} van het Vonk {aan uw samenstelling hebt toegevoegd, worden twee uitgaande overgangen automatisch geproduceerd.** U kunt deze uitgaande overgangen een naam geven. Bovendien, kunt u **selecteren voeg overgang** toe om een andere uitgaande overgang toe te voegen.

![](./assets/activities/fork.png)

+++

#### Planner

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Planningsactiviteit"
>abstract="De **Planner** activiteit staat u toe om te plannen wanneer de publiekssamenstelling begonnen wordt. Deze activiteit moet worden beschouwd als een geplande start. Het kan slechts als eerste activiteit van een samenstelling worden gebruikt."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Geldigheid van planner"
>abstract="U kunt een geldigheidsperiode voor de planner bepalen. Deze kan permanent zijn (standaard) of geldig zijn tot een bepaalde datum."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Planningsopties"
>abstract="Bepaal de frequentie van de planner. Het kan op een specifiek moment, één keer of verscheidene keren per dag, week of maand worden uitgevoerd."

De **Planner** activiteit laat u plannen wanneer om de uitvoering van de samenstelling te beginnen. U **moet** dit als eerste activiteit van de samenstelling gebruiken.

+++ Configuratiedetails

Na het toevoegen van de **Planner** activiteit aan uw samenstelling, kunt u de **frequentie van de Uitvoering** voor de samenstelling plaatsen. De opties omvatten **eens**, **Dagelijks**, **verscheidene tijden a dag**, **wekelijks**, en **maandelijks**.

>[!BEGINTABS]

>[!TAB  Eenmaal ]

>[!NOTE]
>
>De tijd wordt ingesteld op UTC.

Als u **** eens selecteert, wordt de samenstelling slechts eenmaal uitgevoerd. U kunt de datum en het tijdstip selecteren waarop de compositie wordt uitgevoerd.

>[!TAB  Dagelijks ]

Als u **Dagelijks** selecteert, wordt de samenstelling één keer per dag uitgevoerd. Nochtans, kunt u welke dag van de maand de samenstelling onder de **Dag van de maand** sectie wordt uitgevoerd. De mogelijke waarden omvatten **Elke dag**, **Op weekdagen**, **door een geselecteerde periode**, en **Geselecteerde dagen van de week**.

| Dag van de maand | Beschrijving |
| ---------------- | ----------- |
| Elke dag | De samenstelling wordt uitgevoerd elke dag. |
| Op weekdagen | De compositie wordt elke weekdag uitgevoerd. |
| Via een geselecteerde periode | De samenstelling wordt uitgevoerd elke dag door de geselecteerde periode. U kunt de lengte van de herhalingsperiode en de datum waarop de periode begint, instellen. |
| Geselecteerde weekdagen | De samenstelling wordt uitgevoerd elke dag van de week die wordt geselecteerd. |

Na het kiezen van welke dag van de maand het programma zal lopen, kunt u **lanceringstijden van de Voorproef** selecteren om het programma van volgende tien uitvoeringen van uw samenstelling te controleren.

>[!TAB  verscheidene tijden a dag ]

Als u **meerdere keren per dag** selecteert, wordt de samenstelling uitgevoerd veelvoudige tijden per dag. U kunt kiezen of de samenstelling op specifieke tijden per dag of periodiek op vastgestelde tijden wordt uitgevoerd.

Als u **Geselecteerde uren** selecteert, kunt u de specifieke tijden kiezen de samenstelling zal lopen. Als u **Periodiek** selecteert, kunt u kiezen hoe vaak de samenstelling in of uren of notulen zal lopen en tussen welke tijden het zal lopen. Alle tijden zijn in UTC.

Na uitgezocht de uren, kunt u kiezen hoe vaak de uitvoering onder de **Dag van de maand** sectie in werking wordt gesteld.

| Dag van de maand | Beschrijving |
| ---------------- | ----------- |
| Elke dag van de week | De samenstelling wordt uitgevoerd elke dag. |
| Op bepaalde dagen van de week | De samenstelling wordt uitgevoerd elke dag van de week die wordt geselecteerd. |

Na het kiezen van welke dag van de maand het programma zal lopen, kunt u **lanceringstijden van de Voorproef** selecteren om het programma van volgende tien uitvoeringen van uw samenstelling te controleren.

>[!TAB  Wekelijks ]

Als u **wekelijks** selecteert, wordt de samenstelling uitgevoerd op de wekelijkse frequentie die wordt geplaatst. Als u de wekelijkse frequentie instelt op een getal dat groter is dan 1, kunt u ook de datum kiezen vanaf wanneer de uitvoering begint.

Na het kiezen van de evaluatiefrequentie, kunt u kiezen hoe vaak de uitvoering onder de **Dag van de maand** sectie in werking wordt gesteld.

| Dag van de maand | Beschrijving |
| ---------------- | ----------- |
| Elke dag van de week | De samenstelling wordt uitgevoerd elke dag. |
| Op bepaalde dagen van de week | De samenstelling wordt uitgevoerd elke dag van de week die wordt geselecteerd. |

Na het kiezen van welke dag van de maand het programma zal lopen, kunt u **lanceringstijden van de Voorproef** selecteren om het programma van volgende tien uitvoeringen van uw samenstelling te controleren.

>[!TAB  Maandelijks ]

Als u **Maandelijks** selecteert, wordt de samenstelling uitgevoerd op de maandelijkse frequentie die wordt geplaatst. U kunt instellen dat dit elke maand of op bepaalde maanden gebeurt.

Na het kiezen van de maandelijkse frequentie, kunt u de **Dag van de maand** kiezen de uitvoering in werking wordt gesteld.

| Dag van de maand | Beschrijving |
| ---------------- | ----------- |
| Elke dag | De samenstelling wordt uitgevoerd elke dag. |
| Op weekdagen | De compositie wordt elke weekdag uitgevoerd. |
| Via een geselecteerde periode | De samenstelling wordt uitgevoerd elke dag door de geselecteerde periode. U kunt de lengte van de herhalingsperiode en de datum waarop de periode begint, instellen. |
| Geselecteerde weekdagen | De samenstelling wordt uitgevoerd elke dag van de week die wordt geselecteerd. |

Zodra u de **Dag van de maand** plaatst, kunt u de begintijd kiezen. Alle tijden zijn in UTC.

>[!ENDTABS]

Na het selecteren van de uitvoeringsfrequentie, kunt u de **periode van de Geldigheid** van het programma kiezen.

| Geldigheidsperiode | Beschrijving |
| --------------- | ----------- |
| **Permanent (verloopt nooit)** | De compositie zal nooit verlopen. |
| **de periode van de Geldigheid** | De samenstelling zal tussen de bepaalde data lopen. |

+++

#### Wachten

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Wachtactiviteit"
>abstract="**wacht** activiteit wordt gebruikt om de overgang van een activiteit aan een andere te vertragen."

**wacht** activiteit pauzeert de uitvoering van de samenstelling voor de gespecificeerde hoeveelheid tijd.

+++ Configuratiedetails

Nadat u **toevoegt wacht** activiteit aan uw samenstelling, kunt u het of a **Duur** of a **Vaste tijd** maken wachten.

![](./assets/activities/wait.png)

Als u duur selecteert, kunt u de te wachten periode instellen. Deze periode kan in seconden, minuten, uren, of dagen zijn.

Als u vaste tijd selecteert, kunt u de samenstelling plaatsen om tot de bepaalde datum en de tijd te wachten. De tijd wordt geplaatst aan uw **lokale tijdzone**.

+++

## Overgangen {#transitions}

In composities tonen overgangen hoe gegevens van de ene activiteit naar de andere worden overgebracht. De overgangen slaan de gegevens in een tijdelijke het werklijst op. Als u de overgang selecteert, kunt u de volgende informatie weergeven:

- **schema van de Voorproef**: U kunt dit selecteren om het schema voor de het werklijst te bekijken.
- **Resultaten van de Voorproef**: U kunt dit selecteren om de gegevens te visualiseren die in de geselecteerde overgang worden vervoerd. Deze optie is slechts beschikbaar als **het resultaat van tussentijdse populaties tussen twee uitvoeringen** houden wordt toegelaten.

![](assets/transition-preview.png)

## Volgende stappen {#next-steps}

Na het lezen van deze gids, zult u een beter inzicht in de activiteiten en de overgangen hebben u binnen een samenstelling kunt gebruiken. Voor meer informatie over samenstellingen in het algemeen, lees het [ samenstellingsoverzicht ](./create-composition.md).
