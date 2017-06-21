---
title: Btw-betalingen en afrondingsregels
description: In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7ec117598a6a008e5b274179659b515824029874
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="sales-tax-payments-and-rounding-rules"></a>Btw-betalingen en afrondingsregels

[!include[banner](../includes/banner.md)]


In dit artikel wordt uitgelegd hoe de instelling van afrondingregels voor de btw-dienst werkt en afronding van het btw-saldo tijdens de taak Btw vereffenen en boeken.

Periodiek moet btw worden aangegeven en betaald aan de belastingdienst. Dit kan worden uitgevoerd door het proces Btw vereffenen en boeken op de pagina Btw. Btw voor een periode wordt vereffend voor de btw-rekeningen en het btw-saldo wordt naar de rekening Btw-vereffening geboekt. Het btw-saldo, dat op de rekening Btw-vereffening wordt geboekt, kan worden afgerond zoals vereist wordt door de belastingdienst door een afrondingregel in te stellen op de pagina Btw. 

Het afrondingsverschil wordt geboekt naar de rekening Btw-afronding die is geselecteerd in het veld Rekeningen voor automatische transacties in het Grootboek.

Het onderstaande voorbeeld illustreert hoe de afrondingregel op Btw-dienst werkt.

### <a name="example"></a>    Voorbeeld:

De totale btw voor een periode toont een creditsaldo van -98.765,43. De rechtspersoon inde meer btw dan dat betaald werd. Daarom is de rechtspersoon geld verschuldigd aan de belastingsdienst. 

De rechtspersoon wil een afrondingsmethode gebruiken waarmee het saldo wordt afgerond naar de dichtstbijzijnde 1,00. De gebruiker die verantwoordelijk is voor de btw-boekhouding voert de volgende stappen uit.

1.  Klik op Btw &gt; Indirecte belastingen &gt; Btw &gt; Btw-diensten
2.  Selecteer op het sneltabblad Algemeen in het veld Afrondingstype de optie Normaal.
3.  Typ 1,00 in het veld Afronden.
4.  Wanneer het tijd is om de btw te betalen aan de belastingdienst, opent u de pagina Btw vereffenen en boeken. (Klik op Btw &gt; Aangiften &gt; Btw &gt; Btw vereffenen en boeken.)
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

Zie [Btw-overzicht](indirect-taxes-overview.md) voor meer informatie. 




