---
title: Afgerond bedrag voor afschrijvingsberekeningen
description: In dit artikel wordt het veld Afschrijving afronden besproken uit de pagina's Instellingen voor boeken.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ae5c24633a9ce4ce43e213581eb64c8548eecf5d
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a>Afgerond bedrag voor afschrijvingsberekeningen

[!include[banner](../includes/banner.md)]


In dit artikel wordt het veld Afschrijving afronden besproken uit de pagina's Instellingen voor boeken.

Afgeronde afschrijvingsbedragen worden ingesteld voor elk boek. Afgeronde afschrijvingsbedragen worden gebruikt in het afschrijvingsprofiel voor vaste activa dat de toekomstige afschrijving en waarde van het vaste activum weergeeft, en ook in afschrijvingsvoorstellen. Voer het laagste afschrijvingsbedrag in dat is toegestaan voor het boek. 

Ongeacht de afronding die is ingesteld, wordt het afschrijvingsbedrag in de laatste afschrijvingsperiode niet afgerond. Aan het einde van de laatste afschrijvingsperiode moet de waarde van het vaste activum 0 (nul) of de restwaarde zijn als de restwaarde wordt gebruikt.

### <a name="example"></a>Voorbeeld

Afschrijving zonder afronding wordt berekend als 2444,44. Zoals te zien in de volgende tabel, variëren de bedragen die worden voorgesteld, afhankelijk van hoe de afronding is ingesteld.

| Afrondingsmethode | Afschrijvingsbedrag |
|-----------------|---------------------|
| Afronding van 0,1    | 2444,40            |
| Afronding van 1,00   | 2444,00            |
| Afronding van 10,00  | 2440,00            |
| Afronding van 100,00 | 2400,00            |






