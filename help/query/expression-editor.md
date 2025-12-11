---
audience: end-user
title: Bouw uw eerste vraag gebruikend de vraagmodeler
description: Leer hoe te om uw eerste vraag in vraagmodeler te bouwen.
exl-id: abff07ef-2bc0-4e00-8957-4d59fc3bc938
source-git-commit: fdf93fb3554d05057052aa7059e141817a883dcc
workflow-type: tm+mt
source-wordcount: '4097'
ht-degree: 5%

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

<!-- ### Aggregate

The aggregate functions are used to perform calculations on a set of values.

>[!BEGINTABS]

>[!TAB Google BigQuery]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StdDev** | Returns the standard deviation of the values given. | StdDev(&lt;VALUE&gt;) | StdDev([0,3,5]) | -->

<!-- 

>[!TAB Databricks]

Aggregate functions are not available.

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") |

>[!TAB Redshift]

Aggregate functions are not available. -->

<!-- 

>[!TAB Snowflake]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **StringAgg** | Returns the concatenation of the values of a string type column, separated by the character in the second argument | StringAgg(&lt;Value&gt;, &lt;String&gt;) | StringAgg(column, ",") | -->

<!-- 
>[!TAB Vertica]

Aggregate functions are not available. -->

<!-- 
>[!ENDTABS] 
-->

### Datum

De datumfuncties worden gebruikt om datum- of tijdwaarden te manipuleren.

>[!BEGINTABS]

