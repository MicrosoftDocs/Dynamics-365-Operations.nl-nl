---
title: Wisprincipe-instellingen op stuklijstregels worden niet in acht genomen
description: Wisprincipe-instellingen op stuklijstregels worden niet in acht genomen.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026407"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>Wisprincipe-instellingen op stuklijstregels worden niet in acht genomen

KB-nummer: 4612725

## <a name="symptoms"></a>Symptomen

Dit probleem treedt op wanneer het veld **Automatisch stuklijstverbruik** op het tabblad **Automatisch bijwerken** van de pagina **Parameters van productiebeheer** is ingesteld op *Wisprincipe*. Deze instelling geeft aan dat alle stuklijstregels automatisch moeten worden verbruikt wanneer een inkooporder wordt ontvangen. Als het veld **Wisprincipe** op stuklijstregels expliciet is ingesteld op *Handmatig*, kunt u verwachten dat de stuklijstregels niet automatisch worden verbruikt. Wanneer dit probleem zich echter voordoet, worden stuklijstregels waarbij het veld **Wisprincipe** is ingesteld op *Handmatig* toch automatisch verbruikt.

## <a name="resolution"></a>Oplossing

Als u dit probleem ondervindt, kunt u de parameters voor productiebeheer zo instellen dat de instelling **Wisprincipe** voor stuklijstregels wordt overgenomen. Controleer op de pagina **Parameters van productiebeheer** op het tabblad **Automatisch bijwerken** de waarde van het veld **Automatisch stuklijstverbruik**. Als de waarde is ingesteld op *Altijd*, wordt de instelling van **Wisprincipe** voor alle stuklijstregels genegeerd en worden de regels altijd leeggemaakt. Als u wilt instellen dat het systeem de instelling van **Wisprincipe** voor stuklijstregels in acht neemt, wijzigt u de waarde van het veld **Automatisch stuklijstverbruik** in *Wisprincipe*.
