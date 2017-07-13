---
title: Systeemgroeperen voor een lijst met openstaand werk
description: In dit onderwerp wordt beschreven hoe u de lijst met openstaand werk op een mobiel apparaat kunt filteren.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: dbf0e49b1156c54cd37bbbe57ca564cdbc45fb2d
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017


---

# <a name="system-grouping-on-an-open-work-list"></a>Systeemgroeperen voor een lijst met openstaand werk

[!include[banner](../includes/banner.md)]

Met behulp van een systeemgroeperingsveld kunt u een lijst met openstaand werk filteren zonder dat u het menu-item voor het mobiele apparaat moet bewerken.
Waar het wordt toegepast werkt systeemgroepering voor het filteren van een werklijst op een enkel werkkoptekstveld. U kunt systeemgroepering niet gebruiken om te filteren op velden op regelniveau.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Systeemgroepering instellen voor een lijst met openstaand werk
U stelt systeemgroepering in voor een lijst met openstaand werk met de volgende stappen.

-   Selecteer vanuit een menu-item voor een mobiel apparaat **Modus: indirect** en **Activiteitscode: Lijst met openstaand werk weergeven**. De volgende opties worden beschikbaar. Deze opties zijn vereist voor om systeemgroepering te kunnen toepassen op een lijst met openstaand werk. 

| Optie        | Omschrijving   | 
| ------------- | ------------- |
| Systeemgroepering toestaan   | Hiermee staat u systeemgroepering toe voor een geselecteerd menu-item voor een werklijst.| 
| Systeemgroeperingsveld   | Alleen beschikbaar als **Systeemwerk toestaan** is ingesteld op **Ja**. Selecteer het veld dat bepaalt hoe het verzamelen van het werk voor werknemer wordt gegroepeerd. Bijvoorbeeld, als u het veld **ShipmentId** selecteert, scant de werknemer de zendings-ID om orderverzameling werk te groeperen. Alle werk voor de zending wordt vervolgens toegewezen aan de werknemer. Dit veld vereist dat u een menuoptie maakt om bestaand werk te gebruiken dat door het systeem is gegroepeerd. Gebruik het veld **Systeemgroeperingslabel** om de werknemer te melden wat hij moet scannen. |
| Systeemgroeperingslabel   | Alleen beschikbaar als **Systeemwerk toestaan** is ingesteld op **Ja**. Voer informatie in die de werknemer vertelt wat hij moet scannen wanneer het orderverzamelingwerk wordt gegroepeerd. Als u bijvoorbeeld het veld **ShipmentId** gebruikt voor het verzamelen van werk per zending, kunt u Zendings-id in het veld invoeren. Dit veld vereist dat u een menuoptie maakt om bestaand werk te gebruiken dat door het systeem is gegroepeerd. U moet ook het veld selecteren waarop moet worden gegroepeerd in het veld **Systeemgroepering**.|

