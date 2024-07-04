---
audience: end-user
title: De activiteit AND-join gebruiken
description: Leer hoe te om de activiteit EN te gebruiken toetreedt
source-git-commit: 44be467650e2329a1fce6c5adb6d266d94efd1e2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join-activiteit"
>abstract="De **En-join** de activiteit staat u toe om veelvoudige uitvoertakken van een samenstelling te synchroniseren. De regeling wordt in werking gesteld zodra alle voorgaande activiteiten zijn beëindigd. Dit staat u toe om ervoor te zorgen dat bepaalde activiteiten alvorens de samenstelling te blijven uitvoeren worden gebeëindigd."

De **AND-join** de activiteit staat u toe om veelvoudige uitvoertakken van een samenstelling te synchroniseren.

Deze activiteit brengt slechts zijn uitgaande overgang teweeg zodra alle binnenkomende overgangen worden geactiveerd, met andere woorden, zodra alle voorafgaande activiteiten zijn geëindigd. Hierdoor kunt u ervoor zorgen dat bepaalde activiteiten zijn voltooid voordat u doorgaat met het uitvoeren van de compositie.

## Vorm en verbind activiteit {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Vorm EN-verbind activiteit"
>abstract="Selecteer de activiteiten waaraan u wilt deelnemen. In de **Primaire set** keuzelijst, kies welke binnenkomende overgangspopulatie u wilt houden."

Voer de volgende stappen uit om de **AND-join** activiteit:

1. Voeg meerdere activiteiten toe om minstens twee verschillende uitvoeringstakken te vormen.
1. Een **AND-join** activiteiten aan een van de bijkantoren.

   ![](../assets/and-join.png)

1. In de **Samenvoegopties** alle vorige activiteiten die u wilt synchroniseren, controleren.
1. In de **Primaire set** keuzelijst, kies welke binnenkomende overgangspopulatie u wilt houden. De uitgaande overgang kan slechts één van de binnenkomende overgangspopulaties bevatten. Als de activiteit niet wordt gevormd, zal de uitgaande overgang willekeurig één van de binnenkomende populaties selecteren.
