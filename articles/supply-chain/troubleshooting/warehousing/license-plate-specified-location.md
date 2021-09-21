---
title: Nummerplaat moet zijn gespecificeerd voor deze locatie
description: Als u deze fout ontvangt nadat u een transferorder hebt gemaakt voor een WMS-magazijn, is de standaardontvangstlocatie leeg voor een transitmagazijn.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475979"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Fout bij specificatie van nummerplaat bij bevestiging van zending voor transferorder

## <a name="symptoms"></a>Symptomen

Als u een transferorder maakt met behulp van een magazijn dat is ingeschakeld voor geavanceerd magazijnbeheer (WMS) en vervolgens probeert u de zending te bevestigen nadat het werk is voltooid, wordt mogelijk het volgende foutbericht weergegeven:

> Nummerplaat moet zijn gespecificeerd voor deze locatie.

## <a name="cause"></a>Oorzaak

Dit doet zich voor omdat het veld **Standaardlocatie voor ontvangst** leeg wordt gelaten voor een transitmagazijn van het 'van'-magazijn.

## <a name="resolution"></a>Oplossing

U kunt dit probleem oplossen door een standaardlocatie voor ontvangst op te geven in het transitmagazijn. Zorg ervoor dat deze locatie een nummerplaatbeheerde locatie is.
