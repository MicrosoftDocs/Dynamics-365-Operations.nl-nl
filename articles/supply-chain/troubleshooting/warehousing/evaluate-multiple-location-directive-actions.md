---
title: Alle acties voor locatie-instructies met meerdere SKU's evalueren
description: Er is een nieuwe functie toegevoegd om alle acties van locatie-instructies voor meerdere SKU's te evalueren. Deze pagina begeleidt u naar informatie over het inschakelen van de functie.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475995"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>De optie meerdere SKU's evalueert niet meerdere acties voor locatie-instructies

## <a name="symptoms"></a>Symptomen

Locatie-instructies van het werkordertype *Verkooporders* en het werktype *Wegzetten* evalueren meerdere acties van een locatie-instructie niet wanneer de optie **Meerdere SKU's** is geselecteerd. Alleen de eerste actie van een locatie-instructie wordt geëvalueerd.

## <a name="resolution"></a>Oplossing

Een nieuwe functie *Alle acties van locatie-instructies voor meerdere SKU's evalueren* is toegevoegd in versie 10.0.15 (zie [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Met deze functie worden alle acties van locatie-instructies voor meerdere SKU's geëvalueerd. Als u deze functie nodig hebt, kunt u deze met [Functiebeheer](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) inschakelen.