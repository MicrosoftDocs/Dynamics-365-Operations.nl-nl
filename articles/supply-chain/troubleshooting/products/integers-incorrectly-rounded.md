---
title: Incorrect afgeronde gehele getallen in berekeningen van productconfiguratiemodellen
description: Er wordt niet altijd correct afgerond op gehele getallen wanneer de productconfiguratiemodellen worden berekend. Los het probleem op met een extra decimaal kenmerk en een berekening.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476031"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Gehele getallen die incorrect worden afgerond wanneer de productconfiguratiemodellen worden berekend

## <a name="symptoms"></a>Symptomen

Dit probleem kan optreden wanneer u de volgende reeks acties uitvoert:

1. Stel deze kenmerken in voor een productieconfiguratiemodel:

    - Invoer (geheel getal)
    - Percentage (decimaal)
    - Resultaat (geheel getal)

2. Maak een berekening die de volgende expressie bevat:

    *Resultaat* = *invoer* × *procent* ÷ 100

In dit geval wordt het resultaat van het gehele getal niet altijd juist afgerond. Als de invoer bijvoorbeeld 1000 is en het percentage 2,40, verwacht u dat het resultaat van het geheel getal 24 is, omdat 2,40 procent van 1000 24 (of 24,00 in decimale notatie) is. In plaats daarvan wordt het resultaat weergegeven als 23. Wanneer het percentage echter 2,39 is, wordt de berekening afgerond naar 24 in plaats van 23. Wanneer het percentage 2,50 is, wordt de berekening afgerond naar 25, zoals verwacht.

## <a name="cause"></a>Oorzaak

Dit probleem doet zich voor vanwege de manier waarop getallen door Microsoft Solver Foundation intern worden aangeduid met breuken. Voor het bovenstaande voorbeeld wordt het resultaat van de berekening waarbij het percentage 2,40 is, weergegeven als 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375. Wanneer .NET deze waarde als een geheel getal converteert, wordt 23 geretourneerd.

## <a name="resolution"></a>Oplossing

Dit gedrag wordt niet gewijzigd, omdat andere scenario's hiervan afhankelijk zijn. Voor het voorgaande voorbeeld kunt u het probleem oplossen door een extra, decimaal kenmerk en berekeningen te introduceren.

Stel bijvoorbeeld de volgende kenmerken in voor een productieconfiguratiemodel:

- Invoer (geheel getal)
- Percentage (decimaal)
- ResultDecimal (decimaal)
- ResultInteger (geheel getal)

Vervolgens kunt u de volgende berekeningen toevoegen:

- *ResultDecimal* = *invoer* × *procent* ÷ 100
- *ResultInteger* = *ResultDecimal*
