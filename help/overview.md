---
title: Samenstelling federatieve doelgroep
description: Meer informatie over Adobe Federated Audience Composition en hoe u deze kunt gebruiken in downstreamservices zoals Adobe Experience Platform en Adobe Journey Optimizer
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 3%

---

# Samenstelling federatieve doelgroep

Met de Federatieve Audience Composition kunt u een publiek opbouwen en verrijken vanuit uw externe gegevensopslagruimten en het publiek importeren in Adobe Experience Platform. Dit brengt een gemakkelijke en krachtige oplossing om uw entrepot van ondernemingsgegevens direct binnen de stroomafwaartse diensten zoals Adobe Real-Time Customer Data Platform of Adobe Journey Optimizer te verbinden, en vragen op de lijsten van uw gegevenspakhuis uit te voeren. Hierdoor hebt u toegang tot klantgegevens die zijn opgeslagen in gegevenspakhuizen en cloudopslagplatforms zoals Amazon Redshift en Azure Synapse Analytics.

## Mogelijkheden {#rn-capabilities}

Federated Audience Composition breidt de waarde van Real-Time CDP en Journey Optimizer uit met een uitgebreide benadering van publiekscurve en activering:

* **breidt toegang tot kritieke pakhuis-gebaseerde datasets uit om high-value publiek** tot stand te brengen: U kunt bestaande gegevenspakhuizen als belangrijkste systeem van verslag gebruiken, terwijl het leveraging van best-in-klasse toepassingen aan macht grote klantenervaringen.

* **Uitgebreide steun aan de gebruikscase van de machtsovereenkomst**: De Federatieve Samenstelling van het Publiek, die met Real-Time CDP of Journey Optimizer wordt geassocieerd, steunt brand-in werking gestelde, gepersonaliseerde ervaringen met federatief publiek en levert ervaringen in het ogenblik die door gebeurtenissen in real time worden teweeggebracht, die met persoonattributen worden gecombineerd om gebruiksgevalenvereisten over teams te ontmoeten.

* **minimaliseer gegevensbeweging en duplicatie**: U kunt publiek van datasets tot stand brengen die in de entrepots van ondernemingsgegevens leven zonder onderliggende gegevens te kopiëren om actionable marketing profielen en publiek te beheren.

* **gebruik één enkel systeem voor ervaring-gedreven werkschema&#39;s**: U kunt zowel ingebed als gefedereerd publiek in Adobe Experience Platform en coördineert uitgaande ervaringen over alle kanalen tot stand brengen.

* **de steun van de multi-editie**: B2C en B2B CDP de klanten kunnen hefboomwerking Federatieve Samenstelling van het Publiek om op mensen-gebaseerd publiek te bouwen door gegevens van gesteunde opslag van ondernemingsgegevens te integreren. Bovendien kunnen ze bestaande, op mensen gebaseerde Experience Platform-doelgroepen verrijken door de relevante kenmerken die beschikbaar zijn in het Enterprise Data Store op te nemen, waardoor hun publieksprofielen voor meer persoonlijke en doelgerichte betrokkenheid worden verbeterd.

## Gebruiksscenario’s {#use-cases}

De federatieve Samenstelling van het Publiek steunt **drie** categorieën van gebruiksgevallen: publieksverwezenlijking, publieksverrijking, en de verrijking van het klantenprofiel.

* **de verwezenlijking van het publiek**: U kunt publiek van een gegevenspakhuis tot stand brengen en die publiek in Experience Platform voor gebruik in of Real-Time CDP of Journey Optimizer door een tellervriendelijke belemmering-en-dalingsgebruikersinterface federaliseren. Dientengevolge, kunt u uw gegevenspakhuizen vragen zonder gevoelige onderliggende gegevens te kopiëren of bestaande gegevens te dupliceren.
   * **Voorbeeld:** creeer een publiek van hoge waarde voorbij kopers die historische transactiegegevens in het pakhuis gebruiken, zonder die transacties in Experience Platform te kopiëren.

