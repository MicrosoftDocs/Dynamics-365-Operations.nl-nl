---
title: Intercompany-valutaconversies
description: In dit artikel wordt uitgelegd wat valutaconversies voor intercompany-transacties zijn
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
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851473"
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
