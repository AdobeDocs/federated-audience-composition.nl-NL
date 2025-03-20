---
audience: end-user
title: Audit trail
description: Leer hoe acties en gebeurtenissen zijn geregistreerd en toegankelijk in het audittrail
exl-id: 97142f54-53ce-4c2a-9d89-fdcb2a47b159
source-git-commit: 154edf65bc460c6c98ae16f9b799ec38939fb5fd
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 3%

---

# Audit trail {#audit-trail}

>[!CONTEXTUALHELP]
>id="dc_audit_trail"
>title="Audit trail"
>abstract="De audittrailcapaciteit verstrekt een gedetailleerd en chronologisch verslag van alle acties en gebeurtenissen die aan uw milieu van de Samenstelling van het Publiek van Adobe Experience Platform Federated in real time zijn gemaakt."

De functie **[!UICONTROL Audit trail]** neemt voortdurend een gedetailleerd logboek op van acties en gebeurtenissen die in real-time plaatsvinden in de instantie van de Adobe Federated Composition. Het biedt een geschikte methode aan om tot een chronologisch verslag van gegevens toegang te hebben, die vragen zoals: de status van werkschema&#39;s, de recentste individuen richten om hen te wijzigen, of de activiteiten richten die door gebruikers binnen de instantie worden uitgevoerd.

+++ Meer informatie over beschikbare entiteiten van het audittrail

* **het de controlespoor van het Schema van Source** staat u toe om activiteiten en recente wijzigingen te controleren die aan uw schema&#39;s binnen de Adobe Federated instantie van de Samenstelling van het Publiek worden aangebracht.

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

* **Externe Rekening** staat u toe om wijzigingen te controleren die aan externe rekeningen in de instantie van de Samenstelling van het publiek van Adobe worden aangebracht.

  Voor meer informatie over externe rekening, verwijs naar deze [ pagina ](../connections/federated-db.md).

+++

## Audittrail openen {#accessing-audit-trail}

Ga als volgt te werk om het exemplaar **[!UICONTROL Audit trail]** te openen:

1. Selecteer **[!UICONTROL Audit trail]** onder het menu **[!UICONTROL Federated data]** .

1. Het venster **[!UICONTROL Audit trail]** wordt geopend met de lijst met entiteiten. De federated Audience Composition controleert creeert, uitgeeft en schrapt acties voor werkschema&#39;s, opties, leveringen en schema&#39;s.

   ![](assets/audit_trail.png)

1. In het venster **[!UICONTROL Audit entity]** vindt u gedetailleerdere informatie over de gekozen entiteit, zoals:

   * **[!UICONTROL Type]** : workflow, opties, leveringen of schema&#39;s.
   * **[!UICONTROL Entity]** : interne naam van uw activiteiten.
   * **[!UICONTROL Modified by]** : gebruikersnaam van de laatste persoon die deze entiteit als laatste heeft gewijzigd.
   * **[!UICONTROL Action]** : De laatste actie die op deze entiteit is uitgevoerd, is gemaakt, gewijzigd of verwijderd.
   * **[!UICONTROL Modification date]** : Datum van de laatste actie die op deze entiteit is uitgevoerd.
