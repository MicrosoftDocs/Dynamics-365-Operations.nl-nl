---
title: Systeemgroeperen voor een lijst met openstaand werk
description: In dit onderwerp wordt beschreven hoe u de lijst met openstaand werk op een mobiel apparaat kunt filteren.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05b697cce8ecb9ece282fc659ab4d97c4b747c5e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425307"
---
# <a name="system-grouping-on-an-open-work-list"></a>Systeemgroeperen voor een lijst met openstaand werk

[!include [banner](../includes/banner.md)]

Met behulp van een systeemgroeperingsveld kunt u een lijst met openstaand werk filteren zonder dat u het menu-item voor het mobiele apparaat moet bewerken.
Waar het wordt toegepast werkt systeemgroepering voor het filteren van een werklijst op een enkel werkkoptekstveld. U kunt systeemgroepering niet gebruiken om te filteren op velden op regelniveau.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Systeemgroepering instellen voor een lijst met openstaand werk
U stelt systeemgroepering in voor een lijst met openstaand werk met de volgende stappen.

-   Selecteer vanuit een menu-item voor een mobiel apparaat **Modus: indirect** en **Activiteitscode: Lijst met openstaand werk weergeven**. De volgende opties worden beschikbaar. Deze opties zijn vereist voor om systeemgroepering te kunnen toepassen op een lijst met openstaand werk. 

|        Optie         |                                                                                                                                                                                                                                                                         Omschrijving                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Systeemgroepering toestaan |                                                                                                                                                                                                                                                 Hiermee staat u systeemgroepering toe voor een geselecteerd menu-item voor een werklijst.                                                                                                                                                                                                                                                  |
| Systeemgroeperingsveld | Alleen beschikbaar als <strong>Systeemwerk toestaan</strong> is ingesteld op <strong>Ja</strong>. Selecteer het veld dat bepaalt hoe het verzamelen van het werk voor werknemer wordt gegroepeerd. Bijvoorbeeld, als u het veld <strong>ShipmentId</strong> selecteert, scant de werknemer de zendings-ID om orderverzameling werk te groeperen. Alle werk voor de zending wordt vervolgens toegewezen aan de werknemer. Dit veld vereist dat u een menuoptie maakt om bestaand werk te gebruiken dat door het systeem is gegroepeerd. Gebruik het veld <strong>Systeemgroeperingslabel</strong> om de werknemer te melden wat hij moet scannen. |
| Systeemgroeperingslabel |                       Alleen beschikbaar als <strong>Systeemwerk toestaan</strong> is ingesteld op <strong>Ja</strong>. Voer informatie in die de werknemer vertelt wat hij moet scannen wanneer het orderverzamelingwerk wordt gegroepeerd. Als u bijvoorbeeld het veld <strong>ShipmentId</strong> gebruikt voor het verzamelen van werk per zending, kunt u Zendings-id in het veld invoeren. Dit veld vereist dat u een menuoptie maakt om bestaand werk te gebruiken dat door het systeem is gegroepeerd. U moet ook het veld selecteren waarop moet worden gegroepeerd in het veld <strong>Systeemgroepering</strong>.                       |

