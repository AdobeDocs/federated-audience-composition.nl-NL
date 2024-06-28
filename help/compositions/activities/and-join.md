---
audience: end-user
title: De activiteit AND-join gebruiken
description: Leer hoe te om de activiteit EN te gebruiken toetreedt
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="AND-join-activiteit"
>abstract="De **En-join** de activiteit staat u toe om veelvoudige uitvoertakken van een samenstelling te synchroniseren. De regeling wordt in werking gesteld zodra alle voorgaande activiteiten zijn beëindigd. Dit staat u toe om ervoor te zorgen dat bepaalde activiteiten alvorens de samenstelling te blijven uitvoeren worden gebeëindigd."

De **En-join** de activiteit staat u toe om veelvoudige uitvoertakken van een samenstelling te synchroniseren.

Deze activiteit brengt slechts zijn uitgaande overgang teweeg zodra alle binnenkomende overgangen worden geactiveerd, met andere woorden, zodra alle voorafgaande activiteiten zijn geëindigd. Hierdoor kunt u ervoor zorgen dat bepaalde activiteiten zijn voltooid voordat u doorgaat met het uitvoeren van de compositie.

## Vorm en verbind activiteit {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Vorm EN-verbind activiteit"
>abstract="Selecteer de activiteiten waaraan u wilt deelnemen. In de **Primaire set** keuzelijst, kies welke binnenkomende overgangspopulatie u wilt houden."

Voer de volgende stappen uit om de **AND-join** activiteit:

1. Voeg veelvoudige activiteiten zoals kanaalactiviteiten toe om minstens twee verschillende uitvoertakken te vormen.
1. Een **AND-join** activiteiten aan een van de bijkantoren.
1. In de **Samenvoegopties** , controleert u alle vorige activiteiten waaraan u wilt deelnemen.
1. In de **Primaire set** keuzelijst, kies welke binnenkomende overgangspopulatie u wilt houden. De uitgaande overgang kan slechts één van de binnenkomende overgangspopulaties bevatten.

