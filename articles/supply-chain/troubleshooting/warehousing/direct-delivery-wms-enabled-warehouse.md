---
title: Directe levering kan niet worden verwerkt voor magazijn met WMS ingeschakeld
description: Als WMS voor het magazijn is ingeschakeld, wordt directe levering niet ondersteund. Om directe levering te kunnen gebruiken, moet u dus een niet-WMS-artikel en -magazijn selecteren.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476064"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Directe levering kan niet worden verwerkt voor magazijn met WMS ingeschakeld

## <a name="symptoms"></a>Symptomen

Als een artikel wordt toegevoegd aan een verkoopregel voor directe levering vanuit een magazijn waarvoor magazijnbeheer (WMS) is ingeschakeld, wordt het volgende foutbericht weergegeven wanneer de verkoopregel wordt bijgewerkt:

> Directe levering verwerken kan niet voor magazijn 1% omdat magazijnbeheer is ingeschakeld. Geef een ander magazijn op waarvoor magazijnbeheer niet is ingeschakeld.

## <a name="resolution"></a>Oplossing

Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. In WMS wordt rechtstreekse levering momenteel niet ondersteund. Als u rechtstreekse levering wilt gebruiken, moet u dus een niet-WMS artikel en -magazijn selecteren.
