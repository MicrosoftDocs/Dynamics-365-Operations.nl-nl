---
title: Dimensielocatie kan niet leeg zijn als serienummer is ingesteld
description: Als u deze fout ontvangt bij het bevestigen van een zending nadat u een transferorder hebt aangemaakt voor een serieartikel, is het veld Standaardlocatie voor ontvangst leeg.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476048"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Fout bij het bevestigen van de zending nadat er een transferorder voor een serieartikel is aangemaakt

## <a name="symptoms"></a>Symptomen

Het volgende foutbericht wordt weergegeven als u een transferorder maakt voor een serieartikel met behulp van een magazijn dat is ingeschakeld voor geavanceerd magazijnbeheer (WMS) en vervolgens, als het werk is voltooid, probeert de zending te bevestigen.

> Dimensielocatie kan niet leeg worden gelaten als serienummer dimensie is ingesteld.

## <a name="cause"></a>Oorzaak

Dit doet zich voor omdat het veld **Standaardlocatie voor ontvangst** leeg wordt gelaten voor een transitmagazijn van het 'van'-magazijn.

## <a name="resolution"></a>Oplossing

U kunt dit probleem oplossen door een standaardlocatie voor ontvangst op te geven in het transitmagazijn. Zorg ervoor dat deze locatie een nummerplaatbeheerde locatie is.
