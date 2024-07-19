---
audience: end-user
title: Soorten publiek naar compositie van Adobe Federated Audience verzenden
description: Leer hoe u Adobe Experience Platform-publiek naar Federated Audience Composition verzendt
badge: label="Beperkte beschikbaarheid" type="Informative"
source-git-commit: 1e400d98040cdbcc6f13f84faa00e8efa6cfbd4a
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Adobe Experience Platform naar Adobe Federale Audience Composition verzenden {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Een doel maken"
>abstract="Ga de montages in om met het nieuwe Federatieve Gegevensbestand te verbinden. Gebruik de knop **[!UICONTROL Connect to destination]** om uw configuratie te valideren."

Adobe Experience Platform staat u toe om over publiek van het Portaal van het Publiek naar Adobe Federated Audience Composition te verzenden. Op deze manier kunt u bestaande doelgroepen gebruiken voor composities en deze combineren met gegevens uit uw externe databases om nieuwe doelgroepen te maken of bestaande doelgroepen bij te werken.

Hiertoe moet u een nieuwe verbinding in Adobe Experience Platform instellen met de bestemming Adobe Federated Audience Composition. U kunt een planner gebruiken om een bepaald publiek bij regelmatige frequenties te verzenden, kies welke gebieden met het publiek, zoals IDs te verzenden om de gegevens te verzoenen. Als u het beheer- en privacybeleid hebt toegepast op uw publiek, worden deze gegevens bewaard en teruggestuurd naar de portal voor het publiek nadat het publiek is bijgewerkt.

De belangrijkste stappen om Adobe Experience Platform-publiek naar de Adobe Federated Audience Composition te sturen zijn:

1. Open de catalogus van de Doelen van Adobe Experience Platform en selecteer de Federatieve bestemming van de Samenstelling van het Publiek.

   Selecteer **[!UICONTROL Configure new destination]** in het rechterdeelvenster.

   ![](assets/destination-new.png)

1. Geef een naam op voor de nieuwe verbinding en kies de **[!UICONTROL Connection type]** die u wilt gebruiken en de **[!UICONTROL Federated database]** waarmee u verbinding wilt maken en klik op **[!UICONTROL Next]** .

   ![](assets/destination-configure.png)

   In de sectie **[!UICONTROL Alerts]** kunt u waarschuwingen inschakelen voor het ontvangen van meldingen over de status van de gegevensstroom naar uw bestemming. Voor meer informatie over alarm, zie de gids bij [ het intekenen aan bestemmingsalarm gebruikend UI ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts).

1. In de stap **[!UICONTROL Governance policy & enforcement actions]** kunt u het beleid voor gegevensbeheer definiëren en ervoor zorgen dat de gebruikte gegevens voldoen wanneer een publiek wordt verstuurd en geactiveerd.

   Wanneer u klaar bent met het selecteren van de gewenste marketingacties voor het doel, klikt u op **[!UICONTROL Create]** .

1. De nieuwe verbinding met het doel wordt gemaakt. U kunt het publiek nu activeren om naar de bestemming te gaan. U doet dit door het in de lijst te selecteren en op **[!UICONTROL Next]** te klikken

   ![](assets/destination-activate.png)

1. Selecteer het gewenste publiek dat u wilt verzenden en klik op **[!UICONTROL Next]** .

1. Configureer de bestandsnaam en een exportschema voor de geselecteerde doelgroep(en).

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >De gedetailleerde informatie over hoe te om programma en filenames te vormen is beschikbaar in de documentatie van Adobe Experience Platform:
   >* [ de publieksuitvoer van het Programma ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling)
   >* [ vorm dossiernamen ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names)

1. Selecteer in de stap **[!UICONTROL Mapping]** welke kenmerk- en identiteitsvelden u wilt exporteren voor uw publiek of doelgroepen. Voor meer informatie, bekijk de [ toewijzingsstap ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping) in de documentatie van Adobe Experience Platform.

   ![](assets/destination-attributes.png)

1. Controleer de doelconfiguratie en de publieksinstellingen en klik vervolgens op **[!UICONTROL Finish]** .

   ![](assets/destination-review.png)

Het geselecteerde publiek wordt nu geactiveerd voor de nieuwe verbinding. U kunt meer soorten publiek toevoegen om met deze verbinding te verzenden door terug naar de **[!UICONTROL Activate audiences]** pagina te navigeren. U kunt soorten publiek niet verwijderen als ze eenmaal zijn geactiveerd.
