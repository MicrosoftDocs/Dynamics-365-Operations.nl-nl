---
title: Intercompany-batch- en serienummers
description: In dit onderwerp wordt uitgelegd wat er gebeurt wanneer u batchnummers en serienummers registreert voor intercompany-orders
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4da936263bb57c24eeb7021ac61b3945bb2777fb
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548205"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Intercompany-batch- en serienummers

[!include [banner](../../includes/banner.md)]

Bedrijven die serienummers of batchnummers gebruiken om hun artikelen te traceren, moeten ook de serienummers of batchnummers van verzamelde artikelen bijhouden. De intercompany-functie automatiseert het zenden/ontvangen van serienummers en batchnummers van het ene bedrijf naar het andere. Wanneer u de serienummers en batchnummers voor de artikelen registreert op een intercompany-verkooporder, kunt u het programma instellen om deze automatisch naar de intercompany-inkooporder en de oorspronkelijke verkooporder te zenden. U moet de relevante parameters instellen op de pagina **Intercompany** voor de verkooporder:

- Als u het veld **Batchnummer** op de pagina **Beleid voor verkooporders** selecteert, wordt het batchnummer gesynchroniseerd met de voorraadtransacties op de intercompany-inkooporderregels wanneer u de pakbon van de intercompany-verkooporder boekt.
- Als u het veld **Serienummer** selecteert, worden de serienummers gesynchroniseerd met de voorraadtransacties op de intercompany-inkooporderregels wanneer u de pakbon van de intercompany-verkooporder boekt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
