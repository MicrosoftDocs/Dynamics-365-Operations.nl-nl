---
title: Werk de taak voor productontvangstbonnen bij om niet-bevestigde orders te bevestigen
description: Wanneer productontvangstbonnen zijn bijgewerkt, worden niet-bevestigde orders met de status Geregistreerd bevestigd. Meer informatie over de functie waarmee dit probleem wordt opgelost.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475977"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Niet-bevestigde inkooporders worden bevestigd nadat productontvangsten zijn bijgewerkt

## <a name="symptoms"></a>Symptomen

Nadat u de periodieke taak *Productontvangsten bijwerken* hebt uitgevoerd, bevestigt het systeem automatisch onbevestigde inkooporders met de voorraadtransactiestatus *Geregistreerd*.

## <a name="resolution"></a>Oplossing

Met een nieuwe functie voor verwerking van inkomende ladingen, *Meerontvangst voor ladinghoeveelheden*, wordt dit probleem opgelost. Als u deze functies wilt inschakelen, ga naar het werkgebied [Functiebeheer](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) en schakel de volgende functies in, in de volgorde waarin ze staan vermeld:

1. Voorraadtransacties van inkooporder koppelen aan lading
2. Te grote ontvangst van laadhoeveelheden

Zie [Geregistreerde ladinghoeveelheden boeken op inkooporders](/dynamics365/supply-chain/warehousing/inbound-load-handling) voor meer informatie.
