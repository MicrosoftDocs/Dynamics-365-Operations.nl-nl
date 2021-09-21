---
title: Productieplanning houdt geen rekening met de veiligheidsmarges
description: Productieplanning houdt geen rekening met de veiligheidsmarges die zijn ingesteld voor de artikelbehoefte voor getraceerd aanbod
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475991"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Productieplanning houdt geen rekening met de veiligheidsmarges

## <a name="symptoms"></a>Symptomen

Met de veiligheidsmarges wordt in de hoofdplanning rekening gehouden. De veiligheidsmarges worden echter genegeerd wanneer geplande productieorders worden gepland.

## <a name="resolution"></a>Oplossing

Met marges wordt alleen rekening gehouden tijdens de hoofdplanning, niet tijdens handmatige planning. Marges zijn ontworpen om als een buffer te fungeren tijdens de planningsfase, om enige speling te bieden voor het feitelijke proces.

U kunt het gewenste resultaat weergeven door de marge te verwijderen. De route moet vervolgens worden bijgewerkt zodat deze de gewenste tijd omvat (bijvoorbeeld de wachttijd voor de wachtrijen). De hoofdplanning en de handmatige planning moeten vervolgens hetzelfde resultaat opleveren.
