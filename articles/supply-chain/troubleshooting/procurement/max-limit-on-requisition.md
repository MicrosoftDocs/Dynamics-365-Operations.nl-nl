---
title: De maximumlimiet van een inkoopovereenkomst is niet van kracht op een opdracht tot inkoop
description: De maximumlimiet van een inkoopovereenkomst is niet van kracht op een opdracht tot inkoop
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475990"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>De maximumlimiet van een inkoopovereenkomst is niet van kracht op een opdracht tot inkoop

## <a name="symptoms"></a>Symptomen

Wanneer een opdracht tot inkoop aan een inkoopovereenkomst is gekoppeld, is de maximumlimiet van de inkoopovereenkomst niet van kracht op de opdracht tot inkoop. De standaardprijsgegevens zijn juist ingevoerd, maar in de opdracht tot inkoop kan meer dan de maximumlimiet van de inkoopovereenkomst worden besteld.

## <a name="resolution"></a>Oplossing

Dit gedrag is verwacht. Omdat opdrachten niet altijd worden goedgekeurd, moet een hoeveelheid of aantal niet worden gereserveerd in de inkoopovereenkomst. Daarom voldoet u niet aan de maximumlimiet van de inkoopovereenkomst.
