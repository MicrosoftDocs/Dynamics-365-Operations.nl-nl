---
title: Kan voorraadreservering op een verkooporderregel niet opheffen
description: Als er open werk is voor een verkoopregel en u probeert voorraad op de regel vrij te maken, krijgt u een foutmelding. Het werk voltooien of verwijderen voor het vrij maken van de reservering.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476021"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Kan voorraadreservering op een verkooporderregel niet opheffen

## <a name="symptoms"></a>Symptomen

Als er open werk is voor een verkoopregel en u probeert voorraad op de regel vrij te maken, krijgt u de volgende foutmelding:

> Reserveringen kunnen niet worden verwijderd omdat er werk is gemaakt dat afhankelijk is van de reserveringen.

## <a name="resolution"></a>Oplossing

Controleer of er openstaand werk van een verpakkingsgroep bestaat om het artikel van een inpakstation naar een andere locatie te brengen (bijvoorbeeld *Laaddeur*). Bekijk de records in het **Historielogboek van werkaanmaak** en de pagina's **Werkgegevens** om te bepalen wat het is dat fysiek de voorraad reserveert en voer vervolgens de voltooiing of verwijdering van het werk uit om de reservering vrij te maken.
