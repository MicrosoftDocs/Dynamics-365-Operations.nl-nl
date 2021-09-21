---
title: Fout in kostprijsberekening terugwaarts afboeken bij afsluiting voorraad
description: In eerdere releases is er mogelijk sprake van een fout bij de kostprijsberekening terugwaarts afboeken bij het afsluiten van de voorraad. Dit probleem is opgelost.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475997"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Fout in kostprijsberekening terugwaarts afboeken bij afsluiting voorraad

## <a name="symptoms"></a>Symptomen

Als u in releases vóór release 10.0.13 de kostenstroom voor de lean-productie niet gebruikt, wordt tijdens de voorraadafsluiting het volgende onjuiste waarschuwingsbericht weergegeven:

> U staat op het punt een voorraadafsluiting uit te voeren met datum %1. Geen uitvoering van kostprijsberekening via terugwaarts afboeken geregistreerd met datum %1 overeenkomend met een periode-einde. Vergeet niet een kostprijsberekening via terugwaarts afboeken uit te voeren met datum %1 overeenkomend met een periode-einde. De waardering van voorraden, kosten van verkochte goederen en afwijkingen is mogelijk niet juist in subadministratie of grootboek totdat dit is uitgevoerd.

## <a name="resolution"></a>Oplossing

Dit probleem is opgelost in release 10.0.13 en hoger. Zie voor meer informatie [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
