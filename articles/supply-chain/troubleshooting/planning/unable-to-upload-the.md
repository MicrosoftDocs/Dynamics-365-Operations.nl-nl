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
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026409"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>U kunt de voorspelde eenheidskosten niet bijwerken wanneer u vraagprognoserecords importeert

KB-nummer: 4614109

## <a name="symptoms"></a>Symptomen

Wanneer u gegevensentiteiten gebruikt om vraagprognoserecords te importeren, wordt de waarde van **Voorspelde eenheidskosten** voor bestaande records niet bijgewerkt, zodat deze overeenkomt met de geïmporteerde gegevens.

## <a name="cause"></a>Oorzaak

**Voorspelde eenheidskosten** is een alleen-lezenveld. De waarde is gebaseerd op de kosten van de producteenheid en kan niet direct worden ingesteld via importeren.

## <a name="resolution"></a>Oplossing

Omdat het veld alleen-lezen is, kunt u er geen waarden voor importeren. De waarde wordt berekend volgens de bestaande bedrijfslogica.
