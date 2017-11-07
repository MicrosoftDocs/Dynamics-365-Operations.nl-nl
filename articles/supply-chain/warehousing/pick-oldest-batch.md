---
title: Oudste batch verzamelen op een mobiel apparaat
description: In dit onderwerp wordt beschreven hoe u de opties voor het verzamelen van de oudste batch kunt instellen en toepassen op een mobiel apparaat.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 25056886b1a18dbaef12c8732a1fd0bd92a6d04b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>Oudste batch verzamelen op een mobiel apparaat

[!include[banner](../includes/banner.md)]

U hebt toegang tot de configuratie **Oudste batch verzamelen** via het menu van een mobiel apparaat en hiermee kunt u magazijnmedewerkers dwingen of waarschuwen dat zij de oudste batch picken op hun huidige locatie.  

## <a name="where-it-applies"></a>Waar van toepassing
Oudste batch verzamelen wordt geconfigureerd in menu-items van mobiel apparaten en beïnvloedt het verzamelen voor de onderste artikelen in de batch.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>De configuratie voor Oudste batch verzamelen instellen 
Voor artikelen die zijn ingesteld op gebruik van bestaand werk kan **Oudste batch verzamelen** worden ingesteld op **Geen**, **Waarschuwen** of **Forceren** in het menu van een mobiel apparaat.

**Geen**: Werknemers ontvangen geen berichten en ze mogen elke batch in hun locatie verzamelen.

**Waarschuwing** en **Forceren**: Een lijst van de batch(es) met de oudste vervaldatum verschijnt boven het batchbesturingselement wanneer de werknemer een batch selecteert. Als de locatie wordt aangestuurd via nummerplaten, wordt een lijst met nummerplaten die de oudste batch bevatten weergegeven boven het besturingselement nummerplaat. 
-   **Waarschuwing**: Als een werknemer een nummerplaat of een batch kiest die niet in de weergegeven lijst staat, wordt het besturingselement blanco gemaakt en een waarschuwing getoond dat er een oudere batch is die moet worden geselecteerd. Om te kunnen doorgaan met het werk, mag de werknemer dezelfde nummerplaat of batch opnieuw selecteren.  
-   **Forceren**: Werknemers blijven het bericht ontvangen dat er een oudere batch is, die moet worden verzameld.

