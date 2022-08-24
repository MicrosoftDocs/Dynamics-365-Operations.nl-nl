---
title: Geïntegreerde belasting
description: In dit artikel wordt de integratie van belastinggegevens tussen apps voor financiën en bedrijfsactiviteiten en Dataverse beschreven.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288789"
---
# <a name="integrated-tax"></a>Geïntegreerde belasting

[!include [banner](../../includes/banner.md)]



Belastinginstellingsgegevens bepalen de instellingen voor zowel indirecte belastingen (btw, GST, omzetbelasting) als bronbelasting. Het beschrijft de regel voor belastingberekening, het belastingtarief, belastingboekhouding, vereffening en andere concepten.

## <a name="templates"></a>Sjablonen

Belastinggegevens omvatten een verzameling tabeltoewijzingen die samenwerken tijdens de interactie van gegevens, zoals in de volgende tabel wordt weergegeven.

| Apps voor financiën en bedrijfsactiviteiten | Customer Engagement-apps | Description |
|-----------------------------|-----------------------------------|-------------|
[Btw-groep voor artikel](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Btw-dienst](mapping-reference.md#193) | msdyn_taxauthorities | |
[Entiteit btw-vrijstellingscode voor CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Btw-groepen](mapping-reference.md#195) | msdyn_taxgroups | |
[Groepen van boekingen in btw-grootboek V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Bronbelastingcodes](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Bronbelastinggroepen](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

