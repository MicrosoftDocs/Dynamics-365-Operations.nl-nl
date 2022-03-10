---
title: Geïntegreerde belasting
description: In dit onderwerp wordt de integratie van belastinggegevens tussen Finance and Operations en Dataverse beschreven.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 532e6603b74ad0293d65684d2d6858ef31fbc496
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063182"
---
# <a name="integrated-tax"></a>Geïntegreerde belasting

[!include [banner](../../includes/banner.md)]



Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting. Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.

## <a name="templates"></a>Sjablonen

Belastinggegevens omvatten een verzameling tabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

| Apps voor financiële en bedrijfsactiviteiten | Customer Engagement-apps | Description |
|-----------------------------|-----------------------------------|-------------|
[Btw-groep voor artikel](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Btw-dienst](mapping-reference.md#193) | msdyn_taxauthorities | |
[Entiteit btw-vrijstellingscode voor CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Btw-groepen](mapping-reference.md#195) | msdyn_taxgroups | |
[Groepen van boekingen in btw-grootboek V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Bronbelastingcodes](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Bronbelastinggroepen](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
