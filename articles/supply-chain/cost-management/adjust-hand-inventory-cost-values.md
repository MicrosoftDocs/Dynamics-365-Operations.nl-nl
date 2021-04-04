---
title: Kostenwaarden voor voorhanden voorraad corrigeren
description: Gebruik de pagina Correctie van voorhanden voorraad om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66323e99c04a141aa5dc5ab828e0e261c61b83ce
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254330"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Kostenwaarden voor voorhanden voorraad corrigeren

[!include [banner](../includes/banner.md)]

Gebruik de pagina Correctie van voorhanden voorraad om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd.

U kunt de pagina **Correctie van voorhanden voorraad** gebruiken om de kostprijs van de voorhanden voorraadhoeveelheden aan te passen nadat het voorraadafsluitingsproces is uitgevoerd. **Opmerking:** als u de pagina **Correctie van voorhanden voorraad** wilt openen, selecteert u op de pagina **Afsluiten en corrigeren** de record van een voltooid voorraadafsluitingsproces en klikt u vervolgens op **Correctie** &gt; **Voorhanden**. **Voorbeeld:** u hebt de volgende transacties in februari:

-   1 februari: financiële ontvangst in voorraad voor een hoeveelheid van 2 tegen USD 10,00 aan kosten
-   5 februari: financiële ontvangst in voorraad voor een hoeveelheid van 1 tegen USD 13,00 aan kosten
-   19 februari: financiële voorraaduitgifte voor een hoeveelheid van 1 tegen een gemiddelde kostprijs van 11,00 EUR

Dit artikel is ingesteld met het FIFO-voorraadmodel (first in, first out) en de voorraadafsluiting is uitgevoerd vanaf 28 februari. De financiële uitgiftetransactie van USD 11,00 wordt vereffend met de financiële ontvangst van 1 februari en er wordt een correctie van USD 1,00 doorgevoerd. De volgende voorraadontvangsten bevatten vervolgens openstaande voorraadhoeveelheden:

-   1 februari: een hoeveelheid van 1 tegen 10,00 EUR aan kosten
-   5 februari: een hoeveelheid van 1 tegen 13,00 EUR aan kosten

Als u de kosten van deze twee artikelen wilt instellen op USD 15,00, gebruikt u de optie voor het corrigeren van de voorhanden voorraad om de openstaande voorhanden hoeveelheden te corrigeren vanaf de laatste voorraadafsluitingsperiode. **Opmerking:** de boekingsdatum van de correctietransactie voor de voorhanden voorraad is de datum van de laatste voorraadafsluiting. Deze datum kan niet worden gewijzigd.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]