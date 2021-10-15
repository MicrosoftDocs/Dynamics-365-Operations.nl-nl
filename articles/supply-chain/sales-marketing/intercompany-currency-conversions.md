---
title: Intercompany-valutaconversies
description: In dit onderwerp wordt uitgelegd wat valutaconversies voor intercompany-transacties zijn
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
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548203"
---
# <a name="intercompany-currency-conversions"></a>Intercompany-valutaconversies

[!include [banner](../../includes/banner.md)]

Wanneer de valutacodes op de oorspronkelijke verkooporder en de intercompany-inkooporder niet overeenkomen, wordt de valuta voor de volgende velden omgerekend als synchronisatie wordt ingesteld:

- **Eenheidsprijs**
- **Verkoopkosten** of **Toeslagen op inkopen**
- **Korting**
- **Meerregelkorting**

Vervolgens worden deze velden gesynchroniseerd met de intercompany-verkooporderregel.

Aangezien de valuta op de intercompany-inkooporder en de intercompany-verkooporder echter altijd wordt gesynchroniseerd, worden de volgende velden gesynchroniseerd zonder valutaomrekening:

- **Eenheidsprijs**
- **Verkoopkosten** of **Toeslagen op inkopen**
- **Korting**
- **Kortingspercentage**
- **Meerregelkorting**
- **Meerregelkortingspercentage**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
