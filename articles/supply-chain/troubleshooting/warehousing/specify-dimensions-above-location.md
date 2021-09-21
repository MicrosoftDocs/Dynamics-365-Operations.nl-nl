---
title: Een lading voor een gedeeltelijke hoeveelheid kan niet worden vrijgegeven met een hiërarchie boven batch
description: Wanneer u een artikel met de reserveringshiërarchie boven batch gebruikt, moeten ladingsregels de afmetingen boven de locatie opgeven om de voorraad te kunnen toewijzen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475987"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Een lading voor een gedeeltelijke hoeveelheid kan niet worden vrijgegeven met een reserveringshiërarchie boven batch

## <a name="symptoms"></a>Symptomen

Wanneer u een artikel gebruikt met een *batch boven*-reserveringshiërarchie, werkt de opdracht **Vrijgeven aan magazijn** op de pagina **Workbench ladingplanning** niet als u probeert een lading voor een gedeeltelijke hoeveelheid vrij te geven. Mogelijk wordt het volgende foutbericht weergegeven:

> Om aan wave te worden toegewezen, moeten ladingsregels de afmetingen boven de locatie aangeven. Als u deze dimensies wilt toewijzen, moet u de ladingsregel reserveren en opnieuw maken.

Wanneer u echter een artikel gebruikt met een *batch-onder*-reserveringshiërarchie, kunt u een lading vrijgeven voor een gedeeltelijke hoeveelheid vanaf de pagina **Workbench ladingplanning**.

## <a name="cause"></a>Oorzaak

Als een dimensie zich boven de dimensie **Locatie** in de reserveringshiërarchie bevindt, moet deze eerst worden opgegeven voordat deze kan worden vrijgegeven aan het magazijn. Voorraad kan alleen worden toegewezen als er geen hiaten zijn in de dimensies boven locatie.

## <a name="resolution"></a>Oplossing

Zorg ervoor dat alle dimensies boven  **Locatie** zijn toegewezen door de ladingsregel te reserveren en opnieuw te maken.
