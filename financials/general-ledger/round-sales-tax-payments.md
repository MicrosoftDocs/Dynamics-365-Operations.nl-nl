---
title: Btw-betalingen en afrondingsregels
description: In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 8f28ab4ea0fed975edbed60ddf5630d2d26ba0bc
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-payments-and-rounding-rules"></a>Btw-betalingen en afrondingsregels

In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.

Periodiek moet btw worden aangegeven en betaald aan de belastingdienst. Dit kunt doen met het vereffenen en boeken van btw-proces in de btw-pagina. Btw voor een periode worden vereffend met de btw-rekeningen en het saldo van de btw wordt geboekt naar de btw-vereffeningsrekening. Het btw-saldo, dat op de rekening Btw-vereffening wordt geboekt, kan worden afgerond zoals vereist wordt door de belastingdienst door een afrondingregel in te stellen op de pagina Btw. 

Het afrondingsverschil wordt geboekt naar de rekening Btw-afronding die is geselecteerd in het veld Rekeningen voor automatische transacties in het Grootboek.

Het onderstaande voorbeeld illustreert hoe de afrondingregel op Btw-dienst werkt.

### <a name="example"></a>    Voorbeeld:

De totale btw voor een periode toont een creditsaldo van -98.765,43. De rechtspersoon inde meer btw dan dat betaald werd. Daarom is de rechtspersoon geld verschuldigd aan de belastingsdienst. 

De rechtspersoon wil een afrondingsmethode gebruiken waarmee het saldo wordt afgerond naar de dichtstbijzijnde 1,00. De gebruiker die verantwoordelijk is voor de btw-boekhouding voert de volgende stappen uit.

1.  Klik op btw &gt;indirecte belastingen &gt;btw &gt;btw-dienst
2.  Selecteer op het sneltabblad Algemeen in het veld Afrondingstype de optie Normaal.
3.  Typ 1,00 in het veld Afronden.
4.  Wanneer het tijd is om de btw te betalen aan de belastingdienst, opent u de pagina Btw vereffenen en boeken. (Klik op btw &gt;aangiften &gt;btw &gt;vereffenen en boeken van btw.)
5.  Op de btw-vereffeningsrekening is het bedrag van uw btw-belastingschuld van 98.765,43 afgerond naar 98.765.

In de volgende tabel ziet u hoe een bedrag van 98.765,43 wordt afgerond met behulp van elke afrondingsmethode die beschikbaar is in het veld Afrondingstype op de pagina Btw-dienst.

| Optie Afrondingstype                | Afrondingswaarde = 0,01 | Afrondingswaarde = 0,10 | Afrondingswaarde = 1,00 | Afrondingswaarde = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Normaal                              | 98.765,43              | 98.765,40              | 98.765,00              | 98.800,00                |
| Naar beneden afronden                            | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Naar boven afronden                         | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |
| Eigen voordeel, voor een creditsaldo | 98.765,43              | 98.765,40              | 98.765,00              | 98.700,00                |
| Eigen voordeel, voor een debitsaldo  | 98.765,43              | 98.765,50              | 98.766,00              | 98.800,00                |

> [!NOTE]                                                                                  
> Als u Eigen voordeel selecteert, is de afronding altijd in het voordeel van de rechtspersoon. 

Zie voor meer informatie [btw-overzicht](indirect-taxes-overview.md). 


