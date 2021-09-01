---
title: U kunt de voorspelde eenheidskosten niet bijwerken wanneer u vraagprognoserecords importeert
description: Wanneer u gegevensentiteiten gebruikt om vraagprognoserecords te importeren, wordt de kostprijs voor bestaande records niet bijgewerkt, zodat deze overeenkomt met de geïmporteerde gegevens.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765365"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>U kunt de voorspelde eenheidskosten niet bijwerken wanneer u vraagprognoserecords importeert

KB-nummer: 4614109

## <a name="symptoms"></a>Symptomen

Wanneer u gegevensentiteiten gebruikt om vraagprognoserecords te importeren, wordt de waarde van **Voorspelde eenheidskosten** voor bestaande records niet bijgewerkt, zodat deze overeenkomt met de geïmporteerde gegevens.

## <a name="cause"></a>Oorzaak

**Voorspelde eenheidskosten** is een alleen-lezenveld. De waarde is gebaseerd op de kosten van de producteenheid en kan niet direct worden ingesteld via importeren.

## <a name="resolution"></a>Oplossing

Omdat het veld alleen-lezen is, kunt u er geen waarden voor importeren. De waarde wordt berekend volgens de bestaande bedrijfslogica.
