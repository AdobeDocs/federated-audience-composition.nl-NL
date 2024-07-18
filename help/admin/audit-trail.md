---
audience: end-user
title: Aan de slag met Audittrail
description: Leer hoe u uw databases kunt controleren met de audittrail
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: bdef7049ee78c512857adcf7d587066eaf80046e
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 2%

---

# Aan de slag met Audittrail {#audit-trail}

>[!CONTEXTUALHELP]
>id="dc_audit_trail"
>title="Audit trail"
>abstract="De mogelijkheden van het audittrail verstrekken een gedetailleerd en chronologisch verslag van alle acties en gebeurtenissen die aan uw milieu in real time zijn gemaakt."

De mogelijkheden van het audittrail verstrekken een gedetailleerd en chronologisch verslag van alle acties en gebeurtenissen die aan uw milieu in real time zijn gemaakt

De functie **[!UICONTROL Audit trail]** registreert constant een gedetailleerd logboek van acties en gebeurtenissen die binnen de instantie van de Samenstelling van Gegevens van de Adobe in real time plaatsvinden. Het biedt een geschikte methode aan om tot een chronologisch verslag van gegevens toegang te hebben, die vragen zoals: de status van werkschema&#39;s, de recentste individuen richten om hen te wijzigen, of de activiteiten richten die door gebruikers binnen de instantie worden uitgevoerd.

+++ Meer informatie over beschikbare entiteiten van het audittrail

* **Source de auditspoor van het Schema** staat u toe om activiteiten en recente wijzigingen te controleren die aan uw schema&#39;s binnen de instantie van de Samenstelling van Gegevens van de Adobe worden aangebracht.

  Voor gedetailleerde informatie over schema&#39;s, verwijs naar deze [ pagina ](../customer/schemas.md).

* **het controletraject van het Werkschema** staat u toe om spoor van activiteiten en recente veranderingen te houden die aan werkschema&#39;s, met inbegrip van hun huidige staten zoals worden aangebracht:

   * Starten
   * Pauzeren
   * Stoppen
   * Opnieuw starten
   * Opschonen wat overeenkomt met de handeling Historie leegmaken
   * Simuleer wat aan de actieBegin op simulatiemodus evenaart
   * Wakeup die gelijk is aan de handeling Voer taken uit die in behandeling zijn.
   * Onvoorwaardelijk stoppen

  Voor meer informatie over werkschema&#39;s, verwijs naar deze [ pagina ](../compositions/gs-compositions.md).

* **Externe Rekening** staat u toe om wijzigingen te controleren die aan externe rekeningen in de instantie van de Samenstelling van Gegevens van de Adobe worden aangebracht.

  Voor meer informatie over externe rekening, verwijs naar deze [ pagina ](../connections/federated-db.md).

+++

## Audittrail openen {#accessing-audit-trail}

Ga als volgt te werk om het exemplaar **[!UICONTROL Audit trail]** te openen:

1. Selecteer **[!UICONTROL Audit trail]** onder het menu **[!UICONTROL Federated data]** .

1. Het venster **[!UICONTROL Audit trail]** wordt geopend met de lijst met entiteiten. Adobe Campaign Web User Interface controleert het maken, bewerken en verwijderen van acties voor workflows, opties, leveringen en schema&#39;s.

   ![](assets/audit_trail.png)

1. In het venster **[!UICONTROL Audit entity]** vindt u gedetailleerdere informatie over de gekozen entiteit, zoals:

   * **[!UICONTROL Type]** : workflow, opties, leveringen of schema&#39;s.
   * **[!UICONTROL Entity]** : interne naam van uw activiteiten.
   * **[!UICONTROL Modified by]** : gebruikersnaam van de laatste persoon die deze entiteit als laatste heeft gewijzigd.
   * **[!UICONTROL Action]** : De laatste actie die op deze entiteit is uitgevoerd, is gemaakt, gewijzigd of verwijderd.
   * **[!UICONTROL Modification date]** : Datum van de laatste actie die op deze entiteit is uitgevoerd.
