---
audience: end-user
title: Bouw uw eerste vraag gebruikend de vraagmodeler
description: Leer hoe te om uw eerste vraag in de vraagmodeler te bouwen
source-git-commit: 96b578cab1ce328b7db5043539e3b58fa238ebfd
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# Uw eerste query samenstellen {#build-query}

Om te beginnen bouwend een vraag, heb toegang tot de vraagmodeler van de plaats van uw keus, afhankelijk van de actie u wilt uitvoeren. Het Query-model wordt geopend met een leeg canvas. Klik op de knop **+** knoop om de eerste knoop van uw vraag te vormen.

U kunt twee typen elementen toevoegen:

* **Componenten filteren** (De voorwaarde van de Douane, Uitgezochte publiek, Vooraf bepaald filter) staat u toe om uw eigen regels te bouwen, een publiek of een vooraf bepaald filter te selecteren om uw vraag te verfijnen. Zij worden toegevoegd bij het begin van uw vraag en op gestippelde overgangen. [Leer hoe u met filtercomponenten werkt](#filtering)

  Voorbeeld: *Ontvangers die zich hebben geabonneerd op de nieuwsbrief &#39;Sport&#39;*. *Ontvangers in New York*, *Ontvangers in San Francisco*

  ![](assets/query-add-component.png){zoomable="yes"}

* **Groepoperatoren** (EN, OF, BEHALVE) staat u toe om het filtreren componenten in het diagram te groeperen. Ze worden toegevoegd op bestaande overgangen vóór een filtercomponent. [Leer werken met operatoren](#filtering)

  Voorbeeld: *Ontvangers die zich hebben geabonneerd op de nieuwsbrief &quot;Sport&quot;**EN**die in New York wonen **OF**San Francisco*.

  ![](assets/query-add-operator.png){zoomable="yes"}

## Filtercomponenten toevoegen {#filtering}

Door componenten te filteren kunt u de query verfijnen door:

* **[Aangepaste voorwaarden](#custom-condition)**: Filter uw query door uw eigen voorwaarde te maken met kenmerken uit de database en geavanceerde expressies.
* **[Soorten publiek](#audiences)**: Filter de query met een bestaand publiek.
* **[Vooraf gedefinieerd filter](#predefined-filters)**: Filter de query met behulp van bestaande vooraf gedefinieerde filters.

### Een aangepaste voorwaarde configureren {#custom-condition}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_customcondition"
>title="Aangepaste voorwaarde"
>abstract="De voorwaarden van de douane zijn het filtreren componenten die u toestaan om uw vraag te filtreren door uw eigen voorwaarde met attributen van het gegevensbestand en geavanceerde uitdrukkingen te bouwen."

Voer de volgende stappen uit om de query te filteren met behulp van een aangepaste voorwaarde:

1. Klik op de knop **+** op de gewenste knoop en selecteer **[!UICONTROL Custom condition]**. Het deelvenster Eigenschappen voor aangepaste voorwaarde wordt aan de rechterkant geopend.

1. In de **Kenmerk** Selecteer in de database het kenmerk dat u wilt gebruiken om de voorwaarde te maken. De lijst met kenmerken bevat alle kenmerken van uw database, inclusief kenmerken van gekoppelde tabellen.

   ![](assets/query-custom-condition-fields.png){zoomable="yes"}

   >[!NOTE]
   >
   >De **Expressie bewerken** staat u toe aan hefboomwerking de de uitdrukkingsredacteur van het Web om een uitdrukking manueel te bepalen gebruikend gebieden van het gegevensbestand en hulpfuncties. [Leer hoe u expressies kunt bewerken](expression-editor.md)

1. Selecteer in de vervolgkeuzelijst de operator die u wilt toepassen. Er zijn verschillende operatoren beschikbaar voor gebruik. De operatoren in de vervolgkeuzelijst zijn afhankelijk van het gegevenstype van het kenmerk.

   +++Lijst met beschikbare operatoren

   | Operator | Doel | Voorbeeld |
   |  ---  |  ---  |  ---  |
   | Gelijk aan | Retourneert een resultaat dat identiek is aan de gegevens die zijn ingevoerd in de tweede kolom Waarde. | Achternaam (@lastName) gelijk aan &#39;Jones&#39; retourneert alleen ontvangers met als achternaam Jones. |
   | Niet gelijk aan | Retourneert alle waarden die niet identiek zijn aan de ingevoerde waarde. | Taal (@taal) gelijk aan &#39;Engels&#39; |
   | Groter dan | Retourneert een waarde die groter is dan de ingevoerde waarde. | Leeftijd (@leeftijd) groter dan 50</strong>alle waarden boven &quot;50&quot;, d.w.z. &quot;51&quot;, &quot;52&quot; enz. |
   | Minder dan | Retourneert een waarde die kleiner is dan de ingevoerde waarde. | Aanmaakdatum (@created) vóór &#39;DaysAgo(100)&#39;</strong>, worden alle ontvangers geretourneerd die minder dan 100 dagen geleden zijn gemaakt. |
   | Groter dan of gelijk aan | Retourneert alle waarden die gelijk zijn aan of groter zijn dan de ingevoerde waarde. | Leeftijd (@leeftijd) groter dan of gelijk aan &#39;30&#39;</strong>, worden alle ontvangers vanaf 30 jaar geretourneerd. |
   | Kleiner dan of gelijk aan | Retourneert alle waarden die gelijk zijn aan of lager zijn dan de ingevoerde waarde. | Leeftijd (@leeftijd) kleiner dan of gelijk aan &#39;60&#39;</strong>, worden alle ontvangers vanaf 60 jaar geretourneerd. |
   | Opgenomen in | Retourneert resultaten die zijn opgenomen in de aangegeven waarden. Deze waarden moeten door een komma worden gescheiden. | De geboortedatum (@geboortedatum) is opgenomen in &quot;12/10/1979,12/10/1984&quot; en retourneert de tussen deze data geboren ontvangers. |
   | Niet in | Werkt zoals is opgenomen in operator. Hier, willen wij ontvangers uitsluiten die op de ingegane waarden worden gebaseerd. | Geboortedatum (@geboortedatum) is niet opgenomen in &quot;10-12-1979,12-10-1984&quot;. Anders dan in het vorige voorbeeld worden ontvangers die binnen deze datums geboren zijn, niet geretourneerd. |
   | Is leeg | In dit geval komt het resultaat dat we zoeken overeen met een lege waarde in de tweede kolom Waarde. | Mobiele (@mobilePhone) is leeg en retourneert alle ontvangers die geen mobiel nummer hebben. |
   | Is niet leeg | Werkt in omgekeerde volgorde naar de operator Is leeg. Het is niet nodig gegevens in te voeren in de tweede kolom Waarde. | E-mail (@email) is niet leeg. |
   | Begint met | Retourneert de resultaten die beginnen met de ingevoerde waarde. | Account # (@account) begint met &#39;32010&#39;. |
   | Begint niet met | Retourneert de resultaten die niet beginnen met de ingevoerde waarde. | Account # (@account) begint niet met &#39;20&#39; |
   | Bevat | Retourneert de resultaten die ten minste de ingevoerde waarde bevatten. | E-maildomein (@domein) bevat &#39;mail&#39;</strong>, worden alle domeinnamen geretourneerd die &#39;mail&#39; bevatten. Het domein &#39;gmail.com&#39; wordt dus ook geretourneerd. |
   | Bevat niet | Retourneert resultaten die niet de ingevoerde waarde bevatten. | E-maildomein (@domain) bevat geen &#39;vo&#39;</strong>. In dit geval worden domeinnamen die &#39;vo&#39; bevatten, niet geretourneerd. De domeinnaam voila.fr wordt niet weergegeven in de resultaten. |
   | leuk | Net als de Contains-operator. Hiermee kunt u een jokerteken % in de waarde invoegen. | Achternaam (@lastName) zoals &#39;Jon%s&#39;. Hier wordt het jokerteken gebruikt als een joker om de naam Jones te vinden, mocht de operator de ontbrekende letter tussen de &#39;n&#39; en &#39;s&#39; vergeten hebben. |
   | Niet leuk | Net als de Contains-operator. Hiermee kunt u een jokerteken % in de waarde invoegen. | Achternaam (@lastName) houdt niet van &#39;Smi%h&#39;. Hier worden de ontvangers met de achternaam &#39;Smi%h&#39; niet geretourneerd. |

+++

1. In de **Waarde** -veld, definieert u de verwachte waarde. U kunt de de uitdrukkingsredacteur van het Web ook hefboomwerking om een uitdrukking manueel te bepalen gebruikend gebieden van het gegevensbestand en hulpfuncties. Om dit te doen, klik **Expressie bewerken** knop. [Leer hoe u expressies kunt bewerken](expression-editor.md)

   *Voorbeeld van query met alle profielen van 21 jaar of ouder:*

   ![](assets/query-custom-condition.png){zoomable="yes"}

   Voor datatype-kenmerken zijn vooraf gedefinieerde waarden beschikbaar via de **[!UICONTROL Presets]** -optie.

   ![](assets/date-presets.png){zoomable="yes"}

#### Aangepaste voorwaarden voor gekoppelde tabellen (1-1 en 1-N koppelingen){#links}

De voorwaarden van de douane staan u toe om lijsten te vragen verbonden aan de lijst die momenteel door uw regel wordt gebruikt. Dit omvat lijsten met een 1-1 kardinaliteitsverbinding, of inzamelingstabellen (verbinding 1-N).

Voor een **1-1 link**, navigeert u naar de gekoppelde tabel, selecteert u het gewenste kenmerk en definieert u de verwachte waarde.

U kunt ook rechtstreeks een tabelkoppeling selecteren in het dialoogvenster **Waarde** plukker en bevestig. In dat geval moeten de waarden die beschikbaar zijn voor de geselecteerde tabel, worden geselecteerd met een speciale kiezer, zoals in het onderstaande voorbeeld wordt getoond.

+++voorbeeld van Query

Hier, richt de vraag zich merken het waarvan etiket &quot;loopt&quot;.

1. Navigeren in het deelvenster **Merk** en selecteer de **Label** kenmerk.

   ![](assets/1-1-attribute.png){zoomable="yes"}{width="85%" align="center"}

1. Definieer de verwachte waarde voor het kenmerk.

   ![](assets/1-1-table.png){zoomable="yes"}{width="85%" align="center"}

Hier volgt een queryvoorbeeld waarin een tabelkoppeling rechtstreeks is geselecteerd. Beschikbare waarden voor deze tabel moeten worden geselecteerd in een speciale kiezer.

![](assets/1-1-table-direct.png){zoomable="yes"}{width="85%" align="center"}

+++

Voor een **1-N link** U kunt subvoorwaarden definiëren om uw query te verfijnen, zoals in het onderstaande voorbeeld wordt getoond.

+++voorbeeld van Query

Hier richt de query zich op ontvangers die aankopen hebben gedaan met betrekking tot het BrewMaster-product, voor een totale hoeveelheid van ten minste 100$.

1. Selecteer de **Aankopen** tabel en bevestiging.

   ![](assets/1-N-collection.png){zoomable="yes"}{width="50%" align="center"}

1. Een uitgaande overgang wordt toegevoegd, toestaand u om ondervoorwaarden tot stand te brengen.

   ![](assets/1-n-subcondition.png){zoomable="yes"}{width="85%" align="center"}

1. Selecteer de **Prijs** kenmerk- en doelaankopen van 1000$ of meer

   ![](assets/1-n-price.png){zoomable="yes"}{width="85%" align="center"}

1. Voeg subvoorwaarden toe die aan uw behoeften voldoen. Hier hebben we een voorwaarde toegevoegd aan de doelprofielen die een BrewMaster-product hebben aangeschaft.

   ![](assets/custom-condition-1-N.png){zoomable="yes"}{width="85%" align="center"}

+++

#### Werken met geaggregeerde gegevens {#aggregate}

Met aangepaste omstandigheden kunt u gezamenlijke bewerkingen uitvoeren. Hiervoor moet u rechtstreeks een kenmerk in een verzamelingstabel selecteren:

1. Navigeer binnen de gewenste inzamelingstabel en selecteer de attributen waarop u een gezamenlijke verrichting wilt uitvoeren.

   ![](assets/aggregate-attribute.png){zoomable="yes"}{width="85%" align="center"}

1. Schakel in het deelvenster Eigenschappen de optie **Samengevoegde gegevens** en selecteert u de gewenste statistische functie.

   ![](assets/aggregate.png){zoomable="yes"}{width="85%" align="center"}

### Een publiek selecteren {#audiences}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_selectaudience"
>title="Doelgroep selecteren"
>abstract="Met de opdracht **Doelgroep selecteren** kunt u het publiek kiezen dat u wilt gebruiken om de query te filteren."

Voer de volgende stappen uit om uw query te filteren op een bestaand publiek:

1. Klik op de knop **+** op het gewenste knooppunt en kies **[!UICONTROL Select audience]**.

1. De **Doelgroep selecteren** eigenschappenvenster wordt aan de rechterkant geopend. Kies het publiek dat u wilt gebruiken om uw query te filteren.

   *Voorbeeld met zoekopdrachten waarin alle profielen worden geretourneerd die tot het publiek van het &quot;Festival Goers&quot; behoren:*

   ![](assets/query-audience.png){zoomable="yes"}

### Een vooraf gedefinieerd filter gebruiken {#predefined-filters}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_predefinedfilter"
>title="Vooraf gedefinieerd filter"
>abstract="Met de opdracht **Vooraf gedefinieerd filter** kunt u een vooraf gedefinieerd filter selecteren in de lijst met aangepaste filters of in de lijst met favorieten."

Voer de volgende stappen uit om de query te filteren met een vooraf gedefinieerd filter:

1. Klik op de knop **+** op de gewenste knoop en selecteer **[!UICONTROL Predefined filter]**.

1. De **Vooraf gedefinieerd filter** eigenschappenvenster wordt aan de rechterkant geopend. Selecteer een vooraf gedefinieerd filter in de lijst met aangepaste filters of uit favorieten.

   *Voorbeeld van query met alle profielen die overeenkomen met het vooraf gedefinieerde filter &quot;Inactieve klanten&quot;:*

   ![](assets/query-predefined-filter.png){zoomable="yes"}

### Componenten kopiëren en plakken {#copy}

Met de querymodelfunctie kunt u een of meer filtercomponenten kopiëren en deze aan het einde van een overgang plakken. Deze bewerking kan worden uitgevoerd binnen het huidige querycanvas of op elk canvas in uw instantie.

>[!NOTE]
>
>De gekopieerde selectie blijft behouden zolang u in uw exemplaar werkt. Als u zich afmeldt en weer aanmeldt, is uw selectie niet meer beschikbaar voor plakken.

Voer de volgende stappen uit om filtercomponenten te kopiëren en te plakken:

1. Selecteer de filtercomponent die u wilt kopiëren door erop in het vraagcanvas te klikken. Als u meerdere componenten wilt selecteren, gebruikt u het gereedschap Meerdere selecties dat beschikbaar is in de werkbalk rechtsboven op het canvas.

1. Klik op de knop **[!UICONTROL Copy]** in het deelvenster Eigenschappen van de component of in het blauwe lint onder aan het scherm als u meerdere componenten hebt geselecteerd.

   | Eén component kopiëren | Meerdere componenten kopiëren |
   |  ---  |  ---  |
   | ![](assets/copy-single-component.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/copy-multiple-components.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

1. Als u de component(en) wilt plakken, klikt u op de +-knop aan het einde van de gewenste overgang en selecteert u **In items plakken**.

   ![](assets/copy-paste.png){zoomable="yes"}

## Filtercomponenten combineren met operatoren {#operators}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_group"
>title="Groep"
>abstract="In dit deelvenster kunt u de operator wijzigen die wordt gebruikt om filtervoorwaarden aan elkaar te koppelen."

Elke keer dat u een nieuwe filtercomponent aan uw query toevoegt, wordt deze automatisch aan de andere component gekoppeld door een component **EN** operator. Dit betekent dat de resultaten van de twee filtercomponenten worden gecombineerd.

In dit voorbeeld, hebben wij een nieuwe publiek-type het filtreren componenten op de tweede overgang toegevoegd. De component is gekoppeld aan de vooraf gedefinieerde filtervoorwaarde met een **EN** operator, wat betekent dat de queryresultaten ontvangers omvatten die het doelfilter &quot;Madridians&quot; (vooraf gedefinieerd) EN dat tot het publiek &quot;Discount hunters&quot; behoort.

![](assets/query-operator.png){zoomable="yes"}

Als u de operator wilt wijzigen die wordt gebruikt om filtervoorwaarden aan elkaar te koppelen, klikt u erop en selecteert u de gewenste operator in het dialoogvenster **Groep** venster dat aan de rechterkant wordt geopend.

Beschikbare operatoren zijn:

* **EN (Doorsnede)**: Combineert resultaten die overeenkomen met alle filtercomponenten in de uitgaande overgangen.
* **OF (Verenigen)**: Deze groep bevat resultaten die overeenkomen met ten minste een van de filtercomponenten in de uitgaande overgangen.
* **BEHALVE (Uitsluiting)**: Hiermee sluit u resultaten uit die overeenkomen met alle filtercomponenten in de uitgaande overgang.

![](assets/query-operator-change.png){zoomable="yes"}

Bovendien kunt u tussenliggende groepen componenten maken door op de knop **+** op een overgang. Dit staat u toe om een exploitant bij deze specifieke plaats toe te voegen om veelvoudige componenten samen te groeperen en uw vraag te verfijnen.

In het onderstaande voorbeeld hebben we een tussengroep opgericht die resultaten opneemt van het publiek &quot;VIP te belonen&quot; of &quot;Super VIP&quot;.

![](assets/query-intermediate-group.png){zoomable="yes"}

## Uw query controleren en valideren

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_ruleproperties"
>title="Eigenschappen van Rule"
>abstract="Nadat u de query op het canvas hebt gemaakt, kunt u deze controleren met de opdracht **Eigenschappen van Rule** aan de rechterkant.<br/>In dit deelvenster kunt u de resulterende gegevens weergeven, een SQL-codeversie van de query ophalen en het aantal doelrecords controleren.<br/>Gebruik de **Filter selecteren of opslaan** om de query op te slaan als een vooraf gedefinieerd filter of om de canvasinhoud te vervangen door een bestaand filter."

Nadat u de query op het canvas hebt gemaakt, kunt u deze controleren met de opdracht **Eigenschappen van Rule** aan de rechterkant. Beschikbare bewerkingen zijn:

* **Resultaten weergeven:** Hiermee geeft u de gegevens weer die het resultaat zijn van de query.
* **Codeweergave**: Geeft een op code gebaseerde versie van de query in SQL weer.
* **Berekenen**: Updates en geeft het aantal records weer dat wordt bedoeld door uw query.
* **Filter selecteren of opslaan**: Kies een bestaand vooraf gedefinieerd filter dat u op het canvas wilt gebruiken of sla uw query op als een vooraf gedefinieerd filter voor toekomstig hergebruik. <!--[Learn how to work with predefined filters](../get-started/predefined-filters.md)-->

  >[!IMPORTANT]
  >
  >Selecteer een vooraf gedefinieerd filter in het deelvenster Eigenschappen regel om de query die in het canvas is gemaakt te vervangen door het geselecteerde filter.

Wanneer uw vraag klaar is, klik **[!UICONTROL Confirm]** in de rechterbovenhoek om het op te slaan.

U kunt uw query op elk gewenst moment wijzigen door deze te openen. Houd er rekening mee dat als een bestaande query wordt geopend, deze in een vereenvoudigde weergave wordt weergegeven zonder dat de  **+** knoppen. Als u nieuwe elementen aan de query wilt toevoegen, selecteert u een component of operator op het canvas om de component of operator **+** knoppen.

![](assets/edit-audience.png){zoomable="yes"}