>[!TAB  Google BigQuery ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Hiermee voegt u het opgegeven aantal jaren toe aan de opgegeven datumtijd. | AddYear(&lt;DATETIME>, &lt;NUMBER>) | AddYear (&quot;2019-12-25 15 :30: 00&quot;, 3) |
| **AddMonths** | Hiermee voegt u het opgegeven aantal maanden toe aan de opgegeven datumtijd. | AddMonths(&lt;DATETIME>, &lt;NUMBER>) | AddMonths (&quot;2019-12-25 15 :30: 00&quot;, 6) |
| **AddDays** | Hiermee voegt u het opgegeven aantal dagen toe aan de opgegeven datumtijd. | AddDays(&lt;DATETIME>, &lt;NUMBER>) | AddDays (&quot;2019-12-25 15 :30: 00&quot;, 10) |
| **AddHours** | Hiermee voegt u het opgegeven aantal uren toe aan de opgegeven datumtijd. | AddHours(&lt;DATETIME>, &lt;NUMBER>) | AddHours (&quot;2019-12-25 15 :30: 00&quot;, 3) |
| **AddMinutes** | Hiermee voegt u het opgegeven aantal minuten toe aan de opgegeven datumtijd. | AddMinutes(&lt;DATETIME>, &lt;NUMBER>) | AddMinutes (&quot;2019-12-25 15 :30: 00&quot;, 32) |
| **AddSeconds** | Hiermee wordt het opgegeven aantal seconden toegevoegd aan de opgegeven datetime. | AddSeconds(&lt;DATETIME>, &lt;NUMBER>) | AddSeconds (&quot;2019-12-25 15 :30: 00&quot;, 37) |
| **SubYears** | Trekt het gespecificeerde aantal jaren aan de verstrekte datetime af. | SubYear(&lt;DATETIME>, &lt;NUMBER>) | SubYaren (&quot;2019-12-25 15 :30: 00&quot;, 3) |
| **SubMonths** | Trekt het gespecificeerde aantal maanden aan de verstrekte datetime af. | SubMonths(&lt;DATETIME>, &lt;NUMBER>) | SubMonths (&quot;2019-12-25 15 :30: 00&quot;, 6) |
| **SubDays** | Trekt het gespecificeerde aantal dagen aan de verstrekte datetime af. | SubDays(&lt;DATETIME>, &lt;NUMBER>) | SubDays (&quot;2019-12-25 15 :30: 00&quot;, 10) |
| **SubHours** | Trekt het gespecificeerde aantal uren aan de verstrekte datetime af. | SubHours(&lt;DATETIME>, &lt;NUMBER>) | SubHours (&quot;2019-12-25 15 :30: 00&quot;, 3) |
| **SubMinutes** | Trekt het gespecificeerde aantal minuten aan de verstrekte datetime af. | SubMinutes(&lt;DATETIME>, &lt;NUMBER>) | SubMinutes (&quot;2019-12-25 15 :30: 00&quot;, 32) |
| **SubSeconds** | Trekt het gespecificeerde aantal seconden aan de verstrekte datetime af. | SubSeconds(&lt;DATETIME>, &lt;NUMBER>) | SubSeconds (&quot;2019-12-25 15 :30: 00&quot;, 37) |
| **Year** | Extraheert het jaar vanaf het opgegeven datetime-object. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **Month** | Extraheert de maand vanaf het opgegeven datetime-object. | Maand (&lt;DATETIME>) | Maand (&quot;2019-12-15 15 :30: 00&quot;) |
| **Day** | Extraheert de dag vanaf het opgegeven datetime-object. | Dag (&lt;DATETIME>) | Dag (&quot;2019-12-15 15 :30: 00&quot;) |
| **DayOfYear** | Extraheert de dag van het jaar vanaf het opgegeven datetime-object. Bijvoorbeeld, als de verstrekte datetime 2 Februari is, zou het 33 terugkeren. | DayOfYear(&lt;DATETIME>) | DayOfYear (&quot;2019-12-15 15 :30: 00&quot;) |
| **WeekDay** | Extraheert de dag van de week van het opgegeven datetime-object, als een getal van 0 tot en met 6, waarbij 0 staat voor zondag. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **Hour** | Extraheert de uurwaarde van het opgegeven datetime-object. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **Minute** | Extraheert de minutenwaarde uit het opgegeven datetime-object. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **Second** | Extraheert de tweede waarde van het opgegeven datetime-object. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **YearDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van jaren. | YearDiff(&lt;DATETIME>, &lt;DATETIME>) | YarenDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **MonthsDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van maanden. | MonthsDiff(&lt;DATETIME>, &lt;DATETIME>) | MonthsDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **DaysDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van dagen. | DaysDiff(&lt;DATETIME>, &lt;DATETIME>) | DaysDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **HoursDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van uren. | HoursDiff(&lt;DATETIME>, &lt;DATETIME>) | HoursDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **MinutesDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van notulen. | MinutesDiff(&lt;DATETIME>, &lt;DATETIME>) | MinutesDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **SecondsDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van seconden. | SecondsDiff(&lt;DATETIME>, &lt;DATETIME>) | SecondsDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **YearsOld** | Vindt het verschil tussen de bepaalde datum en heden, met een granulariteit van jaren. | YearOld(&lt;DATETIME>) | YarenOld (&quot;2019-12-25 15 :30: 00&quot;) |
| **MonthsOld** | Vindt het verschil tussen de bepaalde datum en heden, met een granulariteit van maanden. | MonthsOld(&lt;DATETIME>) | MonthsOld (&quot;2019-12-25 15 :30: 00&quot;) |
| **DaysOld** | Vindt het verschil tussen bepaalde datetime en heden, met een granulariteit van dagen. | DaysOld(&lt;DATETIME>) | DaysOld (&quot;2019-12-25 15 :30: 00&quot;) |
| **GetDate** | Haal de huidige datum van de server op. | GetDate() | GetDate() |
| **DateOnly** | Kort de datetime aan enkel het jaar, de maand, en de dag in. | DateOnly(&lt;DATETIME>) | DateOnly (&quot;2019-12-25 15 :30: 00&quot;) |
| **ToDate** | Hiermee converteert u het veld naar een datumveld. | ToDate(&lt;DATETIME>) | ToDate (&quot;2019-12-25 15 :30: 00&quot;) |
| **ToDateTime** | Hiermee converteert u het veld naar een datetime-veld. | ToDateTime(&lt;DATE>) | ToDateTime (&quot;2019-12-25 15 :30: 00&quot;) |
| **ToTimestamp** | Hiermee converteert u het veld naar een tijdstempelveld. | ToTimestamp(&lt;DATETIME>) | ToTimestamp (&quot;2019-12-25 15 :30: 00&quot;) |
| **Oldest** | Retourneert de oudste datum tussen de twee opgegeven waarden. | Oudst(&lt;DATETIME>, &lt;DATETIME>) | Oudst (&quot;2015-02-13 11 :59: 59&quot;, &quot;2016-04-13 19 :28: 14&quot;) |
| **TruncDate** | Kort de datetime aan de dichtstbijzijnde eenheid in, op basis van de gegeven numerieke waarde. Als de numerieke waarde gelijk is aan 60, wordt deze afgebroken tot de dichtstbijzijnde minuut. Als de numerieke waarde gelijk is aan 3600, wordt deze afgebroken tot het dichtstbijzijnde uur. Als de numerieke waarde gelijk is aan 86400, wordt deze afgebroken tot de dichtstbijzijnde dag. Anders wordt het naar de dichtstbijzijnde seconde afgebroken. | TruncDate(&lt;DATETIME>, &lt;NUMBER>) | TruncDate (&quot;2016-04-13 19 :28: 14&quot;, 3600) |
| **TruncDateTZ** | Kort de datetime aan de dichtstbijzijnde eenheid in, op basis van de gegeven numerieke waarde, en stelt de datetime in op de opgegeven tijdzone. Als de numerieke waarde gelijk is aan 60, wordt deze afgebroken tot de dichtstbijzijnde minuut. Als de numerieke waarde gelijk is aan 3600, wordt deze afgebroken tot het dichtstbijzijnde uur. Als de numerieke waarde gelijk is aan 86400, wordt deze afgebroken tot de dichtstbijzijnde dag. | TruncDateTZ(&lt;DATETIME>, &lt;NUMBER>, &lt;TIMEZONE>) | TruncDateTZ (&quot;2016-04-13 19 :28: 14&quot;, 3600, &quot;America/Los_Angeles&quot;) |
| **TruncTime** | Stelt de datetime in op 1 januari 2000 en rondt de rest van de datetime af op de dichtstbijzijnde eenheid, op basis van de opgegeven numerieke waarde. Als de numerieke waarde gelijk is aan 60, wordt deze verkort tot de dichtstbijzijnde minuut. Als de numerieke waarde gelijk is aan 3600, wordt deze afgebroken tot het dichtstbijzijnde uur. | TruncTime(&lt;DATETIME>, &lt;NUMBER>) | TruncTime (&quot;2016-04-13 19 :28: 14&quot;, 3600) |
| **TruncQuarter** | Kort de datetime aan de eerste datum in het dichtstbijzijnde kwartaal in. | TruncQuarter(&lt;DATETIME>) | TruncQuarter (&quot;2016-04-13 19 :28: 14&quot;) |
| **TruncYear** | Kort de datetime aan de eerste datum in het dichtstbijzijnde jaar in. | TruncYear(&lt;DATETIME>) | TruncYear (&quot;2016-04-13 19 :28: 14&quot;) |
| **TruncWeek** | Kort de datetime aan de Zondag van de dichtstbijzijnde week in. | TruncWeek(&lt;DATETIME>) | TruncWeek (&quot;2016-04-13 19 :28: 14&quot;) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- | **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | -->


<!-- 
>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncDateTZ** | Truncates the datetime to the nearest unit, based on the numerical value given, and sets the datetime to the specified timezone. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. | TruncDateTZ(&lt;DATETIME&gt;, &lt;NUMBER&gt;, &lt;TIMEZONE&gt;) | TruncDateTZ("2016-04-13 19:28:14", 3600, "America/Los_Angeles") |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |

>[!TAB Redshift]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **ConvertTimezone** | Converts the datetime from its timezone to the timezone of the external account. | ConvertTimezone(&lt;DATETIME&gt;) | ConvertTimezone("2019-12-25 15:30:00") |

 -->

>[!TAB  Snowflake ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Hiermee voegt u het opgegeven aantal jaren toe aan de opgegeven datumtijd. | AddYear(&lt;DATETIME>, &lt;NUMBER>) | AddYear (&quot;2019-12-25 15 :30: 00&quot;, 3) |
| **AddMonths** | Hiermee voegt u het opgegeven aantal maanden toe aan de opgegeven datumtijd. | AddMonths(&lt;DATETIME>, &lt;NUMBER>) | AddMonths (&quot;2019-12-25 15 :30: 00&quot;, 6) |
| **AddDays** | Hiermee voegt u het opgegeven aantal dagen toe aan de opgegeven datumtijd. | AddDays(&lt;DATETIME>, &lt;NUMBER>) | AddDays (&quot;2019-12-25 15 :30: 00&quot;, 10) |
| **AddHours** | Hiermee voegt u het opgegeven aantal uren toe aan de opgegeven datumtijd. | AddHours(&lt;DATETIME>, &lt;NUMBER>) | AddHours (&quot;2019-12-25 15 :30: 00&quot;, 3) |
| **AddMinutes** | Hiermee voegt u het opgegeven aantal minuten toe aan de opgegeven datumtijd. | AddMinutes(&lt;DATETIME>, &lt;NUMBER>) | AddMinutes (&quot;2019-12-25 15 :30: 00&quot;, 32) |
| **AddSeconds** | Hiermee wordt het opgegeven aantal seconden toegevoegd aan de opgegeven datetime. | AddSeconds(&lt;DATETIME>, &lt;NUMBER>) | AddSeconds (&quot;2019-12-25 15 :30: 00&quot;, 37) |
| **SubYears** | Trekt het gespecificeerde aantal jaren aan de verstrekte datetime af. | SubYear(&lt;DATETIME>, &lt;NUMBER>) | SubYaren (&quot;2019-12-25 15 :30: 00&quot;, 3) |
| **SubMonths** | Trekt het gespecificeerde aantal maanden aan de verstrekte datetime af. | SubMonths(&lt;DATETIME>, &lt;NUMBER>) | SubMonths (&quot;2019-12-25 15 :30: 00&quot;, 6) |
| **SubDays** | Trekt het gespecificeerde aantal dagen aan de verstrekte datetime af. | SubDays(&lt;DATETIME>, &lt;NUMBER>) | SubDays (&quot;2019-12-25 15 :30: 00&quot;, 10) |
| **SubHours** | Trekt het gespecificeerde aantal uren aan de verstrekte datetime af. | SubHours(&lt;DATETIME>, &lt;NUMBER>) | SubHours (&quot;2019-12-25 15 :30: 00&quot;, 3) |
| **SubMinutes** | Trekt het gespecificeerde aantal minuten aan de verstrekte datetime af. | SubMinutes(&lt;DATETIME>, &lt;NUMBER>) | SubMinutes (&quot;2019-12-25 15 :30: 00&quot;, 32) |
| **SubSeconds** | AdSubtractsds het gespecificeerde aantal seconden aan de verstrekte datetime. | SubSeconds(&lt;DATETIME>, &lt;NUMBER>) | SubSeconds (&quot;2019-12-25 15 :30: 00&quot;, 37) |
| **Year** | Extraheert het jaar vanaf het opgegeven datetime-object. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **Month** | Extraheert de maand vanaf het opgegeven datetime-object. | Maand (&lt;DATETIME>) | Maand (&quot;2019-12-15 15 :30: 00&quot;) |
| **Day** | Extraheert de dag vanaf het opgegeven datetime-object. | Dag (&lt;DATETIME>) | Dag (&quot;2019-12-15 15 :30: 00&quot;) |
| **DayOfYear** | Extraheert de dag van het jaar vanaf het opgegeven datetime-object. Bijvoorbeeld, als de verstrekte datetime 2 Februari is, zou het 33 terugkeren. | DayOfYear(&lt;DATETIME>) | DayOfYear (&quot;2019-12-15 15 :30: 00&quot;) |
| **WeekDay** | Extraheert de dag van de week van het opgegeven datetime-object als een getal van 1 tot en met 7, waarbij 1 de zondag vertegenwoordigt. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **Hour** | Extraheert de uurwaarde van het opgegeven datetime-object. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **Minute** | Extraheert de minutenwaarde uit het opgegeven datetime-object. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **Second** | Extraheert de tweede waarde van het opgegeven datetime-object. | Jaar (&lt;DATETIME>) | Jaar (&quot;2019-12-15 15 :30: 00&quot;) |
| **YearDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van jaren. | YearDiff(&lt;DATETIME>, &lt;DATETIME>) | YarenDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **MonthsDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van maanden. | MonthsDiff(&lt;DATETIME>, &lt;DATETIME>) | MonthsDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **DaysDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van dagen. | DaysDiff(&lt;DATETIME>, &lt;DATETIME>) | DaysDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **HoursDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van uren. | HoursDiff(&lt;DATETIME>, &lt;DATETIME>) | HoursDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **MinutesDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van notulen. | MinutesDiff(&lt;DATETIME>, &lt;DATETIME>) | MinutesDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **SecondsDiff** | Vindt het verschil tussen de bepaalde datetimes, met een granulariteit van seconden. | SecondsDiff(&lt;DATETIME>, &lt;DATETIME>) | SecondsDiff (&quot;2019-12-25 15 :30: 00&quot;, &quot;2018-10-14 18 :35: 27&quot;) |
| **MonthsOld** | Vindt het verschil tussen de bepaalde datum en heden, met een granulariteit van maanden. | MonthsOld(&lt;DATETIME>) | MonthsOld (&quot;2019-12-25 15 :30: 00&quot;) |
| **DaysOld** | Vindt het verschil tussen bepaalde datetime en heden, met een granulariteit van dagen. | DaysOld(&lt;DATETIME>) | DaysOld (&quot;2019-12-25 15 :30: 00&quot;) |
| **GetDate** | Haal de huidige datum van de server op. | GetDate() | GetDate() |
| **DateOnly** | Kort de datetime aan enkel het jaar, de maand, en de dag in. | DateOnly(&lt;DATETIME>) | DateOnly (&quot;2019-12-25 15 :30: 00&quot;) |
| **ToDate** | Hiermee converteert u het veld naar een datumveld. | ToDate(&lt;DATETIME>) | ToDate (&quot;2019-12-25 15 :30: 00&quot;) |
| **ToDateTime** | Hiermee converteert u het veld naar een datetime-veld. | ToDateTime(&lt;DATE>) | ToDateTime (&quot;2019-12-25 15 :30: 00&quot;) |
| **ToTimestamp** | Hiermee converteert u het veld naar een tijdstempelveld. | ToTimestamp(&lt;DATETIME>) | ToTimestamp (&quot;2019-12-25 15 :30: 00&quot;) |
| **Oldest** | Retourneert de oudste datum tussen de twee opgegeven waarden. | Oudst(&lt;DATETIME>, &lt;DATETIME>) | Oudst (&quot;2015-02-13 11 :59: 59&quot;, &quot;2016-04-13 19 :28: 14&quot;) |
| **TruncDate** | Kort de datetime aan de dichtstbijzijnde eenheid in, op basis van de gegeven numerieke waarde. Als de numerieke waarde gelijk is aan 60, wordt deze afgebroken tot de dichtstbijzijnde minuut. Als de numerieke waarde gelijk is aan 3600, wordt deze afgebroken tot het dichtstbijzijnde uur. Als de numerieke waarde gelijk is aan 86400, wordt deze afgebroken tot de dichtstbijzijnde dag. Anders wordt het naar de dichtstbijzijnde seconde afgebroken. | TruncDate(&lt;DATETIME>, &lt;NUMBER>) | TruncDate (&quot;2016-04-13 19 :28: 14&quot;, 3600) |
| **TruncDateTZ** | Kort de datetime aan de dichtstbijzijnde eenheid in, op basis van de gegeven numerieke waarde, en stelt de datetime in op de opgegeven tijdzone. Als de numerieke waarde gelijk is aan 60, wordt deze afgebroken tot de dichtstbijzijnde minuut. Als de numerieke waarde gelijk is aan 3600, wordt deze afgebroken tot het dichtstbijzijnde uur. Als de numerieke waarde gelijk is aan 86400, wordt deze afgebroken tot de dichtstbijzijnde dag. | TruncDateTZ(&lt;DATETIME>, &lt;NUMBER>, &lt;TIMEZONE>) | TruncDateTZ (&quot;2016-04-13 19 :28: 14&quot;, 3600, &quot;America/Los_Angeles&quot;) |
| **TruncTime** | Stelt de datetime in op 1 januari 2000 en rondt de rest van de datetime af op de dichtstbijzijnde eenheid, op basis van de opgegeven numerieke waarde. Als de numerieke waarde gelijk is aan 60, wordt deze verkort tot de dichtstbijzijnde minuut. Als de numerieke waarde gelijk is aan 3600, wordt deze afgebroken tot het dichtstbijzijnde uur. | TruncTime(&lt;DATETIME>, &lt;NUMBER>) | TruncTime (&quot;2016-04-13 19 :28: 14&quot;, 3600) |
| **TruncQuarter** | Kort de datetime aan de eerste datum in het dichtstbijzijnde kwartaal in. | TruncQuarter(&lt;DATETIME>) | TruncQuarter (&quot;2016-04-13 19 :28: 14&quot;) |
| **TruncYear** | Kort de datetime aan de eerste datum in het dichtstbijzijnde jaar in. | TruncYear(&lt;DATETIME>) | TruncYear (&quot;2016-04-13 19 :28: 14&quot;) |
| **TruncWeek** | Kort de datetime aan de Zondag van de dichtstbijzijnde week in. | TruncWeek(&lt;DATETIME>) | TruncWeek (&quot;2016-04-13 19 :28: 14&quot;) |
| **ConvertNTZ** | Converteert een tijdstempel zonder tijdzone naar een tijdstempel met een tijdzone. De bijgevoegde tijdzone is de tijdzone van de externe rekening. | ConvertNTZ(&lt;DATETIME>) | ConvertNTZ (&quot;2024-06-24 14 :43: 49&quot;) |

<!-- 
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") | 
-->

<!-- 
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **DaysAgoInt** | Calculates the number of days between the current date and the provided timestamp, and returns the value as an integer. | DaysAgoInt(&lt;DATETIME&gt;) | DaysAgoInt("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") | 
-->

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AddYears** | Adds the specified number of years to the provided datetime. | AddYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddYears("2019-12-25 15:30:00", 3) |
| **AddMonths** | Adds the specified number of months to the provided datetime. | AddMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMonths("2019-12-25 15:30:00", 6) |
| **AddDays** | Adds the specified number of days to the provided datetime. | AddDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddDays("2019-12-25 15:30:00", 10) |
| **AddHours** | Adds the specified number of hours to the provided datetime. | AddHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddHours("2019-12-25 15:30:00", 3) |
| **AddMinutes** | Adds the specified number of minutes to the provided datetime. | AddMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddMinutes("2019-12-25 15:30:00", 32) |
| **AddSeconds** | Adds the specified number of seconds to the provided datetime. | AddSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | AddSeconds("2019-12-25 15:30:00", 37) |
| **SubYears** | Subtracts the specified number of years to the provided datetime. | SubYears(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubYears("2019-12-25 15:30:00", 3) |
| **SubMonths** | Adds the specified number of months to the provided datetime. | SubMonths(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMonths("2019-12-25 15:30:00", 6) |
| **SubDays** | Adds the specified number of days to the provided datetime. | SubDays(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubDays("2019-12-25 15:30:00", 10) |
| **SubHours** | Adds the specified number of hours to the provided datetime. | SubHours(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubHours("2019-12-25 15:30:00", 3) |
| **SubMinutes** | Adds the specified number of minutes to the provided datetime. | SubMinutes(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubMinutes("2019-12-25 15:30:00", 32) |
| **SubSeconds** | Adds the specified number of seconds to the provided datetime. | SubSeconds(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | SubSeconds("2019-12-25 15:30:00", 37) |
| **Year** | Extracts the year from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Month** | Extracts the month from the given datetime object. | Month(&lt;DATETIME&gt;) | Month("2019-12-15 15:30:00") |
| **Day** | Extracts the day from the given datetime object. | Day(&lt;DATETIME&gt;) | Day("2019-12-15 15:30:00") |
| **DayOfYear** | Extracts the day of year from the given datetime object. For example, if the provided datetime is February 2nd, it would return 33. | DayOfYear(&lt;DATETIME&gt;) | DayOfYear("2019-12-15 15:30:00") |
| **WeekDay** | Extracts the day of the week from the given datetime object, as a number from 1 to 7, with 1 representing Sunday. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Hour** | Extracts the hour value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Minute** | Extracts the minute value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **Second** | Extracts the second value from the given datetime object. | Year(&lt;DATETIME&gt;) | Year("2019-12-15 15:30:00") |
| **YearsDiff** | Finds the difference between the given datetimes, with a granularity of years. | YearsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | YearsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MonthsDiff** | Finds the difference between the given datetimes, with a granularity of months. | MonthsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MonthsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **DaysDiff** | Finds the difference between the given datetimes, with a granularity of days. | DaysDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | DaysDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **HoursDiff** | Finds the difference between the given datetimes, with a granularity of hours. | HoursDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | HoursDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **MinutesDiff** | Finds the difference between the given datetimes, with a granularity of minutes. | MinutesDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | MinutesDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **SecondsDiff** | Finds the difference between the given datetimes, with a granularity of seconds. | SecondsDiff(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | SecondsDiff("2019-12-25 15:30:00", "2018-10-14 18:35:27") |
| **YearsOld** | Finds the difference between the given datetime and the present, with a granularity of years. | YearsOld(&lt;DATETIME&gt;) | YearsOld("2019-12-25 15:30:00") |
| **MonthsOld** | Finds the difference between the given datetime and the present, with a granularity of months. | MonthsOld(&lt;DATETIME&gt;) | MonthsOld("2019-12-25 15:30:00") |
| **DaysOld** | Finds the difference between the given datetime and the present, with a granularity of days. | DaysOld(&lt;DATETIME&gt;) | DaysOld("2019-12-25 15:30:00") |
| **GetDate** | Get the current date of the server. | GetDate() | GetDate() |
| **DateOnly** | Truncates the datetime to just the year, month, and day. | DateOnly(&lt;DATETIME&gt;) | DateOnly("2019-12-25 15:30:00") |
| **ToDate** | Converts the field to a date field. | ToDate(&lt;DATETIME&gt;) | ToDate("2019-12-25 15:30:00") |
| **ToDateTime** | Converts the field to a datetime field. | ToDateTime(&lt;DATE&gt;) | ToDateTime("2019-12-25 15:30:00") |
| **ToTimestamp** | Converts the field to a timestamp field. | ToTimestamp(&lt;DATETIME&gt;) | ToTimestamp("2019-12-25 15:30:00") |
| **YearAndMonth** | Truncates the datetime to just the year and month. | YearAndMonth(&lt;DATETIME&gt;) | YearAndMonth("2019-12-25 15:30:00") |
| **Oldest** | Returns the oldest date between the two provided. | Oldest(&lt;DATETIME&gt;, &lt;DATETIME&gt;) | Oldest("2015-02-13 11:59:59", "2016-04-13 19:28:14") |
| **TruncDate** | Truncates the datetime to the nearest unit, based on the numerical value given. If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. If the numeric value is equal to 86400, it truncates to the nearest day. Otherwise, it truncates to the nearest second. | TruncDate(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncDate("2016-04-13 19:28:14", 3600) |
| **TruncTime** | Sets the datetime to January 1st, 2000 and rounds the rest of the datetime to the nearest unit, based on the numerical value given.If the numeric value is equal to 60, it truncates to the nearest minute. If the numeric value is equal to 3600, it truncates to the nearest hour. | TruncTime(&lt;DATETIME&gt;, &lt;NUMBER&gt;) | TruncTime("2016-04-13 19:28:14", 3600) |
| **TruncQuarter** | Truncates the datetime to the first date in the nearest quarter. | TruncQuarter(&lt;DATETIME&gt;) | TruncQuarter("2016-04-13 19:28:14") |
| **TruncYear** | Truncates the datetime to the first date in the nearest year. | TruncYear(&lt;DATETIME&gt;) | TruncYear("2016-04-13 19:28:14") |
| **TruncWeek** | Truncates the datetime to the Sunday of the nearest week. | TruncWeek(&lt;DATETIME&gt;) | TruncWeek("2016-04-13 19:28:14") |
| **DaysAgo** | Calculates the number of days between the current date and the provided timestamp, and returns the value as a datetime. | DaysAgo(&lt;DATETIME&gt;) | DaysAgo("2024-06-24 14:43:49") |
| **MonthsAgo** | Calculates the number of months between the current date and the provided timestamp, and returns the value as a datetime. | MonthsAgo(&lt;DATETIME&gt;) | MonthsAgo("2024-06-24 14:43:49") |
| **YearsAgo** | Calculates the number of years between the current date and the provided timestamp, and returns the value as a datetime. | YearsAgo(&lt;DATETIME&gt;) | YearsAgo("2024-06-24 14:43:49") |
-->

>[!ENDTABS]

>[!NOTE]
>
>Merk op dat de **functie Dateonly** rekening houdt met timezone van de server, niet de exploitant.

### Geomarketing

De geomarketing-functies worden gebruikt om geografische waarden te manipuleren.

>[!BEGINTABS]

>[!TAB  Google BigQuery ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **Distance** | Retourneert de afstand tussen twee punten die door hun lengtegraad en breedtegraad in graden worden gedefinieerd, als een dubbele waarde. | Afstand (&lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>) | Afstand(40.345, 39.2345, -35.5834, 34.599) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

>[!TAB Redshift]

Geomarketing functions are not available.

-->

>[!TAB  Snowflake ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **Distance** | Retourneert de afstand tussen twee punten die door hun lengtegraad en breedtegraad in graden worden gedefinieerd, als een dubbele waarde. | Afstand (&lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>, &lt;NUMBER>) | Afstand(40.345, 39.2345, -35.5834, 34.599) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Distance** | Returns the distance between two points defined by their longitude and latitude in degrees, as a double. | Distance(&lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;, &lt;NUMBER&gt;) | Distance(40.345, 39.2345, -35.5834, 34.599) |

-->

>[!ENDTABS]

### Numeriek

De numerieke functies worden gebruikt om tekst om te zetten in getallen.

>[!BEGINTABS]

>[!TAB  Google BigQuery ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **Mod** | Retourneert de rest van het eerste getal gedeeld door het tweede getal. | Mod(&lt;NUMBER>, &lt;NUMBER>) | Mod (3, 2) |
| **Percent** | Berekent welk percentage het eerste getal van het tweede getal is. | Percentage (&lt;NUMBER>, &lt;NUMBER>) | Percentage (1, 2) |
| **Random** | Retourneert een willekeurig getal tussen 0 (exclusief) en 1 (exclusief). | Random() | Willekeurig () |
| **Round** | Retourneert het opgegeven getal naar de dichtstbijzijnde aangevraagde decimale waarde. | Round(&lt;NUMBER>, &lt;NUMBER>) | Round(4.5394, 2) |
| **ToDouble** | Zet het verstrekte aantal in een dubbel. | ToDouble(&lt;NUMBER>) | ToDouble(5) |
| **ToInteger** | Zet het opgegeven getal om in een geheel getal. | ToInteger(&lt;NUMBER>) | ToInteger(45) |
| **ToInt64** | Zet het verstrekte aantal in een geheel met 64 bits om. | ToInt64(&lt;NUMBER>) | ToInt64(493) |
| **Trunc** | Kort het opgegeven getal in tot het gewenste aantal decimalen. | Trunc(&lt;NUMBER>, &lt;NUMBER>) | Trunc(36.9348934, 3) |

<!-- 
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Floor** | Rounds down the provided number to the nearest integer. For example, if the provided number is 3.8, it will return 3. | Floor(&lt;NUMBER&gt;) | Floor(3.8) |
| **Greatest** | Returns the larger number between the two provided numbers. | Greatest(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Greatest(1, 2) |
| **Least** | Returns the smaller number between the two provided numbers. | Least(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Least (1,2) |
 -->

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Ceil** | Rounds up the provided number to the nearest integer. For example, if the provided number is 2.3, it will return 3. | Ceil(&lt;NUMBER&gt;) | Ceil(2.3) |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

>[!TAB Redshift]

Numeric functions are not available.

--->

>[!TAB  Snowflake ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **Mod** | Retourneert de rest van het eerste getal gedeeld door het tweede getal. | Mod(&lt;NUMBER>, &lt;NUMBER>) | Mod (3, 2) |
| **Percent** | Berekent welk percentage het eerste getal van het tweede getal is. | Percentage (&lt;NUMBER>, &lt;NUMBER>) | Percentage (1, 2) |
| **Random** | Retourneert een willekeurig getal tussen 0 (exclusief) en 1 (exclusief). | Random() | Willekeurig () |
| **ToDouble** | Zet het verstrekte aantal in een dubbel. | ToDouble(&lt;NUMBER>) | ToDouble(5) |
| **ToInteger** | Zet het opgegeven getal om in een geheel getal. | ToInteger(&lt;NUMBER>) | ToInteger(45) |
| **ToInt64** | Zet het verstrekte aantal in een geheel met 64 bits om. | ToInt64(&lt;NUMBER>) | ToInt64(493) |
| **Trunc** | Kort het opgegeven getal in tot het gewenste aantal decimalen. | Trunc(&lt;NUMBER>, &lt;NUMBER>) | Trunc(36.9348934, 3) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Mod** | Returns the remainder of the first number divided by the second number. | Mod(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Mod (3, 2) |
| **Percent** | Calculates what percentage the first number is of the second number. | Percent(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Percent(1, 2) |
| **Random** | Returns a random number between 0 (inclusive) and 1 (exclusive). | Random() | Random () |
| **ToDouble** | Converts the provided number to a double. | ToDouble(&lt;NUMBER&gt;) | ToDouble(5) |
| **ToInteger** | Converts the provided number to an integer. | ToInteger(&lt;NUMBER&gt;) | ToInteger(45) |
| **ToInt64** | Converts the provided number to a 64-bit integer. | ToInt64(&lt;NUMBER&gt;) | ToInt64(493) |
| **Trunc** | Truncates the provided number to the requested number of decimal places. | Trunc(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | Trunc(36.9348934, 3) |

--->

>[!ENDTABS]

### Overige

Deze tabel bevat de resterende beschikbare functies.

>[!BEGINTABS]

>[!TAB  Google BigQuery ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **Case** | Retourneert de eerste waarde als de expressie true is. Anders wordt de tweede waarde geretourneerd. | Case(When(&lt;EXPRESSION> &lt;VALUE>), else(&lt;VALUE>) | Case(When(a > b, &quot;yes&quot;), Else(&quot;no&quot;) |
| **When** | Wordt gebruikt als onderdeel van de functie Case. Wordt gebruikt om de expressie te controleren in Hoofdletters en kleine letters. | When(&lt;EXPRESSION> &lt;VALUE>) | Wanneer(a > b, &quot;ja&quot;) |
| **Else** | Wordt gebruikt als onderdeel van de functie Case. Wordt gebruikt om de andere optie te kiezen als de expressie Bij onwaar is. | else(&lt;VALUE>) | Anders (&quot;nee&quot;) |
| **Coalesce** | Retourneert de eerste niet-null-waarde. | Coalesce(&lt;VALUE>, &lt;VALUE>) | Coalesce (&quot;&quot;, &quot;string&quot;) |
| **Decode** | Retourneert de eerste optie als de waarden gelijk zijn. Retourneert de tweede optie als de waarden niet gelijk zijn. | Decode(&lt;VALUE>, &lt;VALUE>, &lt;VALUE>, &lt;VALUE>) | Decode(1, 2, &quot;true&quot;, &quot;false&quot;) |
| **GetEmailDomain** | Extraheert het domein van het opgegeven e-mailadres. | GetEmailDomain(&lt;STRING>) | GetEmailDomain(&quot;sample@example.com&quot;) |
| **Iif** | Retourneert de eerste optie als de voorwaarde true is en retourneert de tweede optie als de voorwaarde false is. | IF(&lt;CONDITION>, &lt;VALUE>, &lt;VALUE>) | IF(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | Retourneert de eerste optie als de tekenreeks leeg is. Anders wordt de tweede optie geretourneerd. | IsEmptyString( &lt;STRING> ,&lt;VALUE>, &lt;VALUE>) | IsEmptyString(&quot;string&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **NewUID** | Genereert een nieuwe unieke UID. | NewUID() | NewUID() |
| **NoNull** | Retourneert de opgegeven tekenreeks als deze niet leeg is en retourneert een lege tekenreeks als de opgegeven tekenreeks leeg is. | NoNull(&lt;STRING>) | NoNull(&quot;test&quot;) |
| **IsBitSet** | Voert bitsgewijze en (&amp;) uit op de opgegeven getallen. Hiermee kunt u controleren of het bit binnen de eerste parameter is ingesteld op de positie die in de tweede parameter is opgegeven. | IsBitSet(&lt;NUMBER>, &lt;NUMBER>) | IsBitSet(5, 3) |
| **ClearBit** | Hierdoor kunt u het bit binnen de eerste parameter wissen op de positie die in de tweede parameter is opgegeven. | ClearBit(&lt;NUMBER>, &lt;NUMBER>) | |
| **SetBit** | Voert bitsgewijze of (\|) uit op de opgegeven getallen. Hierdoor kunt u het bit binnen de eerste parameter instellen op de positie die in de tweede parameter wordt opgegeven. | SetBit(&lt;NUMBER>, &lt;NUMBER>) | SetBit(5, 3) |
| **RowId** | Retourneert het regelnummer. | RowId() | RowId() |
| **ToBoolean** | Zet de waarde om in een booleaanse waarde. | ToBoolean(&lt;VALUE>) | ToBoolean(a=b) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBool(&lt;VALUE&gt;) | ToBool(a=b) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |

>[!TAB Redshift]

Other functions are not available.

--->

>[!TAB  Snowflake ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **Case** | Retourneert de eerste waarde als de expressie true is. Anders wordt de tweede waarde geretourneerd. | Case(When(&lt;EXPRESSION> &lt;VALUE>), else(&lt;VALUE>) | Case(When(a > b, &quot;yes&quot;), Else(&quot;no&quot;) |
| **When** | Wordt gebruikt als onderdeel van de functie Case. Wordt gebruikt om de expressie te controleren in Hoofdletters en kleine letters. | When(&lt;EXPRESSION> &lt;VALUE>) | Wanneer(a > b, &quot;ja&quot;) |
| **Else** | Wordt gebruikt als onderdeel van de functie Case. Wordt gebruikt om de andere optie te kiezen als de expressie Bij onwaar is. | else(&lt;VALUE>) | Anders (&quot;nee&quot;) |
| **GetEmailDomain** | Extraheert het domein van het opgegeven e-mailadres. | GetEmailDomain(&lt;STRING>) | GetEmailDomain(&quot;sample@example.com&quot;) |
| **Iif** | Retourneert de eerste optie als de voorwaarde true is en retourneert de tweede optie als de voorwaarde false is. | IF(&lt;CONDITION>, &lt;VALUE>, &lt;VALUE>) | IF(10 &lt; 20, &quot;true&quot;, &quot;false&quot;) |
| **IsEmptyString** | Retourneert de eerste optie als de tekenreeks leeg is. Anders wordt de tweede optie geretourneerd. | IsEmptyString( &lt;STRING> ,&lt;VALUE>, &lt;VALUE>) | IsEmptyString(&quot;string&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **ToBoolean** | Retourneert 1 als de waarde true is. Retourneert 0 als de waarde false is. | ToBoolean(&lt;VALUE>) | ToBoolean(a=b) |
| **ToBooleanType** | Zet de waarde om in een booleaanse waarde. | ToBooleanType(&lt;VALUE>) | ToBooleanType(a=b) |
| **IsBitSet** | Voert bitsgewijze en (&amp;) uit op de opgegeven getallen. Hiermee kunt u controleren of het bit binnen de eerste parameter is ingesteld op de positie die in de tweede parameter is opgegeven. | IsBitSet(&lt;NUMBER>, &lt;NUMBER>) | IsBitSet(5, 3) |
| **ClearBit** | Hierdoor kunt u het bit binnen de eerste parameter wissen op de positie die in de tweede parameter is opgegeven. | ClearBit(&lt;NUMBER>, &lt;NUMBER>) | |
| **SetBit** | Voert bitsgewijze of (\|) uit op de opgegeven getallen. Hierdoor kunt u het bit binnen de eerste parameter instellen op de positie die in de tweede parameter wordt opgegeven. | SetBit(&lt;NUMBER>, &lt;NUMBER>) | SetBit(5, 3) |
| **RowId** | Retourneert het regelnummer. | RowId() | RowId() |
| **NewUID** | Genereert een nieuwe unieke UID. | NewUID() | NewUID() |
| **NoNull** | Retourneert de opgegeven tekenreeks als deze niet leeg is en retourneert een lege tekenreeks als de opgegeven tekenreeks leeg is. | NoNull(&lt;STRING>) | NoNull(&quot;test&quot;) |
| **AESEncrypt** | Codeert de opgegeven tekenreeks met het AES-coderingstype. | AESEncrypt() | AESEncrypt(&quot;hello&quot;) |
| **ObjectConstruct** | Maakt een object dat is gebaseerd op de opgegeven sleutel-/waardeparen. | ObjectConstruct(&lt;STRING>, &lt;STRING>) | ObjectConstruct(&quot;key&quot;, &quot;value&quot;) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **Case** | Returns the first value if the expression is true. Otherwise, returns the second value. | Case(When(&lt;EXPRESSION&gt; &lt;VALUE&gt;), Else(&lt;VALUE&gt;)) | Case(When(a > b, "yes"), Else("no")) |
| **When** | Used as part of the Case function. Used to check the expression within Case. | When(&lt;EXPRESSION&gt; &lt;VALUE&gt;) | When(a > b, "yes") |
| **Else** | Used as part of the Case function. Used to choose the other option, if the When expression is false. | Else(&lt;VALUE&gt;) | Else ("no") |
| **Coalesce** | Returns the first non-null value. | Coalesce(&lt;VALUE&gt;, &lt;VALUE&gt;) | Coalesce ("", "string") |
| **GetEmailDomain** | Extracts the domain from the provided email address. | GetEmailDomain(&lt;STRING&gt;) | GetEmailDomain("sample@example.com") |
| **Iif** | Returns the first option if the condition is true and returns the second option if the condition is false. | Iif(&lt;CONDITION&gt;, &lt;VALUE&gt;, &lt;VALUE&gt;) | Iif(10 < 20, "true", "false") |
| **IsBitSet** | Performs a bitwise and (&) on the provided numbers. This lets you check if the bit within the first parameter is set at the position provided in the second parameter. | IsBitSet(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | IsBitSet(5, 3) |
| **ClearBit** | This lets your clear the bit within the first parameter at the position provided in the second parameter. | ClearBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | |
| **SetBit** | Performs a bitwise or (\|) on the provided numbers. This lets you set the bit within the first parameter is set at the position provided in the second parameter. | SetBit(&lt;NUMBER&gt;, &lt;NUMBER&gt;) | SetBit(5, 3) |
| **IsEmptyString** | Returns the first option if the string is empty. Otherwise, returns the second option. | IsEmptyString( &lt;STRING&gt; ,&lt;VALUE&gt;, &lt;VALUE&gt;) | IsEmptyString("string", "yes", "no") |
| **NewUUID** | Generates a new unique UUID. | NewUUID() | NewUUID() |
| **NoNull** | Returns the provided string if it's not empty, and returns an empty string if the provided string is empty. | NoNull(&lt;STRING&gt;) | NoNull("test") |
| **RowId** | Returns the line number. | RowId() | RowId() |
| **ToBoolean** | Converts the value to a boolean. | ToBoolean(&lt;VALUE&gt;) | ToBoolean(a=b) |

-->

>[!ENDTABS]

### String

De tekenreeksfuncties worden gebruikt om een set tekenreeksen te manipuleren.

>[!BEGINTABS]

>[!TAB  Google BigQuery ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Neemt twee tekenreeksen en controles als alle tekenreeksen niet null en niet leeg zijn. | AllNonNull2(&lt;STRING>, &lt;STRING>) | AllNonNull2(&quot;&quot;, &quot;string2&quot;) |
| **AllNonNull3** | Neemt drie tekenreeksen en controleert of alle tekenreeksen niet null en niet leeg zijn | AllNonNull3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | AllNonNull3(&quot;&quot;, &quot;one&quot;, &quot;three&quot;) |
| **Ascii** | Neemt een tekenreeks en retourneert de resulterende tekenreeks. | Ascii(&lt;STRING>) | Ascii (&quot;foo&quot;) |
| **Char** | Neemt een array van Unicode-codepunten en retourneert de resulterende tekenreeks. | Char(&lt;ARRAY>) | Char ([ 65, 68, 79, 66, 69 ]) |
| **Charindex** | Vindt het eerste voorkomen van het gespecificeerde substring binnen het belangrijkste koord. | Charindex(&lt;STRING>, &lt;SUBSTRING>) | Charindex (&quot;bar@example.com&quot;, &quot;@&quot;) |
| **dataLength** | Geeft het aantal bytes in de tekenreeks. | dataLength(&lt;STRING>) | dataLength(&quot;Mijn tekenreeks&quot;) |
| **GetLine** | Retourneer de aangevraagde regel van de opgegeven tekenreeks. | GetLine(&lt;STRING>, &lt;NUMBER>) | GetLine(multiline string, 5) |
| **IfEquals** | Neemt vier tekenreeksen en retourneert de derde tekenreeks als de eerste twee tekenreeksen gelijk zijn en retourneert de vierde tekenreeks als de eerste twee tekenreeksen niet gelijk zijn. | IfEquals(&lt;STRING>, &lt;STRING>, &lt;STRING>, &lt;STRING>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **IsMemoNull** | Retourneert 1 als de tekenreeks null is, anders retourneert deze 0. | IsMemoNull(&lt;STRING>) | IsMemoNull(&quot;hello&quot;) |
| **JuxtWords** | Neemt twee tekenreeksen en combineert deze tot één tekenreeks. Spaties tussen de tekenreeksen worden indien nodig toegevoegd. | JuxtWords(&lt;STRING>, &lt;STRING>) | JuxtWords(&quot;Hello&quot;, &quot;World&quot;) |
| **JuxtWords3** | Neemt drie tekenreeksen en combineert deze tot één tekenreeks. Spaties tussen de tekenreeksen worden indien nodig toegevoegd. | JuxtWords3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | JuxtWords3(&quot;Hello&quot;, &quot;New&quot;, &quot;World&quot;) |
| **Left** | Neemt een tekenreeks en retourneert de meest linkse tekens zoals opgegeven. | Left(&lt;STRING>, &lt;NUMBER>) | Left(&quot;Substring&quot;, 3) |
| **Length** | Retourneert de lengte van de tekenreeks. | Lengte (&lt;STRING>) | Length(&quot;MyString&quot;) |
| **Md5Digest** | Zet de MD5-hashed-tekenreeks om in de hexadecimale representatie. | Md5Digest(&lt;STRING>) | Md5Digest(&quot;String&quot;) |
| **MemoContains** | Controleert of de tekenreeks de opgegeven subtekenreeks bevat. | MemoContains(&lt;STRING>, &lt;STRING>) | memoContains(&quot;string&quot;, &quot;str&quot;) |
| **Right** | Neemt een tekenreeks en retourneert de meest rechtse tekens zoals opgegeven. | Right(&lt;STRING>, &lt;NUMBER>) | Right (&quot;Substring&quot;, 3) |
| **Smart** | Retourneert de tekenreeks met de eerste letter van elk woord met hoofdletter. | Smart(&lt;STRING>) | Smart(&quot;hello world&quot;) |
| **Substring** | Neem een tekenreeks en retourneert een deel van de opgegeven tekenreeks op basis van de opgegeven posities. | Substring(&lt;STRING>, &lt;LEFT_NUMBER>, RIGHT_NUMBER>) | Substring(&quot;Substring&quot;, 3, 5) |
| **Sha256Digest** | Zet de SHA256-gehakte koord in zijn hexadecimale vertegenwoordiging om. | Sha256Digest(&lt;STRING>) | Sha256Digest(&quot;tekenreeks&quot;) |
| **Sha512Digest** | Zet de SHA512-hashed koord in zijn hexadecimale vertegenwoordiging om. | Sha512Digest(&lt;STRING>) | Sha512Digest(&quot;string&quot;) |
| **ToString** | Retourneert de waarde als een tekenreeks. | ToString(&lt;VALUE>) | ToString(123) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **IsMemoNull** |  Returns 1 if the string is null, otherwise it returns 0. | IsMemoNull(&lt;STRING&gt;) | IsMemoNull("hello") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |

>[!TAB Redshift]

String functions are not available.

-->

>[!TAB  Snowflake ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Neemt twee tekenreeksen en controles als alle tekenreeksen niet null en niet leeg zijn. | AllNonNull2(&lt;STRING>, &lt;STRING>) | AllNonNull2(&quot;&quot;, &quot;string2&quot;) |
| **AllNonNull3** | Neemt drie tekenreeksen en controleert of alle tekenreeksen niet null en niet leeg zijn | AllNonNull3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | AllNonNull3(&quot;&quot;, &quot;one&quot;, &quot;three&quot;) |
| **Char** | Neemt een array van Unicode-codepunten en retourneert de resulterende tekenreeks. | Char(&lt;ARRAY>) | Char ([ 65, 68, 79, 66, 69 ]) |
| **Charindex** | Vindt het eerste voorkomen van het gespecificeerde substring binnen het belangrijkste koord. | Charindex(&lt;STRING>, &lt;SUBSTRING>) | Charindex (&quot;bar@example.com&quot;, &quot;@&quot;) |
| **dataLength** | Geeft het aantal bytes in de tekenreeks. | dataLength(&lt;STRING>) | dataLength(&quot;Mijn tekenreeks&quot;) |
| **GetLine** | Retourneer de aangevraagde regel van de opgegeven tekenreeks. | GetLine(&lt;STRING>, &lt;NUMBER>) | GetLine(multiline string, 5) |
| **IfEquals** | Neemt vier tekenreeksen en retourneert de derde tekenreeks als de eerste twee tekenreeksen gelijk zijn en retourneert de vierde tekenreeks als de eerste twee tekenreeksen niet gelijk zijn. | IfEquals(&lt;STRING>, &lt;STRING>, &lt;STRING>, &lt;STRING>) | IfEquals(&quot;a&quot;, &quot;a&quot;, &quot;yes&quot;, &quot;no&quot;) |
| **IsMemoNull** | Retourneert 1 als de tekenreeks null is, anders retourneert deze 0. | IsMemoNull(&lt;STRING>) | IsMemoNull(&quot;hello&quot;) |
| **JuxtWords** | Neemt twee tekenreeksen en combineert deze tot één tekenreeks. Spaties tussen de tekenreeksen worden indien nodig toegevoegd. | JuxtWords(&lt;STRING>, &lt;STRING>) | JuxtWords(&quot;Hello&quot;, &quot;World&quot;) |
| **JuxtWords3** | Neemt drie tekenreeksen en combineert deze tot één tekenreeks. Spaties tussen de tekenreeksen worden indien nodig toegevoegd. | JuxtWords3(&lt;STRING>, &lt;STRING>, &lt;STRING>) | JuxtWords3(&quot;Hello&quot;, &quot;New&quot;, &quot;World&quot;) |
| **Left** | Neemt een tekenreeks en retourneert de meest linkse tekens zoals opgegeven. | Left(&lt;STRING>, &lt;NUMBER>) | Left(&quot;Substring&quot;, 3) |
| **Length** | Retourneert de lengte van de tekenreeks. | Lengte (&lt;STRING>) | Length(&quot;MyString&quot;) |
| **Lijn** | Retourneert de opgegeven genummerde regel van de tekenreeks. | Regel (&lt;STRING>, &lt;NUMBER>) | Regel (multiline-tekenreeks, 5) |
| **Md5Digest** | Zet de MD5-hashed-tekenreeks om in de hexadecimale representatie. | Md5Digest(&lt;STRING>) | Md5Digest(&quot;String&quot;) |
| **Replace** | Neemt een tekenreeks en vervangt alle instanties van de subtekenreeks door een vervangende subtekenreeks. | Vervangen(&lt;STRING>, &lt;STRING&amp;gt, &lt;STRING&amp;gt) | Replace(&quot;Kapitein Steve&quot;, &quot;kapitein&quot;, &quot;ingenieur&quot;) |
| **Right** | Neemt een tekenreeks en retourneert de meest rechtse tekens zoals opgegeven. | Right(&lt;STRING>, &lt;NUMBER>) | Right (&quot;Substring&quot;, 3) |
| **Sha256Digest** | Zet de SHA256-gehakte koord in zijn hexadecimale vertegenwoordiging om. | Sha256Digest(&lt;STRING>) | Sha256Digest(&quot;tekenreeks&quot;) |
| **Sha512Digest** | Zet de SHA512-hashed koord in zijn hexadecimale vertegenwoordiging om. | Sha512Digest(&lt;STRING>) | Sha512Digest(&quot;string&quot;) |
| **Smart** | Retourneert de tekenreeks met de eerste letter van elk woord met hoofdletter. | Smart(&lt;STRING>) | Smart(&quot;hello world&quot;) |
| **ToString** | Retourneert de waarde als een tekenreeks. | ToString(&lt;VALUE>) | ToString(123) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **AllNonNull2** | Takes two strings and checks if all of them are not null and not empty. |  AllNonNull2(&lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull2("", "string2") | 
| **AllNonNull3** | Takes three strings and checks if all of them are not null and not empty | AllNonNull3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | AllNonNull3("", "one", "three") |
| **Char** | Takes an array of Unicode codepoints and returns the resulting string. | Char(&lt;ARRAY&gt;) | Char([65, 68, 79, 66, 69]) |
| **Charindex** | Finds the first occurrence of the specified substring within the main string. | Charindex(&lt;STRING&gt;, &lt;SUBSTRING&gt;) | Charindex ("bar@example.com", "@") |
| **dataLength** | Returns the number of bytes in the string. | dataLength(&lt;STRING&gt;) | dataLength("My string") |
| **GetLine** | Return the requested line of the provided string. | GetLine(&lt;STRING&gt;, &lt;NUMBER&gt;) | GetLine(multilinestring, 5) |
| **IfEquals** | Takes four strings and returns the third string if the first two strings are equal and returns the fourth string if the first two strings are not equal. | IfEquals(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | IfEquals("a", "a", "yes", "no") |
| **JuxtWords** | Takes two strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords(&lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords("Hello", "World") |
| **JuxtWords3** | Takes three strings and combines them into a single string. Spaces between the strings are added if required. | JuxtWords3(&lt;STRING&gt;, &lt;STRING&gt;, &lt;STRING&gt;) | JuxtWords3("Hello", "New", "World") |
| **Left** | Takes a string and returns the leftmost characters as specified. | Left(&lt;STRING&gt;, &lt;NUMBER&gt;) | Left("Substring", 3) |
| **Length** | Returns the length of the string. | Length(&lt;STRING&gt;) | Length("MyString") |
| **LPad** | Pads the provided string on the left side with the padding string up to the length given. | LPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | LPad("LongerString", 15, "ch") |
| **Md5Digest** | Converts the MD5-hashed string into its hexadecimal representation. |  Md5Digest(&lt;STRING&gt;) | Md5Digest("String") |
| **Right** | Takes a string and returns the rightmost characteres as specified. | Right(&lt;STRING&gt;, &lt;NUMBER&gt;)  | Right ("Substring", 3) |
| **RPad** | Pads the provided string on the right side with the padding string up to the length given. | RPad(&lt;STRING&gt;, &lt;NUMBER&gt;, &lt;STRING&gt;) | RPad("LongerString", 15, "ch") |
| **Sha256Digest** | Converts the SHA256-hashed string into its hexadecimal representation. | Sha256Digest(&lt;STRING&gt;)  | Sha256Digest("string") |
| **Sha512Digest** | Converts the SHA512-hashed string into its hexadecimal representation. | Sha512Digest(&lt;STRING&gt;)  | Sha512Digest("string") |
| **Smart** | Returns the string with the first letter of each word capitalized. | Smart(&lt;STRING&gt;) | Smart("hello world") |
| **ToString** | Returns the value as a string. | ToString(&lt;VALUE&gt;) | ToString(123) |

-->

>[!ENDTABS]

### Venster

>[!BEGINTABS]

>[!TAB  Google BigQuery ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Retourneert een reeks rijen op basis van de tabelpartitie en de sorteervolgorde. | RowNum(PartitionBy(&lt;EXPRESSION>), OrderBy(&lt;EXPRESSION>) | RowNum(PartitionBy(Division), OrderBy(time)) |
| **PartitionBy** | Hiermee scheidt u de invoerrijen in verschillende verdelingen op basis van de gegeven expressie. | PartitionBy(&lt;EXPRESSION>) | PartitionBy(delen) |
| **OrderBy** | Hiermee sorteert u het resultaat van de partitie. | OrderBy(&lt;EXPRESSION>) | OrderBy(age) |
| **Desc** | Laat uw OrderBy soort door dalende orde, eerder dan het stijgen orde. | Desc(OrderBy(&lt;EXPRESSION>) | Desc(OrderBy(age)) |

<!-- 

>[!TAB Databricks]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Fabric]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

>[!TAB Redshift]

Window functions are not available.

--->

>[!TAB  Snowflake ]

| Naam | Beschrijving | Syntaxis | Voorbeeld |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Retourneert een reeks rijen op basis van de tabelpartitie en de sorteervolgorde. | RowNum(PartitionBy(&lt;EXPRESSION>), OrderBy(&lt;EXPRESSION>) | RowNum(PartitionBy(Division), OrderBy(time)) |
| **PartitionBy** | Hiermee scheidt u de invoerrijen in verschillende verdelingen op basis van de gegeven expressie. | PartitionBy(&lt;EXPRESSION>) | PartitionBy(delen) |
| **OrderBy** | Hiermee sorteert u het resultaat van de partitie. | OrderBy(&lt;EXPRESSION>) | OrderBy(age) |
| **Desc** | Laat uw OrderBy soort door dalende orde, eerder dan het stijgen orde. | Desc(OrderBy(&lt;EXPRESSION>) | Desc(OrderBy(age)) |

<!-- 

>[!TAB Vertica]

| Name | Description | Syntax | Example |
| ---- | ----------- | ------ | ------- |
| **RowNum** | Returns a sequence of rows based on the table partition and the sorting sequence. | RowNum(PartitionBy(&lt;EXPRESSION&gt;), OrderBy(&lt;EXPRESSION&gt;)) | RowNum(PartitionBy(division), OrderBy(time)) |
| **PartitionBy** | Separates the input rows into different partitions, based on the expression given. | PartitionBy(&lt;EXPRESSION&gt;) | PartitionBy(division) |
| **OrderBy** | Sorts the result of the partition. | OrderBy(&lt;EXPRESSION&gt;) | OrderBy(age) |
| **Desc** | Lets your OrderBy sort by descending order, rather than ascending order. | Desc(OrderBy(&lt;EXPRESSION&gt;)) | Desc(OrderBy(age)) |

-->

>[!ENDTABS]
