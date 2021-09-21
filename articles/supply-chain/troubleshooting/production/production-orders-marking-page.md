---
title: Productieorders worden niet weergegeven op de pagina Markering
description: Sommige productieorders worden niet weergegeven op de pagina Markering. In dit onderwerp krijgt u informatie over de drie productconfiguraties die niet beschikbaar zijn voor markering.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 87507e91d3feb2557e7ba771b8e34ff7ca105749
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475958"
---
# <a name="production-orders-arent-shown-on-the-marking-page"></a>Productieorders worden niet weergegeven op de pagina Markering

## <a name="symptoms"></a>Symptomen

Wanneer u werkt met afzonderlijke fabricage, worden sommige productieorders niet weergegeven op de pagina **Markering**.

## <a name="resolution"></a>Oplossing

Producten met de volgende configuraties zijn niet beschikbaar voor markering. Deze worden daarom niet weergegeven op de pagina **Markering**:

- De producten worden gedefinieerd als producten van het type *catch weight*.
- De producten zijn ingeschakeld voor de geavanceerde magazijnprocessen.
- Ze zijn geconfigureerd om te worden beheerd door het principe *Standaardkosten*.
