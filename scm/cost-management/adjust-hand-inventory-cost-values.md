---
title: Kostenwaarden voor voorhanden voorraad corrigeren
description: Gebruik de pagina Correctie van voorhanden voorraad om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Kostenwaarden voor voorhanden voorraad corrigeren

Gebruik de pagina Correctie van voorhanden voorraad om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.

U kunt de pagina **Correctie van voorhanden voorraad** gebruiken om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd. **opmerking:** opent de **correctie van voorhanden voorraad** pagina op de **afsluiten en corrigeren** pagina en klik vervolgens op de record van een voltooid voorraadafsluitingsproces **correctie**&gt;**voorhanden**. **Voorbeeld:** u hebt de volgende transacties in februari:

-   1 februari: financiële ontvangst in voorraad voor een hoeveelheid van 2 tegen USD 10,00 aan kosten
-   5 februari: financiële ontvangst in voorraad voor een hoeveelheid van 1 tegen USD 13,00 aan kosten
-   19 februari: financiële voorraaduitgifte voor een hoeveelheid van 1 tegen een gemiddelde kostprijs van 11,00 EUR

Dit artikel is ingesteld met het FIFO-voorraadmodel (first in, first out) en de voorraadafsluiting is uitgevoerd vanaf 28 februari. De financiële uitgiftetransactie van USD 11.00 worden vereffend met de financiële ontvangst van 1 februari en een correctie van USD 1.00 worden uitgevoerd. De volgende voorraadontvangsten bevatten vervolgens openstaande voorraadhoeveelheden:

-   1 februari: een hoeveelheid van 1 tegen 10,00 EUR aan kosten
-   5 februari: een hoeveelheid van 1 tegen 13,00 EUR aan kosten

Als u de kosten van deze twee artikelen wilt instellen op USD 15,00, gebruikt u de optie voor het corrigeren van de voorhanden voorraad om de openstaande voorhanden hoeveelheden te corrigeren vanaf de laatste voorraadafsluitingsperiode. **Opmerking:** de boekingsdatum van de correctietransactie voor de voorhanden voorraad is de datum van de laatste voorraadafsluiting. Deze datum kan niet worden gewijzigd.


