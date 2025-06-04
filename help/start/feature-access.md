---
title: Access Federal Audience Composition
description: Meer informatie over de vereiste machtigingen voor Federated Audience Composition
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 62bbed4818caf06539234f97d4c0d1cf9c9a52d1
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Access Federal Audience Composition {#feature-access}

## Toegang tot sandboxen beheren {#access-sandboxes}

Wanneer u Adobe Experience Platform Federated Audience Composition aanschaft, wordt voor elke actieve sandbox op dat moment een productprofiel gemaakt. Dit productprofiel wordt gecreeerd in Admin Console onder **Adobe Experience Platform** productkaart en volgt deze noemende overeenkomst: `ACP_FAC - <<SandboxName>> - admin.` om tot de Federatieve Samenstelling van de Publiek voor een specifieke zandbak toegang te hebben, moeten de gebruikers aan het productprofiel worden toegevoegd dat voor die zandbak wordt gecreeerd.

Als bijvoorbeeld een nieuwe sandbox met de naam &quot;fac-test&quot; wordt geactiveerd, wordt een overeenkomstig productprofiel &quot;ACP_FAC - fac-test - admin&quot; gemaakt. Gebruikers moeten aan dit productprofiel worden toegevoegd om Federated Audience Composition met deze sandbox te kunnen benaderen.

## Toegang tot Federale Audience-compositie beheren

Om tot **Federated de Samenstelling van het Publiek** toegang te hebben, moet u eerst ervoor zorgen dat u de vereiste toestemmingen toewijst om tot verschillende aspecten van de Samenstelling van het Publiek toegang te hebben Federated. Deze rollen moeten dan aan gebruikers worden toegewezen die toegang tot **Federated de Samenstelling van het Publiek** nodig hebben.

Merk op dat slechts de beheerders de capaciteit hebben om toestemmingen toe te wijzen.

1. Navigeer naar het menu **[!UICONTROL Permissions]** .

1. Selecteer in het menu **[!UICONTROL Roles]** de **[!UICONTROL Role]** die u wilt bijwerken.

   ![](assets/access_fda_1.png)

1. Selecteer **[!UICONTROL Edit]** om de machtigingen voor uw rol te wijzigen.

   ![](assets/access_fda_2.png)

1. Voeg de vereiste machtigingen voor de gebruiker toe. U kunt de volgende toestemmingen voor toegang tot de Samenstelling van de Publiek toevoegen:

   | Machtiging | Beschrijving |
   | ---------- | ----------- |
   | Federale gegevens beheren | Gebruik deze toestemming om alle aspecten van de Samenstelling van de Publiek te beheren Federated. Met deze machtiging worden Federale database beheren, Federaal schema beheren, Federaal gegevensmodel beheren en Federale composities beheren overgeërfd. |
   | Federale database beheren | Gebruik deze machtiging om uw verbindingen met gefederaliseerde databases toe te voegen, weer te geven, bij te werken en te verwijderen. |
   | Federale database weergeven | Gebruik deze toestemming om uw verbindingen aan gefederaliseerde gegevensbestanden te bekijken. |
   | Federaal schema beheren | Met deze machtiging kunt u schema&#39;s maken, weergeven, bijwerken, verwijderen en vernieuwen. |
   | Federale schemagegevens weergeven | Gebruik deze machtiging om het gegevenstabblad weer te geven in de schemasectie. |
   | Federaal schema weergeven | Gebruik deze machtiging om de schematabellen weer te geven. |
   | Federaal gegevensmodel beheren | Met deze machtiging kunt u gegevensmodellen maken, weergeven, bijwerken en verwijderen. |
   | Federaal gegevensmodel weergeven | Gebruik deze machtiging om de gegevensmodellen weer te geven. |
   | Federation Audit Trail weergeven | Gebruik deze toestemming om het controlespoor voor de Samenstelling van de Publiek te bekijken Federated. |
   | Federale composities beheren | Met deze machtiging kunt u gefedereerde composities maken, weergeven, bijwerken en verwijderen. |
   | Federale composities weergeven | Gebruik deze machtiging om gefedereerde composities weer te geven. |

   ![](assets/permissions.png)

1. Selecteer **[!UICONTROL Save]** als u de benodigde wijzigingen hebt aangebracht.

Om het even welke gebruikers die reeds aan deze rol worden toegewezen zullen hun toestemmingen automatisch bijgewerkt hebben en toegang tot de Samenstelling van het Federale publiek.

Deze rol toewijzen aan nieuwe gebruikers:

1. Navigeer naar het tabblad **[!UICONTROL Users]** in het dashboard Rol en selecteer **[!UICONTROL Add Users]** .

   ![](assets/access_fda_4.png)

1. Voer de naam of het e-mailadres van de gebruiker in of selecteer een van de beschikbare lijsten. Selecteer vervolgens **[!UICONTROL Save]** .

<!-- Alternatively, you can assign one of the pre-existing roles to the users, depending on what permissions they need. For more information on assigning pre-existing roles to a user, please read the [guide on managing users for a product profile](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

| Role name | Permissions |
| --------- | ----------- |
| FAC Data Managers | <ul><li>Manage Federated Compositions</li><li>View Federated Databases</li><li>View Federated Schemas</li><li>View Federated Schema Data</li><li>View Federated Data Models</li></ul> |
| FAC Composition Managers | <ul><li>Manage Federated Compositions</li></ul> |
| FAC Administrators | <ul><li>Manage Federated Data</li></ul> | -->

De gebruiker ontvangt vervolgens een e-mail met instructies om toegang te krijgen tot uw exemplaar. Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).
