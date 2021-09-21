---
title: Voorraadeigenaar is niet toegestaan bij het verwerken van verplaatsingen
description: Mogelijk wordt de fout 'De voorraadeigenaar %1 is niet toegestaan' weergegeven. Processen van magazijnbeheer ondersteunen alleen voorraad die eigendom is van de rechtspersoon.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475988"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Voorraadeigenaar is niet toegestaan bij het verwerken van verplaatsingen in de magazijn-app

## <a name="symptoms"></a>Symptomen

Wanneer u verplaatsingen verwerkt in de mobiele app Warehouse Management, wordt mogelijk het volgende foutbericht weergegeven:

> De voorraadeigenaar %1 is niet toegestaan in dit proces.

## <a name="cause"></a>Oorzaak

Deze fout doet zich voor omdat de traceringsdimensie **Eigenaar** ontbreekt wanneer de mobiele app Warehouse Management wordt gebruikt om verplaatsingen door te voeren. Een normaal voorraadoverboekingjournaal van de Supply Chain Management-client lijkt te werken zoals bedoeld en kan alleen worden geboekt als de dimensie **Eigenaar** is ingevuld.

## <a name="resolution"></a>Oplossing

Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. Momenteel ondersteunt magazijnbeheer alleen voorraad die eigendom is van de rechtspersoon.
