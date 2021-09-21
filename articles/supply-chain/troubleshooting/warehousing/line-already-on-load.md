---
title: Een van de regels wordt reeds geladen
description: "Op deze pagina wordt uitgelegd waarom u mogelijk de volgende fout ontvangt: 'Een van de regels wordt reeds geladen. Kan niet worden vrijgegeven aan het magazijn' en hoe u het probleem kunt oplossen."
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476062"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Een van de regels wordt reeds geladen

## <a name="symptoms"></a>Symptomen

Wanneer u aan ladingopbouw en zendingen werkt, wordt mogelijk het volgende foutbericht weergegeven:

> Een van de regels wordt reeds geladen. Kan niet worden vrijgeven aan het magazijn.

Als u handmatig taken maakt of als u het proces zo instelt dat er al ladingen zijn gemaakt voordat de verkooporderregel wordt ingevoerd, is de veronderstelling dat de volgende vrijgave handmatig wordt uitgevoerd en dat de route en beoordeling van de lading wordt gebruikt.

In een ander mogelijk scenario probeert u een automatische vrijgave aan het magazijn uit te voeren, maar tijdens het waveproces kan er geen werk worden gemaakt. Daarom wordt toch een openstaande zending of lading gemaakt. Deze openstaande zending of lading blokkeert vervolgens alle pogingen om de order automatisch vrij te geven, totdat u de openstaande zending of lading verwijdert of de wave handmatig opnieuw verwerkt.

## <a name="resolution"></a>Oplossing

U kunt alleen vrijgeven vanaf de verkooporderpagina of een automatische vrijgave uitvoeren vanaf de vrijgaveverkooporderpagina als er geen lading bestaat voorafgaand aan de vrijgave aan het magazijn. De lading wordt automatisch gemaakt nadat de wave is verwerkt.
