---
title: Hoeveelheid is niet geldig bij het registreren van inkomende orders
description: Als de hoeveelheid die is toegewezen voor een nummerplaat, groter is dan de hoeveelheid die nog moet worden ontvangen, wordt het foutbericht 'De hoeveelheid is niet geldig' weergegeven.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476052"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Nummerplaathoeveelheid is niet geldig bij het registreren van inkomende orders

## <a name="symptoms"></a>Symptomen

Wanneer u inkomende orders registreert, wordt mogelijk het volgende foutbericht weergegeven:

> De hoeveelheid is niet geldig.

Als het veld **Groeperingsbeleid nummerplaten** is ingesteld op *Door gebruiker gedefinieerd* voor een menu-item voor mobiele apparaten dat wordt gebruikt om inkomende orders te registreren, ontvangt u dit foutbericht en kunt u de registratie niet voltooien.

## <a name="cause"></a>Oorzaak

Wanneer *Door gebruiker gedefinieerd* wordt gebruikt als groeperingsbeleid voor kentekenplaten, splitst het systeem de inkomende voorraad op in afzonderlijke nummerplaten, zoals aangegeven door de eenheidsvolgordegroep. Als batch- of serienummers worden gebruikt om het artikel bij te houden dat wordt ontvangen, moeten de hoeveelheden van elke batch of serie worden opgegeven per nummerplaat die is geregistreerd. Als de hoeveelheid die is opgegeven voor een nummerplaat groter is dan de hoeveelheid die nog moet worden ontvangen voor de huidige dimensies, wordt dit foutbericht weergegeven.

## <a name="resolution"></a>Oplossing

Wanneer u een artikel registreert met behulp van een menu-item voor mobiele apparaten waarbij het veld **Groeperingsbeleid nummerplaten** is ingesteld op *Door gebruiker gedefinieerd*, moet u mogelijk nummerplaatnummers, batchnummers of serienummers bevestigen of invoeren.

Op de bevestigingspagina van de nummerplaat toont het systeem de hoeveelheid die is toegewezen voor de huidige nummerplaat. Op de bevestigingspagina's voor batch- of serienummers toont het systeem de hoeveelheid die nog moet worden ontvangen voor de huidige nummerplaat. Het bevat ook een veld waarin u de hoeveelheid kunt invoeren die u wilt registreren voor die combinatie van nummerplaat en batch- of serienummer. Zorg er in dat geval voor dat de hoeveelheid die wordt geregistreerd voor de nummerplaat, niet groter is dan de hoeveelheid die nog moet worden ontvangen.

Als er te veel nummerplaten worden gegenereerd bij inkomende orderregistratie, kan de waarde van het veld **Groeperingsbeleid nummerplaten** worden gewijzigd in *Nummerplaatgroepering*, kan een nieuwe eenheidsvolgordegroep aan het artikel worden toegewezen of kan de optie **Nummerplaatgroepering** worden gedeactiveerd voor de eenheidsvolgordegroep.