* **de verrijking van het publiek**: U kunt meer detail aan uw bestaand publiek in Experience Platform toevoegen door extra datasets van uw gegevenspakhuizen te gebruiken en uw publiek met deze informatie te bedekken - allen zonder de onderliggende gegevens in Experience Platform te kopiëren. Met de verrijking van het publiek kunt u een verbeterde personalisatie met het verrijkte publiek aanbieden.
   * **Voorbeeld:** verrijkt een publiek van Experience Platform van karretjes verlaten met het Federated publiek van de Samenstelling van het Publiek van hoog-waarde voorbij kopers om een gerichte aanbieding te leveren.

* **de verrijking van het Profiel**: U kunt individuele klantenattributen van uw gegevenspakhuis selecteren om de profielen van Experience Platform te verbeteren. Met gefederaliseerde gegevens die aan deze profielen worden toegevoegd, kunt u betere krachtige ervaringen op het ogenblik die door binnenkomende klantensignalen worden teweeggebracht.
   * **Voorbeeld:** verrijkt een profiel van Experience Platform met informatie van het gefedereerde publiek. U kunt nu een site-bezoeker die tot de waardevolle, in het verleden gefedereerde kopers behoort, een doelaanbieding aanbieden die wordt geactiveerd door hun onsite gedrag.

