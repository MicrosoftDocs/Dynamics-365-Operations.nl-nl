---
title: Kostenwaarden voor voorhanden voorraad corrigeren
description: Gebruik de pagina Correctie van voorhanden voorraad om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7f7c1008eea83bbda96ace92cd4aedf09c8febdc
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Kostenwaarden voor voorhanden voorraad corrigeren

[!include[banner](../includes/banner.md)]


Gebruik de pagina Correctie van voorhanden voorraad om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.

U kunt de pagina **Correctie van voorhanden voorraad** gebruiken om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd. **Opmerking:** als u de pagina **Correctie van voorhanden voorraad** wilt openen, selecteert u op de pagina **Afsluiten en corrigeren** de record van een voltooid voorraadafsluitingsproces en klikt u vervolgens op **Correctie** &gt; **Voorhanden**. **Voorbeeld:** u hebt de volgende transacties in februari:

-   1 februari: financiële ontvangst in voorraad voor een hoeveelheid van 2 tegen USD 10,00 aan kosten
-   5 februari: financiële ontvangst in voorraad voor een hoeveelheid van 1 tegen USD 13,00 aan kosten
-   19 februari: financiële voorraaduitgifte voor een hoeveelheid van 1 tegen een gemiddelde kostprijs van 11,00 EUR

Dit artikel is ingesteld met het FIFO-voorraadmodel (first in, first out) en de voorraadafsluiting is uitgevoerd vanaf 28 februari. De financiële uitgiftetransactie van USD 11,00 wordt vereffend met de financiële ontvangst van 1 februari en er wordt een correctie van USD 1,00 doorgevoerd. De volgende voorraadontvangsten bevatten vervolgens openstaande voorraadhoeveelheden:

-   1 februari: een hoeveelheid van 1 tegen 10,00 EUR aan kosten
-   5 februari: een hoeveelheid van 1 tegen 13,00 EUR aan kosten

Als u de kosten van deze twee artikelen wilt instellen op USD 15,00, gebruikt u de optie voor het corrigeren van de voorhanden voorraad om de openstaande voorhanden hoeveelheden te corrigeren vanaf de laatste voorraadafsluitingsperiode. **Opmerking:** de boekingsdatum van de correctietransactie voor de voorhanden voorraad is de datum van de laatste voorraadafsluiting. Deze datum kan niet worden gewijzigd.




