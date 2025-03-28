---
title: Access Federal Audience Composition
description: Meer informatie over de vereiste machtigingen voor Federated Audience Composition
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 0f4bba9c749a6548da07d78136e914cc53314684
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Access Federal Audience Composition {#feature-access}

## Toegang tot sandboxen beheren {#access-sandboxes}

Wanneer u Adobe Experience Platform Federated Audience Composition aanschaft, wordt voor elke actieve sandbox op dat moment een productprofiel gemaakt. Dit productprofiel wordt gecreeerd in Admin Console onder **Adobe Experience Platform** productkaart en volgt deze noemende overeenkomst: `ACP_FAC - <<SandboxName>> - admin.` om tot de Federatieve Samenstelling van de Publiek voor een specifieke zandbak toegang te hebben, moeten de gebruikers aan het productprofiel worden toegevoegd dat voor die zandbak wordt gecreeerd.

Als bijvoorbeeld een nieuwe sandbox met de naam &quot;fac-test&quot; wordt geactiveerd, wordt een overeenkomstig productprofiel &quot;ACP_FAC - fac-test - admin&quot; gemaakt. Gebruikers moeten aan dit productprofiel worden toegevoegd om Federated Audience Composition met deze sandbox te kunnen benaderen.

## Toegang tot Federale Audience-compositie beheren

Om tot **Federated de Samenstelling van het Publiek** toegang te hebben, moet u eerst ervoor zorgen dat **Federatieve Gegevens** toestemming beheert aan de aangewezen rollen wordt toegewezen. Deze rollen moeten dan aan gebruikers worden toegewezen die toegang tot **Federated de Samenstelling van het Publiek** nodig hebben.

Merk op dat slechts de beheerders de capaciteit hebben om toestemmingen toe te wijzen.

1. Navigeer naar het menu **[!UICONTROL Permissions]** .

1. Selecteer in het menu **[!UICONTROL Roles]** de **[!UICONTROL Role]** die u wilt bijwerken.

   ![](assets/access_fda_1.png)

1. Klik op **[!UICONTROL Edit]** om de machtigingen voor uw rol te wijzigen.

   ![](assets/access_fda_2.png)

1. Voeg het **Verdeelde 1} middel van Gegevens {toe, dan uitgezocht **[!UICONTROL Manage Federated Data]**van het drop-down menu.**

   ![](assets/access_fda_3.png)

1. Klik op **[!UICONTROL Save]** als u de benodigde wijzigingen hebt aangebracht.

Om het even welke gebruikers die reeds aan deze rol worden toegewezen zullen hun toestemmingen automatisch bijgewerkt hebben en toegang tot de Samenstelling van het Federale publiek.

Deze rol toewijzen aan nieuwe gebruikers:

1. Navigeer naar het tabblad **[!UICONTROL Users]** in het dashboard Rol en klik op **[!UICONTROL Add Users]** .

   ![](assets/access_fda_4.png)

1. Voer de naam of het e-mailadres van de gebruiker in of selecteer een van de beschikbare lijsten. Klik op **[!UICONTROL Save]** als u klaar bent.

De gebruiker ontvangt vervolgens een e-mail met instructies om toegang te krijgen tot uw exemplaar. Als de gebruiker niet eerder werd gecreeerd, verwijs naar [ deze documentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users).
