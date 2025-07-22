---
title: Aan de slag met Experience Platform Federated Audience Composition
description: Meer informatie over Adobe Federated Audience Composition en hoe u deze in Adobe Experience Platform kunt gebruiken
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: bb3e01b11d34568b61fdd98eedaa59af5267fd87
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 3%

---

# Aan de slag met Federatieve Audience Composition {#gs-fac}

De Federatieve Samenstelling van het Publiek is beschikbaar voor [ Adobe Real-Time Customer Data Platform ](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home){target="_blank"} en [ Adobe Journey Optimizer ](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/ajo-home){target="_blank"} milieu&#39;s. Zo kunt u een publiek opbouwen en verrijken vanuit uw externe gegevensopslagruimten en het publiek importeren in Adobe Experience Platform. De Federatieve Samenstelling van het Publiek brengt een gemakkelijke en krachtige oplossing om uw entrepot van ondernemingsgegevens direct binnen Adobe Real-Time Customer Data Platform en/of Adobe Journey Optimizer te verbinden, en vragen op de lijsten van uw gegevenspakhuis uit te voeren.

Met Adobe Federated Audience Composition kunnen gebruikers van Adobe Experience Platform-apps toegang krijgen tot hun klantgegevens die zijn opgeslagen in hun gegevenspakhuizen en platforms voor cloudopslag, zoals Amazon Redshift, Azure Synapse Analytics en meer. De gegevens van de klant kunnen in veelvoudige gegevenspakhuizen leven en zijn nu onmiddellijk toegankelijk, zonder replicatie. De gesteunde platforms zijn vermeld op [ deze pagina ](../connections/federated-db.md#supported-db).

>[!INFO]
>
>Volg deze [ stap voor stap gids ](https://experienceleague.adobe.com/en/docs/platform-learn/tutorial-comprehensive-technical/datacollection/module13/fac) om te leren hoe te om publiek tot stand te brengen gebruikend de Federale Samenstelling van het Publiek.

## Mogelijkheden {#rn-capabilities}

Federated Audience Composition breidt de waarde van Real-Time CDP en Journey Optimizer uit met een uitgebreide benadering van publiekscurve en activering:

* Breid toegang tot kritieke pakhuis-gebaseerde datasets uit om een publiek van hoge waarde tot stand te brengen: Gebruikt bestaande gegevenspakhuizen als belangrijkste systeem van verslag, terwijl het leveraging van best-in-klassentoepassingen om grote klantenervaringen te drijven.

* Uitgebreide ondersteuning voor het gebruik van zaken voor betrokkenheid bij energieverbruik: Federated Audience Composition, in combinatie met Real-Time CDP of Journey Optimizer, ondersteunt door het merk geïnitieerde, gepersonaliseerde ervaringen met een federaal publiek en biedt actuele ervaringen die worden geactiveerd door real-time gebeurtenissen, in combinatie met persoonlijke kenmerken om te voldoen aan gebruikscasevereisten voor verschillende teams.

* Minimaliseer gegevensbeweging en duplicatie: maak een publiek op van gegevenssets die in een bedrijfsgegevenspakhuis wonen zonder onderliggende gegevens te kopiëren om handelingsprofielen en publiek te beheren.

* Maak gebruik van één systeem voor ervaren workflows: zorg dat ingeslikte en gefedereerde doelgroepen in Adobe Experience Platform worden gekruld en dat uitgaande ervaringen op alle kanalen worden gecoördineerd.

* B2C en B2B CDP klanten kunnen nu hefboomwerking Federated Audience Composition om op mensen-gebaseerd publiek te bouwen door gegevens van gesteunde opslag van ondernemingsgegevens te integreren. Bovendien kunnen ze bestaande, op mensen gebaseerde AEP-doelgroepen verrijken door de relevante kenmerken die beschikbaar zijn in het Enterprise Data Store op te nemen, waardoor hun publieksprofielen voor meer persoonlijke en doelgerichte betrokkenheid worden verbeterd.

## Gebruiksscenario’s {#use-cases}

De federatieve Samenstelling van het Publiek steunt **drie** categorieën van gebruiksgevallen: publieksverwezenlijking, publieksverrijking, en de verrijking van het klantenprofiel.

* Aanmaken van publiek: u kunt een publiek maken vanuit een gegevenspaket en dat publiek in Experience Platform samenvoegen voor gebruik in Real-Time CDP of Journey Optimizer via een markeerentvriendelijke gebruikersinterface voor slepen en neerzetten. Dientengevolge, kunt u uw gegevenspakhuizen vragen zonder gevoelige onderliggende gegevens te kopiëren of bestaande gegevens te dupliceren.
   * **Voorbeeld:** creeer een publiek van hoge waarde voorbij kopers die historische transactiegegevens in het pakhuis gebruiken, zonder die transacties in Experience Platform te kopiëren.

* Verrijking van het publiek: U kunt meer detail aan uw bestaand publiek in Experience Platform toevoegen door extra datasets van uw gegevenspakhuizen te gebruiken en uw publiek met deze informatie te bedekken - allen zonder de onderliggende gegevens in Experience Platform te kopiëren. Met de verrijking van het publiek kunt u een verbeterde personalisatie met het verrijkte publiek aanbieden.
   * **Voorbeeld:** verrijkt een publiek van Experience Platform van karretjes verlaten met het Federated publiek van de Samenstelling van het Publiek van hoog-waarde voorbij kopers om een gerichte aanbieding te leveren.

* Profielverrijking: u kunt afzonderlijke klantkenmerken selecteren in uw gegevenspaket om Experience Platform-profielen te verbeteren. Met gefederaliseerde gegevens die aan deze profielen worden toegevoegd, kunt u betere krachtige ervaringen op het ogenblik die door binnenkomende klantensignalen worden teweeggebracht.
   * **Voorbeeld:** verrijkt een profiel van Experience Platform met informatie van het gefedereerde publiek. U kunt nu een site-bezoeker die tot de waardevolle, in het verleden gefedereerde kopers behoort, een doelaanbieding aanbieden die wordt geactiveerd door hun onsite gedrag.

![ diagram ](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

Voor meer informatie over het gebruik van de Samenstelling van de Federatieve Audience van de Auditie gelieve te lezen [ Verfelijke whitepaper van de Samenstelling van het Publiek ](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html).

## Belangrijkste stappen {#gs-steps}

Met Adobe Federated Audience Composition kunt u Adobe Experience Platform-soorten publiek rechtstreeks vanuit uw database maken en bijwerken, zonder dat er iets hoeft te worden ingevoerd.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

Belangrijkste stappen:

1. **Integratie van Gegevens**: Breng gegevens van diverse bronnen samen, en voeg hen in een verenigde dataset samen. Leer hoe te om Adobe Experience Platform te verbinden apps en uw entrepot van ondernemingsgegevens, gesteunde gegevensbestanden, en hoe te om hen te vormen zijn gedetailleerd in [ deze sectie ](../connections/federated-db.md).

1. **Modellering van Gegevens**: Ontwerp en creeer gegevensmodellen en schema&#39;s die de structuur, de verhoudingen, en de beperkingen van de gegevens bepalen. Leer meer over schema&#39;s op [ deze pagina ](../customer/schemas.md). Leer hoe te om verbindingen voor uw datamodel op [ tot stand te brengen deze pagina ](../data-management/gs-models.md).

1. **Transformatie van Gegevens**: Pas de technieken van de gegevensmanipulatie toe om het formaat, de structuur, of de waarden van gegevenselementen te wijzigen om hen compatibel of geschikt voor specifieke analyse of toepassingen te maken.

1. **Gebruik van Gegevens**: Creeer, orkestel en bouw publiek. Leer hoe te om publiek op [ deze pagina ](../compositions/gs-compositions.md) samen te stellen. U kunt bestaande doelgroepen ook bijwerken of opnieuw gebruiken via het Adobe Experience Platform Audience-portaal en de Doelen. Leer meer op [ deze pagina ](../connections/destinations.md)

>[!NOTE]
>
>Na het uitvoeren van de samenstelling, wordt het resulterende publiek bewaard in Adobe Experience Platform als extern publiek, en beschikbaar in Adobe Real-Time Customer Data Platform en/of Adobe Journey Optimizer. Het wordt toegankelijk gemaakt in het **publiek** menu. [Meer informatie](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Bestuur, privacy en veiligheid {#governance-privacy-security}

### Privacyverzoeken {#gov-privacy-requests}

Nadat u een compositie hebt gemaakt, worden de resulterende doelgroepen opgeslagen in Adobe Experience Platform.

U kunt privacyverzoeken om tot profielgegevens toegang te hebben en/of te schrappen die aan deze publiek door Adobe Experience Platform **Privacy Service** beantwoorden, die a [ gebruikersinterface ](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html){target="_blank"} en [ RESTful API ](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/overview){target="_blank"} verstrekt om u te helpen verzoeken van klantengegevens beheren.

>[!NOTE]
>
>Voor meer informatie over Privacy Service, verwijs naar de [ documentatie van Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl){target="_blank"}.

U kunt individuele verzoeken tot stand brengen en beheren om tot klantengegevens van de Compositie van de Federatieve Audience van Adobe toegang te hebben en te schrappen. De stappen om **toegangsverzoeken** voor te leggen en **verzoeken** schrappen zijn gedetailleerd in de [ documentatie van het Profiel van de Klant in real time ](https://experienceleague.adobe.com/en/docs/experience-platform/profile/privacy){target="_blank"}.

### Audit trail {#gov-audit-trail}

De mogelijkheden van het audittrail verstrekken een gedetailleerd en chronologisch verslag van alle acties en gebeurtenissen die aan uw milieu in real time zijn gemaakt. [Meer informatie](../admin/audit-trail.md)

## Meer informatie {#learn}

<!-- Workflow + Workflow activities-->


Leer hoe te om tot de Samenstelling van het Publiek, guardrails en beperkingen op [ toegang te hebben deze pagina ](access-prerequisites.md).

Zie ook vaak gestelde vragen op [ deze pagina ](faq.md).


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

