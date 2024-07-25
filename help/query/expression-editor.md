---
audience: end-user
title: Bouw uw eerste vraag gebruikend de vraagmodeler
description: Leer hoe te om uw eerste vraag in vraagmodeler te bouwen.
badge: label="Beperkte beschikbaarheid" type="Informative"
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: 0efe4046cf30b4c447551c1cebbea0b4c2085a9f
workflow-type: tm+mt
source-wordcount: '2058'
ht-degree: 53%

---

# Expressies bewerken {#expression}

Als u een expressie bewerkt, moet u handmatig voorwaarden invoeren om een regel te vormen. In deze modus kunt u geavanceerde functies gebruiken waarmee u de waarden kunt bewerken die worden gebruikt voor het uitvoeren van specifieke query&#39;s, zoals datums, tekenreeksen, numerieke velden, sorteren, enzovoort.

## Werken met de expressie-editor {#edit}

De expressie-editor is beschikbaar via de knop querymodel **[!UICONTROL Edit expression]** , beschikbaar voor de velden **[!UICONTROL Attribute]** en **[!UICONTROL Value]** wanneer u een aangepaste voorwaarde configureert.

| Toegang vanuit het veld **[!UICONTROL Attribute]** | Toegang vanuit het veld **[!UICONTROL Value]** |
|  ---  |  ---  |
| ![](assets/expression-editor-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![](assets/edit-expression.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

De uitdrukkingsredacteur verstrekt:

* Een **inputgebied (1)** waarin de uitdrukking wordt bepaald.
* De lijst van beschikbare **gebieden (2)** die in de uitdrukking en het beantwoorden aan het schema kunnen worden gebruikt, dat ook als het richten dimensie, van de vraag wordt bekend.
* **de functies van de Helper (3)**, die door categorie wordt gesorteerd.

Bewerk de expressie door een expressie rechtstreeks in het invoerveld in te voeren. Als u een veld of hulpfunctie wilt toevoegen, plaatst u de cursor in de expressie waar u deze wilt toevoegen en klikt u op +.

![](assets/expression-editor.png){zoomable="yes"}

Klik op de knop **[!UICONTROL Confirm]** als uw expressie gereed is. De expressie wordt weergegeven in het geselecteerde veld. Als u deze wilt bewerken, opent u de editor voor de expressie en brengt u de gewenste wijzigingen aan.

In het onderstaande voorbeeld ziet u een expressie die is geconfigureerd voor het veld **[!UICONTROL Value]** . Als u de expressie wilt bewerken, moet u de expressie-editor openen met de knop **[!UICONTROL Edit expression]** .

![](assets/edit-expression-value.png){zoomable="yes"}

## Helpfuncties

Met het gereedschap voor het bewerken van query&#39;s kunt u geavanceerde functies gebruiken om complexe filtering uit te voeren op basis van de gewenste resultaten en de typen gemanipuleerde gegevens. De volgende functies zijn beschikbaar:

### Geaggregeerd

De aggregatiefuncties worden gebruikt voor het uitvoeren van berekeningen op een reeks waarden.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong> Avg </strong><br /> </td> 
   <td> Keert het gemiddelde van een kolom van het aantaltype terug <br /> </td> 
   <td> Avg(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> Telling </strong><br /> </td> 
   <td> Telt de niet-nulwaarden van een kolom <br /> </td> 
   <td> Count(&lt;value&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong> CountAll </strong><br /> </td> 
   <td> Telt de teruggekeerde waarden (alle gebieden) <br /> </td> 
   <td> CountAll()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong> Countdifferent </strong><br /> </td> 
   <td> Telt de duidelijke niet-krachteloze waarden van een kolom <br /> </td> 
   <td> Countdifferent(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> Max </strong><br /> </td> 
   <td> Keert de maximumwaarde van een aantal, een koord, of een kolom van het datumtype terug <br /> </td> 
   <td> Max(&lt;value&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong> Min </strong><br /> </td> 
   <td> Keert de minimumwaarde van een aantal, een koord of een kolom van het datumtype terug <br /> </td> 
   <td> Min(&lt;value&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> StdDev </strong><br /> </td> 
   <td> Retourneert de standaardafwijking van een getal, tekenreeks of datumkolom <br /> </td> 
   <td> StdDev(&lt;value&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong> StringAgg </strong><br /> </td> 
   <td> Keert de aaneenschakeling van de waarden van een koordtype kolom terug, die door het karakter in het tweede argument wordt gescheiden <br /> </td> 
   <td> StringAgg(&lt;Value&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> Som </strong><br /> </td> 
   <td> Keert de som waarden van een aantal, een koord, of een kolom van het datumtype terug <br /> </td> 
   <td> Sum(&lt;value&gt;)<br /></td> 
  </tr> 
 </tbody> 
</table>

### Datum

De datumfuncties worden gebruikt om datum- of tijdwaarden te manipuleren.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AddDays</strong><br /> </td> 
   <td> Hiermee voegt u een aantal dagen toe aan een datum<br /> </td> 
   <td> AddDays(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddHours</strong><br /> </td> 
   <td> Hiermee voegt u een aantal uren toe aan een datum<br /> </td> 
   <td> AddHours(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMinutes</strong><br /> </td> 
   <td> Hiermee voegt u een aantal minuten toe aan een datum<br /> </td> 
   <td> AddMinutes(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddMonths</strong><br /> </td> 
   <td> Hiermee voegt u een aantal maanden toe aan een datum<br /> </td> 
   <td> AddMonths(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddSeconds</strong><br /> </td> 
   <td> Hiermee voegt u een aantal seconden toe aan een datum<br /> </td> 
   <td> AddSeconds(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>AddYears</strong><br /> </td> 
   <td> Hiermee voegt u een aantal jaren toe aan een datum<br /> </td> 
   <td> AddYear(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong> ConvertNTZ </strong><br /> </td> 
   <td> Converteert timestamp NTZ (timestamp zonder timezone) in TZ (timestamp met timezone) het toepassen van bepaalde zitting TZ <br/> </td> 
   <td> ConvertNTZ (&lt;date+time&gt;) <br /> </td>  
  </tr>
  <tr> 
   <!--<td> <strong>ConvertTimezone</strong><br /> </td> 
   <td> <br/> </td> 
   <td> ConvertNTZ (&lt;date+time&gt;)<br /> </td>  
  </tr>-->
  <tr> 
   <td> <strong> DateCmp </strong><br /> </td> 
   <td> Twee datums vergelijken <br/> </td> 
   <td> DateCmp (&lt;date&gt;,&lt;date&gt;) <br /> </td>  
  </tr>
  <tr> 
   <td> <strong>DateOnly</strong><br /> </td> 
   <td> Keert de datum slechts (met tijd bij 00:00)* terug <br /> </td> 
   <td> DateOnly(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Day</strong><br /> </td> 
   <td> Retourneert het getal dat de dag van de datum vertegenwoordigt<br /> </td> 
   <td> Day(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DayOfYear</strong><br /> </td> 
   <td> Keert het aantal van de dag in het jaar van de datum terug <br /> </td> 
   <td> DayOfYear(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgo</strong><br /> </td> 
   <td> Retourneert de datum die overeenkomt met de huidige datum min n dagen <br /> </td> 
   <td> DaysAgo(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysAgoInt</strong><br /> </td> 
   <td> Retourneert de datum (geheel getal jjjjmmdd) die overeenkomt met de huidige datum minus n dagen <br /> </td> 
   <td> DaysAgoInt(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysDiff</strong><br /> </td> 
   <td> Aantal dagen tussen twee datums<br /> </td> 
   <td> DaysDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>DaysOld</strong><br /> </td> 
   <td> Retourneert de leeftijd in dagen van een datum<br /> </td> 
   <td> DaysOld(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetDate</strong><br /> </td> 
   <td> Hiermee wordt de huidige systeemdatum van de server geretourneerd<br /> </td> 
   <td> GetDate()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Hour</strong><br /> </td> 
   <td> Retourneert het uur van de datum<br /> </td> 
   <td> Hour(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>HoursDiff</strong><br /> </td> 
   <td> Retourneert het aantal uren tussen twee datums<br /> </td> 
   <td> HoursDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Minute</strong><br /> </td> 
   <td> Retourneert de minuten van de datum<br /> </td> 
   <td> Minute(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MinutesDiff</strong><br /> </td> 
   <td> Retourneert het aantal minuten tussen twee datums<br /> </td> 
   <td> MinutesDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Month</strong><br /> </td> 
   <td> Retourneert het getal dat de maand van de datum vertegenwoordigt<br /> </td> 
   <td> Month(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsAgo</strong><br /> </td> 
   <td> Retourneert de datum die overeenkomt met de huidige datum minus n maanden<br /> </td> 
   <td> MonthsAgo(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsDiff</strong><br /> </td> 
   <td> Retourneert het aantal maanden tussen twee datums<br /> </td> 
   <td> MonthsDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>MonthsOld</strong><br /> </td> 
   <td> Retourneert de leeftijd in maanden van een datum<br /> </td> 
   <td> MonthsOld(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Oldest</strong><br /> </td> 
   <td> Keert de oudste datum in een waaier terug <br /> </td> 
   <td> Oudst (&lt;date, date&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Second</strong><br /> </td> 
   <td> Retourneert de seconden van de datum<br /> </td> 
   <td> Second(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SecondsDiff</strong><br /> </td> 
   <td> Retourneert het aantal seconden tussen twee datums<br /> </td> 
   <td> SecondsDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubDays</strong><br /> </td> 
   <td> Hiermee trekt u een aantal dagen van een datum af<br /> </td> 
   <td> SubDays(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubHours</strong><br /> </td> 
   <td> Hiermee trekt u een aantal uren van een datum af<br /> </td> 
   <td> SubHours(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMinutes</strong><br /> </td> 
   <td> Hiermee trekt u een aantal aantal minuten van een datum af<br /> </td> 
   <td> SubMinutes(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubMonths</strong><br /> </td> 
   <td> Hiermee trekt u een aantal maanden van een datum af<br /> </td> 
   <td> SubMonths(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubSeconds</strong><br /> </td> 
   <td> Hiermee trekt u een aantal seconden van een datum af<br /> </td> 
   <td> SubSeconds(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>SubYears</strong><br /> </td> 
   <td> Hiermee trekt u een aantal jaren van een datum af<br /> </td> 
   <td> SubYears(&lt;datum&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDate</strong><br /> </td> 
   <td> Converteert een datum + tijd als datum<br /> </td> 
   <td> ToDate(&lt;datum + tijd&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDateTime</strong><br /> </td> 
   <td> Zet een tekenreeks om in een datum + tijd<br /> </td> 
   <td> ToDateTime(&lt;tekenreeks&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong> ToTimestamp </strong><br /> </td> 
   <td> Converteert een koord in timestamp <br /> </td> 
   <td> ToTimestamp (&lt;string&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong> ToTimeZone </strong><br /> </td> 
   <td> Converteer een datum + tijd naar tijdzone <br /> </td> 
   <td> ToTimeZone (&lt;date&gt;,&lt;time zone&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncDate</strong><br /> </td> 
   <td> Rondt een datum+tijd af naar de dichtstbijzijnde seconde<br /> </td> 
   <td> TruncDate(@lastModified, &lt;aantal seconden&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncDateTZ</strong><br /> </td> 
   <td> Rondt een datum + tijd af naar een bepaalde precisie die in seconden wordt uitgedrukt<br /> </td> 
   <td> TruncDateTZ(&lt;datum&gt;, &lt;aantal seconden&gt;, &lt;tijdzone&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>TruncQuarter</strong><br /> </td> 
   <td> Rondt een datum af naar het kwartaal<br /> </td> 
   <td> TruncQuarter(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncTime</strong><br /> </td> 
   <td> Rondt het tijdsdeel af naar de dichtstbijzijnde seconde<br /> </td> 
   <td> TruncTim (e&lt;date&gt;, &lt;number of seconds&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncWeek</strong><br /> </td> 
   <td> Rondt een datum af naar de week<br /> </td> 
   <td> TruncWeek(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>TruncYear</strong><br /> </td> 
   <td> Rondt een datum + tijd naar 1 januari van het jaar<br /> </td> 
   <td> TruncYear(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>WeekDay</strong><br /> </td> 
   <td> Keert een aantal terug dat de dag in de week van de datum vertegenwoordigt (0=Maandag, 6=Zondag) <br /> </td> 
   <td> WeekDay(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Year</strong><br /> </td> 
   <td> Retourneert het getal dat het jaar van de datum vertegenwoordigt<br /> </td> 
   <td> Year(&lt;datum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearAnd Month</strong><br /> </td> 
   <td> Retourneert het getal dat het jaar en de maand van de datum vertegenwoordigt.<br /> </td> 
   <td> YearAndMonth(&lt;datum&gt;)<br /> </td>  
  </tr>
  <tr> 
   <td> <strong> YearAgo </strong><br /> </td> 
   <td> Keert het aantal jaren tussen een bepaalde datum en de huidige datum terug <br /> </td> 
   <td> YearAgo (&lt;date&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearDiff</strong><br /> </td> 
   <td> Retourneert het aantal jaren tussen de twee datums<br /> </td> 
   <td> YearsDiff(&lt;einddatum&gt;, &lt;begindatum&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>YearsOld</strong><br /> </td> 
   <td> Retourneert de leeftijd in jaren van een datum<br /> </td> 
   <td> YearOld(&lt;datum&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Merk op dat de **functie Dateonly** rekening houdt met timezone van de server, niet de exploitant.

### Geomarketing

De geomarketing-functies worden gebruikt om geografische waarden te manipuleren.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> Retourneert de afstand tussen twee punten die worden gedefinieerd door hun lengte en breedte, uitgedrukt in graden.<br /> </td> 
   <td> Distance(&lt;Lengtegraad A&gt;, &lt;Breedtegraad A&gt;, &lt;Lengtegraad B&gt;, &lt;Breedtegraad B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Numeriek

De numerieke functies worden gebruikt om tekst om te zetten in getallen.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Retourneert de absolute waarde van een getal<br /> </td> 
   <td> Abs(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Retourneert het laagste gehele getal dat groter is dan of gelijk is aan een getal<br /> </td> 
   <td> Ceil(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Retourneert het grootste gehele getal dat groter is dan of gelijk is aan een getal <br /> </td> 
   <td> Floor(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Retourneert het hoogste van twee getallen<br /> </td> 
   <td> Greatest(&lt;nummer 1&gt;, &lt;nummer 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Retourneert het laagste van twee getallen<br /> </td> 
   <td> Least(&lt;nummer 1&gt;, &lt;nummer 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Keert de rest van de geheelverdeling van n1 door n2 terug <br /> </td> 
   <td> Mod(&lt;nummer 1&gt;, &lt;nummer 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> Retourneert de verhouding van twee getallen uitgedrukt als een percentage<br /> </td> 
   <td> Percent(&lt;nummer 1&gt;, &lt;nummer 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Hiermee wordt de willekeurige waarde geretourneerd<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Rondt een getal af naar n decimalen<br /> </td> 
   <td> Round(&lt;nummer&gt;, &lt;aantal decimalen&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Hiermee wordt het teken van het getal geretourneerd<br /> </td> 
   <td> Sign(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Hiermee wordt een geheel getal omgezet in een zwevende waarde<br /> </td> 
   <td> ToDouble(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Zet een zwevende waarde om in een 64-bits geheel getal<br /> </td> 
   <td> ToInt64(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Hiermee wordt een zwevende waarde omgezet in een geheel getal<br /> </td> 
   <td> ToInteger(&lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Kapt aantal decimalen af van n1 tot n2<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Overige

Deze tabel bevat de resterende beschikbare functies.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong> AESEncrypt </strong><br /> </td> 
   <td> Codeer koord dat in argument wordt verstrekt <br /> </td> 
   <td> AESEncrypt (&lt;value&gt;) <br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Retourneert waarde 1 als de voorwaarde true is. Als niet, keert het waarde 2 terug.<br /> </td> 
   <td> Case(When(&lt;voorwaarde&gt;, &lt;waarde 1&gt;), Else(&lt;waarde 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Hiermee verwijdert u de markering in de waarde<br /> </td> 
   <td> ClearBit(&lt;identificatiecode&gt;, &lt;markering&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Retourneert waarde 2 als waarde 1 null of nihil is, anders wordt waarde 1 geretourneerd<br /> </td> 
   <td> Coalesce(&lt;waarde 1&gt;, &lt;waarde 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Retourneert waarde 3 als waarde 1 = waarde 2. Indien niet waarde 4 terugkeert.<br /> </td> 
   <td> Decode(&lt;waarde 1&gt;, &lt;waarde 2&gt;, &lt;waarde 3&gt;, &lt;waarde 4&gt;)<br /> </td>  
  </tr> 
  <!--<tr> 
   <td> <strong>DefaultFolder</strong><br /> </td> 
   <td> Returns value 3 if value 1 = value 2. If not returns value 4.<br /> </td> 
   <td> Decode(&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;, &lt;value 4&gt;)<br /> </td>  
  </tr> -->
  <tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Retourneert waarde 1 (mag alleen worden gebruikt als parameter van de case-functie)<br /> </td> 
   <td> Else (&lt;value 1&gt;, &lt;value 2&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Extraheert het domein uit een e-mailadres<br /> </td> 
   <td> GetEmailDomain(&lt;waarde&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Hiermee wordt de URL van de server van de spiegelpagina opgehaald<br /> </td> 
   <td> GetMirrorURL(&lt;waarde&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Retourneert waarde 1 als de expressie true is. Als niet, keert waarde 2 <br /> terug </td> 
   <td> Iif(&lt;voorwaarde&gt;, &lt;waarde 1&gt;, &lt;waarde 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Geeft aan of de markering zich in de waarde bevindt<br /> </td> 
   <td> IsBitSet(&lt;identificatiecode&gt;, &lt;markering&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Retourneert waarde 2 als tekenreeks 1 leeg is, anders retourneert u waarde 3 <br /> </td> 
   <td> IsEmptyString (&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong> NewUID </strong><br /> </td> 
   <td> Retourneert een unieke id <br /> </td> 
   <td> NewUID() <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Retourneert de lege tekenreeks als het argument NULL is<br /> </td> 
   <td> NoNull(&lt;waarde&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Retourneert het regelnummer<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Hiermee wordt de markering in de waarde geforceerd<br /> </td> 
   <td> SetBit(&lt;identificatiecode&gt;, &lt;markering&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Hiermee wordt een getal omgezet in een Booleaanse waarde<br /> </td> 
   <td> ToBoolean(&lt;nummer&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Retourneert waarde 1 als de expressie true is. Als niet, keert het waarde 2 terug (kan slechts als parameter van de case functie worden gebruikt) <br /> </td> 
   <td> When(&lt;voorwaarde&gt;, &lt;waarde 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### String

De tekenreeksfuncties worden gebruikt om een set tekenreeksen te manipuleren.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Geeft aan of alle parameters niet null en niet leeg zijn<br /> </td> 
   <td> AllNonNull2(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Geeft aan of alle parameters niet null en niet leeg zijn<br /> </td> 
   <td> AllNonNull3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> Ascii </strong><br /> </td> 
   <td> Keert de waarde van ASCII van het eerste karakter in het koord terug.<br /> </td> 
   <td> Ascii(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Hiermee wordt het teken geretourneerd dat overeenkomt met de ASCII-code ‘n’<br /> </td> 
   <td> Char(&lt;number&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Keert de positie van koord 2 in koord 1 terug.<br /> </td> 
   <td> Charindex(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> dataLength </strong><br /> </td> 
   <td> Keert de grootte in bytes van het koord terug <br /> </td> 
   <td> dataLength(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Retourneert de n-de (van 1 tot en met n) regel van de tekenreeks<br /> </td> 
   <td> GetLine(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Retourneert de derde parameter als de eerste twee parameters gelijk zijn. Indien niet, keert de laatste parameter <br /> terug </td> 
   <td> IfEquals(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Geeft aan of het als parameter doorgegeven memo null is<br /> </td> 
   <td> IsMemoNull(&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Voegt de doorgegeven tekenreeksen samen als parameters. Voegt ruimten tussen de koorden toe indien nodig.<br /> </td> 
   <td> JuxtWords(&lt;string&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Voegt de doorgegeven tekenreeksen samen als parameters. Voegt indien nodig spaties tussen de tekenreeksen toe <br /> </td> 
   <td> JuxtWords3(&lt;string&gt;, &lt;string&gt;, &lt;string&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Retourneert de eerste n tekens van de tekenreeks<br /> </td> 
   <td> Left(&lt;string&gt;, &lt;number&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Keert de lengte van het koord <br /> terug </td> 
   <td> Lengte (&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> Lijn </strong><br /> </td> 
   <td> Regel n uit tekenreeks extraheren <br /> </td> 
   <td> Regel (&lt;string&gt;,&lt;number&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Hiermee wordt de tekenreeks in kleine letters geretourneerd<br /> </td> 
   <td> Lower(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Hiermee wordt de voltooide tekenreeks links geretourneerd<br /> </td> 
   <td> LPad (&lt;String&gt;, &lt;Number&gt;, &lt;Char&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Hiermee worden spaties links van de tekenreeks verwijderd<br /> </td> 
   <td> Ltrim(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Retourneert een hexadecimale representatie van de MD5-toets van een tekenreeks<br /> </td> 
   <td> Md5Digest(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> Hiermee wordt opgegeven of het memo de tekenreeks bevat die als parameter is doorgegeven<br /> </td> 
   <td> MemoContains(&lt;memo&gt;, &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong> NodeValue </strong><br /> </td> 
   <td> Extraheert de waarde van een gebied van XML van zijn XPath en de gebiedsgegevens <br /> </td> 
   <td> NodeValue (&lt;String&gt;, &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Vervangt alle voorkomen van een gespecificeerde koordwaarde met een andere koordwaarde.<br /> </td> 
   <td> Replace(&lt;String&gt;,&lt;String&gt;,&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Retourneert de laatste n tekens van de tekenreeks<br /> </td> 
   <td> Right(&lt;tekenreeks&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Hiermee wordt de voltooide tekenreeks aan de rechterkant geretourneerd<br /> </td> 
   <td> RPad(&lt;string&gt;, &lt;number&gt;, &lt;character&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Hiermee worden spaties rechts van de tekenreeks verwijderd<br /> </td> 
   <td> Rtrim(&lt;tekenreeks&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Hexadecimale vertegenwoordiging van de sleutel SHA256 van een koord.<br /> </td> 
   <td> Sha256Digest (&lt;String&gt;) <br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Hexadecimale vertegenwoordiging van de sleutel SHA512 van een koord.<br /> </td> 
   <td> Sha512Digest (&lt;String&gt;) <br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Retourneert de tekenreeks met de eerste letter van elk woord in hoofdletters<br /> </td> 
   <td> Smart(&lt;tekenreeks&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Extraheert substring die bij karakter n1 van het koord en van lengte n2 begint <br /> </td> 
   <td> Substring(&lt;tekenreeks&gt;, &lt;offset&gt;, &lt;lengte&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Zet het getal om in een tekenreeks<br /> </td> 
   <td> ToString (&lt;number&gt;, &lt;number&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Hiermee wordt de tekenreeks in hoofdletters geretourneerd<br /> </td> 
   <td> Upper(&lt;tekenreeks&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Retourneert de externe sleutel van een koppeling die als een parameter is doorgegeven als de andere twee parameters gelijk zijn<br /> </td> 
   <td> VirtualLink(&lt;nummer&gt;, &lt;nummer&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Retourneert de externe sleutel (tekst) van een koppeling die als parameter wordt doorgegeven als de andere twee parameters gelijk zijn<br /> </td> 
   <td> VirtualLinkStr(&lt;tekenreeks&gt;, &lt;nummer&gt;, &lt;nummer&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Venster

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Naam</strong><br /> </td> 
   <td> <strong>Beschrijving</strong><br /> </td> 
   <td> <strong>Syntaxis</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Over__</strong><br /> </td> 
   <td> Voer de SQL functievraag uit die als 1st parameter, over Verdeling of Orde door de gebieden is ingegaan als 2de parameter <br /> is ingegaan </td> 
   <td> _Over_ (&lt;Value&gt;, &lt;Value&gt;) <br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Hiermee wordt een aflopende sortering toegepast<br /> </td> 
   <td> Desc(&lt;waarde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Hiermee wordt het resultaat binnen de partitie gesorteerd<br /> </td> 
   <td> OrderBy(&lt;waarde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Verdeelt het resultaat van een query op een lijst<br /> </td> 
   <td> PartitionBy(&lt;waarde 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Produceert een lijnaantal dat op de lijstverdeling en op een sorterende opeenvolging wordt gebaseerd.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;waarde 1&gt;), OrderBy(&lt;waarde 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
