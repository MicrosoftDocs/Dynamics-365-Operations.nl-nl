---
title: Het gewicht van de lading kan alleen positieve getallen bevatten.
description: Wanneer u werk tussen locaties verwerkt, wordt er mogelijk een fout weergegeven met betrekking tot het gewicht van de lading en het annuleren van de update. Volg deze stappen om het probleem op te lossen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476000"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Fout met het gewicht van de lading en update geannuleerd tijdens de verwerking van werk tussen locaties

## <a name="symptoms"></a>Symptomen

Als er openstaand werk is wanneer u werk verwerkt vanuit verpakkingslocaties naar faseringslocaties of vanuit faseringslocaties naar doklocaties, wordt mogelijk het volgende foutbericht weergegeven:

> Het veld Gewicht lading (=-%1) kan alleen positieve getallen bevatten. Update is geannuleerd.

## <a name="resolution"></a>Oplossing

Als u dit probleem wilt verhelpen, gaat u naar **Systeembeheer \> Periodieke taken \> Database \> Consistentiecontrole** en voert u het proces uit voor **Consistentiecontrole capaciteit magazijn**.
