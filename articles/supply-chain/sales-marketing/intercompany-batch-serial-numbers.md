---
title: Intercompany-batch- en serienummers
description: In dit artikel wordt uitgelegd wat er gebeurt wanneer u batchnummers en serienummers registreert voor intercompany-orders
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5c743c8eee8d27a2c2357523a11236eb247ec5be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851502"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Intercompany-batch- en serienummers

[!include [banner](../../includes/banner.md)]

Bedrijven die serienummers of batchnummers gebruiken om hun artikelen te traceren, moeten ook de serienummers of batchnummers van verzamelde artikelen bijhouden. De intercompany-functie automatiseert het zenden/ontvangen van serienummers en batchnummers van het ene bedrijf naar het andere. Wanneer u de serienummers en batchnummers voor de artikelen registreert op een intercompany-verkooporder, kunt u het programma instellen om deze automatisch naar de intercompany-inkooporder en de oorspronkelijke verkooporder te zenden. U moet de relevante parameters instellen op de pagina **Intercompany** voor de verkooporder:

- Als u het veld **Batchnummer** op de pagina **Beleid voor verkooporders** selecteert, wordt het batchnummer gesynchroniseerd met de voorraadtransacties op de intercompany-inkooporderregels wanneer u de pakbon van de intercompany-verkooporder boekt.
- Als u het veld **Serienummer** selecteert, worden de serienummers gesynchroniseerd met de voorraadtransacties op de intercompany-inkooporderregels wanneer u de pakbon van de intercompany-verkooporder boekt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