![&#x200B; diagram &#x200B;](assets/overview/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

Voor meer informatie over het gebruik van de Samenstelling van de Federatieve Audience van de Auditie gelieve te lezen [&#x200B; Verfelijke whitepaper van de Samenstelling van het Publiek &#x200B;](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html).

## Belangrijkste stappen {#gs-steps}

Met Adobe Federated Audience Composition kunt u Adobe Experience Platform-soorten publiek rechtstreeks vanuit uw database maken en bijwerken, zonder dat er iets hoeft te worden ingevoerd.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

1. **creeer een verbinding**: Breng gegevens van diverse bronnen samen, en voeg hen in een verenigde dataset samen. Voor meer informatie bij het verbinden van Adobe Experience Platform apps met uw entrepot van ondernemingsgegevens, gesteunde gegevensbestanden, en het vormen van uw verbinding, lees het [&#x200B; verbindingsoverzicht &#x200B;](./connections/home.md).

2. **Model uw gegevens**: Ontwerp en creeer schema&#39;s en gegevensmodellen die de structuur, de verhoudingen, en de beperkingen van de gegevens bepalen. Voor meer informatie over schema&#39;s, lees het [&#x200B; schemaoverzicht &#x200B;](./data-modelling/schemas.md). Voor meer informatie over gegevensmodellen, lees het [&#x200B; overzicht van het gegevensmodel &#x200B;](./data-modelling/models.md).

3. **zet uw gegevens** om: Pas de technieken van de gegevensmanipulatie toe om het formaat, de structuur, of de waarden van gegevenselementen te wijzigen om hen compatibel of geschikt voor specifieke analyse of toepassingen te maken.

4. **stel uw publiek** samen: Creeer, orkestel en bouw publiek. Voor meer informatie bij het samenstellen van publiek, lees het [&#x200B; samenstellingsoverzicht &#x200B;](./compositions/home.md). U kunt bestaande doelgroepen ook bijwerken of opnieuw gebruiken via het Adobe Experience Platform Audience-portaal en de Doelen. Leer meer op [&#x200B; deze pagina &#x200B;](./connections/destinations.md)

>[!NOTE]
>
>Na het uitvoeren van de samenstelling, wordt het resulterende publiek bewaard in Adobe Experience Platform als extern publiek, en beschikbaar in Adobe Real-Time Customer Data Platform en/of Adobe Journey Optimizer. Het wordt toegankelijk gemaakt in het **publiek** menu. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Bestuur, privacy en veiligheid {#governance-privacy-security}

### Privacyverzoeken {#gov-privacy-requests}

Nadat u een compositie hebt gemaakt, worden de resulterende doelgroepen opgeslagen in Adobe Experience Platform.

U kunt privacyverzoeken om tot profielgegevens toegang te hebben en/of te schrappen die aan deze publiek door Adobe Experience Platform **Privacy Service** beantwoorden, die a [&#x200B; gebruikersinterface &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html){target="_blank"} en [&#x200B; RESTful API &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/overview){target="_blank"} verstrekt om u te helpen verzoeken van klantengegevens beheren.

>[!NOTE]
>
>Voor meer informatie over Privacy Service, verwijs naar de [&#x200B; documentatie van Adobe Experience Platform &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl){target="_blank"}.

U kunt individuele verzoeken tot stand brengen en beheren om tot klantengegevens van de Compositie van de Federatieve Audience van Adobe toegang te hebben en te schrappen. De stappen om **toegangsverzoeken** voor te leggen en **verzoeken** schrappen zijn gedetailleerd in de [&#x200B; documentatie van het Profiel van de Klant in real time &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/profile/privacy){target="_blank"}.

### Audit trail {#gov-audit-trail}

De audittrailcapaciteit verstrekt een gedetailleerd en chronologisch verslag van alle acties en gebeurtenissen die aan uw milieu in real time zijn gemaakt. Om meer over het auditspoor te leren, te lezen gelieve het [&#x200B; overzicht van het controlespoor &#x200B;](./admin/audit-trail.md).

## Meer informatie {#learn}

<!-- Workflow + Workflow activities-->

Leer hoe te om tot de Samenstelling van het Publiek, guardrails en beperkingen op [&#x200B; toegang te hebben deze pagina &#x200B;](./start/access-prerequisites.md).

Voor antwoorden op vaak gestelde vragen, lees [&#x200B; Federated Veelgestelde Veelgestelde Veelgestelde vragen van de Samenstelling van het publiek.](./faq.md)

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Instellingen voor uitvoering"
>abstract="In deze sectie, kunt u montages met betrekking tot de uitvoering van het werkschema vormen, zoals het aantal dagen de samenstellingsgeschiedenis wordt gehouden."

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Activiteit niet bewerkbaar"
>abstract="Wanneer de a **Vraag** of een **Verrijking** activiteit met extra gegevens in de console wordt gevormd, wordt het verrijkingsgegeven genomen en overgegaan in de uitgaande overgang, maar het kan niet worden uitgegeven."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Een koppeling maken"
>abstract="Geef de koppelingsinstellingen op."


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Incrementele query"
>abstract="De **Incrementele vraag** activiteit staat u toe om het gegevensbestand te vragen gebruikend de modelleerling van de Vraag. Telkens wanneer deze activiteit wordt uitgevoerd, worden de resultaten van de vorige uitvoeringen uitgesloten. Zo kunt u doelgericht alleen nieuwe elementen benaderen."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Incrementele querygeschiedenis"
>abstract="Incrementele querygeschiedenis"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Incrementele query verwerkte gegevens"
>abstract="Incrementele query verwerkte gegevens"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="Incrementele querymodus"
>abstract="Met de incrementele query kunt u dezelfde query meerdere keren uitvoeren door de resultaten van vorige uitvoeringen voor elke nieuwe uitvoering uit te sluiten."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="Incrementele querymodus"
>abstract="Met de incrementele query kunt u dezelfde query meerdere keren uitvoeren door alleen de resultaten in aanmerking te nemen als het datumveld later is dan of gelijk is aan de laatste uitvoeringsdatum van de incrementele query-activiteit."

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="Doeldimensie selecteren"
>abstract="Met de doeldimensie kunt u de doelgroep van de actie definiëren: ontvangers, begunstigden van contracten, exploitant, abonnees, enz. Standaard is het doel voor e-mails en SMS geselecteerd in de ingebouwde tabel Ontvangers. Voor pushberichten is de standaarddoeldimensie Subscriber-toepassingen."

