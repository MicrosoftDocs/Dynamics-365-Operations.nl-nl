---
title: Beschikbare voorraad wordt niet in aanmerking genomen voor artikelen boven batch
description: Bij sommige vakkensjablonen wordt geen rekening met de beschikbare voorraad voor artikelen boven batch. Het batch- of serienummer moet worden opgegeven in de vraagorder.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476012"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Bij vakkensjablonen wordt geen rekening met de beschikbare voorraad voor artikelen boven batch

## <a name="symptoms"></a>Symptomen

Vaksjablonen met het criterium voor het vak *Voorhanden overwegen* houden geen rekening met de huidige voorhanden voorraad voor *batch-boven*-artikelen. Ze houden hier alleen rekening mee als het batchnummer is opgegeven op de verkooporderregel.

Wanneer u echter *batch-onder*-artikelen gebruikt, wordt zoals verwacht rekening gehouden met de huidige voorhanden voorraad.

Zie [Magazijnvakken](/dynamics365/supply-chain/warehousing/warehouse-slotting) voor meer informatie.

## <a name="resolution"></a>Oplossing

De header van de vakkensjabloon kan worden gedefinieerd voor de vraagstrategie *Besteld*, *Gereserveerd* of *Vrijgegeven*. Voor de vraagstrategie *Besteld* gelden dezelfde reserveringshiërarchievereisten als van toepassing zijn op reserveringsprocessen of processen voor vrijgave aan het magazijn. Daarom moet voor artikelen met *batch-boven*- en *serienummer-onder*-reserveringshiërarchieën het batch- of serienummer worden opgegeven op de vraagorder (verkoop of transfer).

Als alternatief kan de vraagstrategie *Gereserveerd* worden gebruikt om het batch- of serienummer te selecteren voordat de vraag voor magazijnvakken wordt gegenereerd.
